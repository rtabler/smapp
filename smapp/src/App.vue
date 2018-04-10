<template>
  <div id="app">
    <div id="top-bar">
      <h1>Social Media Something</h1>
      <h2>
        Do you know what social media doing to you?
        <br>
        Take this quiz to find out!
      </h2>
    </div>
    <quiz></quiz>
    <!-- <test></test> -->
  </div>
</template>

<script>
import Test from './components/Test'
import Quiz from './components/Quiz'

export default {
  name: 'App',
  components: {
    Test,
    Quiz
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: cyan;
  /*margin-top: 60px;*/
}
#top-bar {
  /*background-color: red;*/
  /*height: 90px;*/
}
h1 {
  background-color: red;
  margin: 0px;
  padding: 12px;
  font-size: 22pt;
}
h2 {
  background-color: orange;
  margin: 0px;
  padding: 6px;
  font-size: 12pt;
}
</style>
