<template>
  <div id="app">
    <hello-world/>
    <working/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Working from './components/working.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Working
  }
}
</script>

<style>

</style>
