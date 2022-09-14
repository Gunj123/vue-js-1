<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <ul>
    <li v-for="item in user" :key="item.name">
      <user :data="item" :getdata="getdata"/>
    </li>
  </ul>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import user from './components/user.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    user
  },
  methods:{
    getdata(name){
      alert(name)
    }
  },
  data() {
    return {
      user: [{ name: 'gunjan', email: 'gunjan.goswami.9@gmail.com' },
      { name: 'sanjana', email: 'sanjana.bharadiya.9@gmail.com' },
      { name: 'anil', email: 'anil.goswami.9@gmail.com' }
      ]
    }
  },
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
