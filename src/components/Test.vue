<template>
  <div>
    <p>jusn a test page</p>
    <router-link to="/">回到首页</router-link>
  </div>
</template>
<script>
  export default {
    activated() {
      console.log('%c [Test] - activated ', 'background:#ffffff;color:#000066;')
    },
    beforeCreate() {
      console.log('%c [Test] - beforeCreate]', 'background:#ffffff;color:#003366;')
    },
    beforeDestroy() {
      console.log('%c [Test] - beforeDestroy ', 'background:#ffffff;color:#006666;')
    },
    created() {
      console.log('%c [Test] - created ', 'background:#ffffff;color:#009966;')
    },
    destroyed() {
      console.log('%c [Test] - destroyed ', 'background:#ffffff;color:#00CC66;')
    },
    mounted() {
      console.log(this.$route.params)
    }
  }
</script>
