<template>
  <div id="app">
    
    <nav>
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        </ul>
      </nav>
    <router-view></router-view>
    <component v-bind:is="cmp"> </component>

    <button v-on:click="updateCmp('signin')">Sign In </button>
    <button v-on:click="updateCmp('signup')">Sign Up </button>
    
    
   
  </div>
</template>

<script>
import SignIn from './components/SignIn.vue'
import SignUp from './components/SignUp.vue'
export default {
  name: 'App',

  components:{
    'signin' : SignIn,
    'signup' : SignUp
  },
  data(){
    return{cmp:'signup'}
  },
  methods:{
    updateCmp(item)
    {
      this.cmp=item
    }
  }
 
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
