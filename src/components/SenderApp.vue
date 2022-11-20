<template>
  <div>
    <h1>Sender component</h1>
    <textarea v-model='msg'></textarea>
    <button @click='send()'>Send</button>
  </div>
  
</template>

<script>
// import EventBus from './EventBus'

export default {
  data() {
    return {
      msg: '',
      msgs: []
    }
  },
  methods: {
    send(){
      this.msgs.push({content:this.msg});
      this.msg = '';
      this.$emit('sendMessage',this.msgs);

    }
  }
}
</script>
