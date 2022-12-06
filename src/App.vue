<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">-->
  <div class = "header">
  <MyHeader headername="networks"/>
  </div>
  <Network_Box :networks="networks" />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import Network_Box from './components/Network_Box.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    Network_Box
  },
  data(){
    return {
      networks: []
    }
  },
   methods: {

    // promises

      async fetchnetworks(){
          //const res = await fetch('http://localhost:8585/networks/')
          const res = await fetch("https://swetha-heroku.herokuapp.com/api")
          const data = await res.json()
          console.log(data)
          return data.networks
      }


  },
  async created(){
    this.networks = await this.fetchnetworks()
    //console.log(this.networks)
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
.header{
  height: 0em;
}
</style>
