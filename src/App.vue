<template>
  <div id="app">
    <button id="switch" @click="isGrid = !isGrid"> style switch</button>
    <div id="tweets" v-bind:class="{gridTweets:isGrid}">
      <pageTweet content="This is the first tweet on vue" date="17/09/2020" user="khaled" />
      <pageTweet content="This is the second tweet on vue" date="17/09/2020" user="rainer" />
      <pageTweet content="This is the third tweet on vue" date="17/09/2020" user="alex" />

    </div>
  </div>
</template>

<script>
import pageTweet from './components/tweet.vue' 

export default {
  name: 'App',
  components: {
    pageTweet
  },
  data:function() {
    return{
    isGrid:false
  }
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

.gridTweets{
  display: grid;
  grid-template-columns: repeat(3,1fr) ;
  align-items: center;
  justify-items: center;
}
#tweets{
  display: grid;
  align-items: center;
  justify-items: center;
}
#switch{
  background-color: green;
  color: white;
  width: 200px;
  height: 50px;
}
</style>
