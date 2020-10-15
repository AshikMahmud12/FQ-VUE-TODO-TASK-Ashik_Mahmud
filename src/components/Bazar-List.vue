<template>
  <div id="app">
    <div class="container " >
      <div class="row ">
<div class="col-md-4 ml-5 ">

<h3 class="text-center mb-4">Bazar List</h3>

<input class="input" v-model="newToDo" >
<button class="add-button ml-3" v-on:click="add()">Add</button>
<ul style="list-style-type: none;">
<li v-for="(todo, index) in existingToDo" :key="index.id" class="mt-3">
<span>
  {{ index + 1  }}: {{ todo.text }} - <input v-model="todo.price" />
</span>
 
 <button class="btn btn-danger ml-4" @click="removeItem(index)">Del</button>


</li>
 <li class="list-group-item mt-3">Total - {{ total }}</li>
</ul>

        
        </div>
        </div>
  </div>
  </div>
</template>

<script>
export default{
  name:'app',
  data(){
    return {
newToDo: '',
existingToDo:[
  { text: 'rice',price: 12.5,  id:0 },                      
  { text: 'wheat', price: 12.5, id:1 },
  { text: 'oil', price: 12.5,  id:2 }
]
    }
  },
    computed: {
                    total() {
                        var total = 0;
                        this.existingToDo.forEach((todo) => {
                            total += parseFloat(todo.price);
                        });
                        return total;
                    }
                },
  methods: {
     add(){
      this.existingToDo.push({
        text: this.newToDo,
        id: new Date().valueOf(),
         price: 0.0,
      }),
      this.newToDo=''
    },
    removeItem(index){
      this.existingToDo.splice(index,1 )
    }
  }
  
}


</script>


<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
