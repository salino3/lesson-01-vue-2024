<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <MyComponent />
  <br>
  <SecondComponent />
</template>

<script>
import MyComponent from './components/MyComponent.vue';
import SecondComponent from './components/SecondComponent.vue';

export default {
  name: 'App',
  components: {
    MyComponent,
    SecondComponent
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
