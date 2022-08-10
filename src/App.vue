<template>
  <div id="app">
   
    <HelloWorld msg="Calculadora Vue.Js"/>   
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
},
props:{
  selectedS:[]
}

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  background-color: #cdf0d3;
  margin-top: 20px;
}


</style>
