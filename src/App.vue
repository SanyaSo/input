<template>
  <div id="app">
    <input type="text" v-model="text">
    <button v-on:click="handleButton">оқу</button>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      text: []
    }
  },
  methods:{
    handleButton: function(){
        let value
        if(this.text.length > 10){
          alert('10 символдан үлкен')
        }else{
          for (let i = 1; i <= 10 - this.text.length ; i++) {
            value = '*'.repeat(i)
            
          }
          console.log(value)
         alert(this.text + value)
        }
        
        
        
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
