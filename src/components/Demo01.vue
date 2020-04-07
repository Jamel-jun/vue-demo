<style>
  .red{
    background-color: red;
  }
  .yellow{
    background-color: yellow;
  }
</style>
<template>
  <div class="hello">
    {{msg}}
    <p>{{myage}}</p>
    <p v-text="myage"></p>
    <div :class="isActive?'red':'yellow'" @click="click01">切换Class，进行高亮显示</div>
    <div v-if="isCreate">我是动态创建的</div>
    <div v-show="isShow">IsShow</div>
  </div>
</template>

<script>
export default {
  name: 'Demo01',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      myage: 100,
      isActive: true,
      isCreate: false,
      isShow: true
    }
  },
  methods: {
    click01(){
      this.isActive = !this.isActive;
    }
  }
}
</script>
