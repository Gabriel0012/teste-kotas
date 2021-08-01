<template>
  <HomePage msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    HomePage
  }
}
</script>

<style>
#app {
  /* font-family: Mulish; */
  font-family: Mulish, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* color: #2c3e50; */
}

.card {
  border-radius: 10px;
  background-color: white;
  text-align: center;
  padding: 10px;
  box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
  margin: 16px 0;
}

.card h4 {
  color: #141728;
  font-size: 18px;
}

.cols,.cols-label {
  display: flex;
  justify-content: space-between;
}
</style>
