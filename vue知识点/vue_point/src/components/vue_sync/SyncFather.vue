<template>
  <div class="father">
    <sync-child :age = "age" :str = "str"/>
    <button @click="add($event)">按钮</button>
    <hr>
    <input type="text"  v-model = "str">
  </div>
</template>

<script>
import SyncChild from './SyncChild.vue'

export default {
  components: {SyncChild },
  //组件中定义data属性 只能是函数 
  // data 对象就是要渲染到页面上的内容
  data(){
    return{
      age :8,
      str:'性张力'
    }

  },
  methods:{
    add(e){
     console.log(e.target);// 事件对象的目标
    }
  }
}
</script>

<style>

</style>