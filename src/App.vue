<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Calculadora Vue.Js"/>
    <ComponentTable/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ComponentTable from './components/ComponentTable.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ComponentTable
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  background-color: #cdf0d3;
  margin-top: 20px;
  justify-content: space-between;

}

img{
  width: 100px;
  height: 100px;
}
</style>
