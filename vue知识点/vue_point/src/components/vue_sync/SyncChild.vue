<template>
  <div class="children">
    <h1>{{age}}</h1>
    <input type="text"  :value=$emit(str)>
  </div>
</template>

<script>
export default {
  props:['age','str']
};
</script>

<style>
</style>  