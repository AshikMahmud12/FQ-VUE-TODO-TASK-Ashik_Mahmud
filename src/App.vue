<template>
  <div id="app">
  <List></List>
  <product></product>
          
 </div> 
</template>

<script>
 import BazarList from './components/Bazar-List.vue'
 import Data from './components/productAdding'

export default {
  name: 'App',
 components:{
List: BazarList,
product: Data
 }


}


</script>

<style>
   
</style>
