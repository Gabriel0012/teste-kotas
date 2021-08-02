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

@media screen and (max-width: 480px) {
  .card {
    box-shadow: 0px 4px 20px rgba(225, 225, 225, 0.5);
    border-radius: 10px;
  }
}

@media screen and (min-width: 481px) {
  .card {
    box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
    border-radius: 10px;
  }
}

.card {
  background-color: white;
  text-align: center;
  padding: 10px;
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

.text-center {
  text-align: center;
}

.text-right {
  text-align: right;
}
</style>
