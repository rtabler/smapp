<template>
  <div id="app">
    <div id="top-bar">
      <a class="main-header-link" href="index.html"><h1 class="main-header noselect">LogOUT</h1></a>
      <h2 v-if="!quizActive" class="subtitle">
        Do you know what social media doing to you?
        <br>
        Take this quiz to find out!
      </h2>
    </div>
    <button class="big-button" v-if="!quizActive" v-on:click="beginQuiz()">BEGIN QUIZ</button>
    <quiz v-if="quizActive"></quiz>

    <div class="share-footer">
      <p>Share this site to help a friend!</p>
      <ul class="share-buttons">
        <li><a href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Frtabler.github.io%2Fsmapp%2F&quote=" title="Share on Facebook" target="_blank" onclick="window.open('https://www.facebook.com/sharer/sharer.php?u=' + encodeURIComponent(document.URL) + '&quote=' + encodeURIComponent(document.URL)); return false;"><img alt="Share on Facebook" src="./images/social_flat_rounded_rects_svg/Facebook.svg" /></a></li>
        <li><a href="https://twitter.com/intent/tweet?source=https%3A%2F%2Frtabler.github.io%2Fsmapp%2F&text=:%20https%3A%2F%2Frtabler.github.io%2Fsmapp%2F" target="_blank" title="Tweet" onclick="window.open('https://twitter.com/intent/tweet?text=' + encodeURIComponent(document.title) + ':%20'  + encodeURIComponent(document.URL)); return false;"><img alt="Tweet" src="./images/social_flat_rounded_rects_svg/Twitter.svg" /></a></li>
        <li><a href="https://plus.google.com/share?url=https%3A%2F%2Frtabler.github.io%2Fsmapp%2F" target="_blank" title="Share on Google+" onclick="window.open('https://plus.google.com/share?url=' + encodeURIComponent(document.URL)); return false;"><img alt="Share on Google+" src="./images/social_flat_rounded_rects_svg/Google+.svg" /></a></li>
        <li><a href="http://pinterest.com/pin/create/button/?url=https%3A%2F%2Frtabler.github.io%2Fsmapp%2F&description=" target="_blank" title="Pin it" onclick="window.open('http://pinterest.com/pin/create/button/?url=' + encodeURIComponent(document.URL) + '&description=' +  encodeURIComponent(document.title)); return false;"><img alt="Pin it" src="./images/social_flat_rounded_rects_svg/Pinterest.svg" /></a></li>
        <li><a href="http://www.reddit.com/submit?url=https%3A%2F%2Frtabler.github.io%2Fsmapp%2F&title=" target="_blank" title="Submit to Reddit" onclick="window.open('http://www.reddit.com/submit?url=' + encodeURIComponent(document.URL) + '&title=' +  encodeURIComponent(document.title)); return false;"><img alt="Submit to Reddit" src="./images/social_flat_rounded_rects_svg/Reddit.svg" /></a></li>
        <li><a href="mailto:?subject=&body=:%20https%3A%2F%2Frtabler.github.io%2Fsmapp%2F" target="_blank" title="Send email" onclick="window.open('mailto:?subject=' + encodeURIComponent(document.title) + '&body=' +  encodeURIComponent(document.URL)); return false;"><img alt="Send email" src="./images/social_flat_rounded_rects_svg/Email.svg" /></a></li>
      </ul>
    </div>
    <!-- <test></test> -->
  </div>
</template>

<script>
import Test from './components/Test'
import Quiz from './components/Quiz'
import ShareScreen from './components/ShareScreen'

export default {
  name: 'App',
  components: {
    Test,
    Quiz,
    ShareScreen
  },
  data: function() {
    return {
      quizActive: true
    };
  },
  computed: {

  },
  methods: {
    beginQuiz: function() {
      this.quizActive = true;
    }
  }
}
</script>

<style>
body {
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /*background-color: ;*/
  /*margin-top: 60px;*/
}
.main-header {
  font-family: Helvetica;
  font-weight: bold;
}
#top-bar {
  /*background-color: red;*/
  /*height: 90px;*/
}
.big-button {
  display: block;
  box-sizing: border-box;
  /*background-color: green;*/
  margin: auto;
  margin-top: 8px;
  margin-bottom: 8px;
  border-style: solid;
  border-width: 1px;
  border-radius: 10px;
  padding: 10px;
  color: black;
  font-family: "Avenir";
  text-decoration: none;
  font-size: 16pt;
  font-weight: bold;
  width: 90%;
}
.subtitle {
  background-color: rgb(255,219,109);
  color: black;
  margin: 0px;
  padding: 6px;
  font-size: 12pt;
}








/* copied from universal.css */
.main-header-link {
  text-decoration: none;
}
.main-header {
  font-family: Helvetica;
  font-weight: bold;
}
.resources-pre {
  text-align: left;
  margin: 16px;
}
.resources-link {
  display: block;
  box-sizing: border-box;
  /*background-color: green;*/
  /*background-color: #9DB4E5;*/
  background-color: #fee49b;
  padding: 10px;
  color: black;
  font-family: "Avenir";
  font-weight: bold;
  text-decoration: none;
}
.share-footer {
  background-color: rgb(59,89,152);
  /*background-color: #5986E5;*/
  color: white;
  box-sizing: border-box;
  padding: 8px;
  padding-bottom: 20px;
}
/* https://simplesharingbuttons.com/#code */
ul.share-buttons{
  list-style: none;
  padding: 0;
  margin: 0;
  margin-top: 8px;
  margin-bottom: 8px;
}
ul.share-buttons li{
  display: inline;
}
ul.share-buttons .sr-only{
  position: absolute;
  clip: rect(1px 1px 1px 1px);
  clip: rect(1px, 1px, 1px, 1px);
  padding: 0;
  border: 0;
  height: 1px;
  width: 1px;
  overflow: hidden;
}
ul.share-buttons img{
  width: 32px;
}



</style>
