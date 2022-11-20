<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <SenderApp v-on:sendMessage='sendMessage'/>
  <ReceiverApp :msgs = 'msgs'/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import SenderApp from './components/SenderApp.vue'
import ReceiverApp from './components/ReceiverApp.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    SenderApp,
    ReceiverApp
  },
  data () {
    return {
      msgs: ["abcs","avscadfg"],
    };
  },methods: {
    sendMessage () {
      
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
</style>
