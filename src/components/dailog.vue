<template>
  <div class="dialog" v-show="isShow">
    <div>
      <h1> Dialog </h1>
      <button @click="close">关闭</button>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        isShow: false,
        name: 'Compomnents Name'
      }
    },
    activated() {
      console.log('%c [Dialog] - activated ', 'background:#000066;color:#ffffff;')
    },
    beforeCreate() {
      console.log('%c [Dialog] - beforeCreate]', 'background:#003366;color:#ffffff;')
    },
    beforeDestroy() {
      console.log('%c [Dialog] - beforeDestroy ', 'background:#006666;color:#ffffff;')
    },
    created() {
      console.log('%c [Dialog] - created ', 'background:#009966;color:#ffffff;')
    },
    destroyed() {
      console.log('%c [Dialog] - destroyed ', 'background:#00CC66;color:#ffffff;')
    },
    mounted() {
      console.log('%c [Dialog] - mounted ', 'background:#00FF66;color:#ffffff;')
    },
    methods: {
      open() {
        this.isShow = true
      },
      close() {
        this.isShow = false
      }
    },
    components: {},
    computed: {}
  }
</script>
<style scoped>
  .dialog {
    position: fixed;
    background-color: #ffffff;
    border: 1px solid #000000;
    width: 200px;
    height: 150px;
    box-shadow: 0 0 3px rgba(0, 0, 0, .5);
    top: 50%;
    left: 50%;
    margin: -75px 0 0 -100px;
    box-sizing: border-box;
  }
</style>
