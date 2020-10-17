
<template>
  <div class="dashboard mt-5 container">
    
<table class="table table-bordered">
    
 <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Item</th>
      <th scope="col">Price</th>
    
    </tr>
  </thead>
  
  <tbody>
    <tr v-for="project in projects" :key="project.id">
         
      <th scope="row">{{  project.id }}</th>
      <td>{{  project.Item }}</td>
      <td>{{  project.price }}</td>
     
    </tr>
    
  </tbody>
   
</table>
 </div>

</template>

<script>
export default {
  data() {
    return {
      projects: [
        { id: '1', Item: 'Onion', price: '80' },
        {  id: '2' ,Item: 'Potato', price: '40'},
        {  id: '3', Item: 'Apple', price: '100'},
        { id: '4', Item: 'Banana', price: '30' },
      ]
    }
  }
}
</script>

<style>

</style>