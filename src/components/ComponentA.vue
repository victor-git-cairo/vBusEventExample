<template> 
    <button v-on:click="sayHi" class="p-4 border bg-gray-100 rounded-lg mb-12">Say Hi to component B</button>   
</template>

<script>

import {EventBus} from '../main'
export default {
  name: 'ComponentA',
  props: {
    msg: String
  },
  methods: {
    sayHi: function(){
      EventBus.$emit('say-hi')

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
