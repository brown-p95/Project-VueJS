<template>
<div id="app">
  <img alt="Vue logo" src="./assets/logo.png">
  <title2 text="2.0"/>
  <Cuenta/>
</div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import title2 from './components/title2.vue';
import Cuenta from './components/Cuenta.vue';
export default {
  name: 'App',
  components: {
    title2,Cuenta
    
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
