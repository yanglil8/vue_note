<template>
  <div id="app">
     <sync-father />
  </div>
</template>

<script>
import SyncFather from './components/vue_sync/SyncFather.vue'

export default {
  name: 'App',
  components: {
    SyncFather
  }
}
</script>

<style>
#app{
  margin: 50px auto;
}
</style>
