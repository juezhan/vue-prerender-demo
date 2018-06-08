<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!--<router-link :to="{path:'/test/', params:{app:'123'}}">/test</router-link>-->
    <router-link to="/test/myapp">/test</router-link>
    <button @click="openDialog">Open Dialog</button>
    <my-dailog ref="myDailog"></my-dailog>
  </div>
</template>

<script>
  import MyDailog from './dailog'

  export default {
    name: 'hello',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    methods: {
      openDialog() {
        console.log('this.$refs.myDailog:', this.$refs)
        this.$refs.myDailog.open()
      }
    },
    components: {
      MyDailog
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
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
