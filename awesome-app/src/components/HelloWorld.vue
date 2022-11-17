<template>
  <div class="hello">
    <h1>Welcome to Your Vue.js App</h1>
    <button @click="showUsername = !showUsername">Toggle button</button>
  <div v-if="showUsername">
  <BigYellowUsernameVue username="irenakoval" />
  </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {
  components: {
    BigYellowUsernameVue: defineAsyncComponent(() => import(/* webpackChunkName: 'BigYellowUsername' */'./BigYellowUsername.vue'))
  },
  data () {
    return {
      showUsername: false
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
