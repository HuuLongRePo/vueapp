<template>
  <div>
    <h1>Receiver component</h1>
    <ul>
      <li v-for='mess in msgs' :key='mess'> {{mess}}</li>
    </ul>
  </div>

</template>

<script >
  // import EventBus from './EventBus'

export default {
props: {
  msgs: {
    type: Array, // String, Number, Boolean, Function, Object, Array
    required: true,
    default: ()=>{return []}
  }
},
data () {
  return {
    msg:'Receiver App message'
  };
}
}
</script>