<template>

  <Navbars/>
  <Forms/>
  <Items/>
  
  
</template>

<script>
import Navbars from './components/NavbarView.vue'
import Forms from './components/FormViews.vue'


export default {
  name: 'App',
  components: {
    Navbars,
    Forms,
  }
}
</script>

<style>
#app {
  width: 50%;
  align-items: center;
  text-align: center;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: auto;
  border: solid 2px red ;
  border-radius: 10px;
  border-style: dashed;
  padding: 25px 5px;
}

</style>
