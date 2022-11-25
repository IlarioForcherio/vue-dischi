<template>
  <div id="app">
    <img alt="" src="">
    <CardComp msg=""/>
    
  </div>
</template>

<script>
import CardComp from './components/CardComp.vue'
// // import axios from' axios'

export default {
    name: 'App',
    components: {
      CardComp
    },
    data() {
      return {
        dataPersonaggi: ''
      }
    },
    mounted() {
      // const self = this;
      // console.log('ciao')
      // axios.get('https://api.sampleapis.com/rickandmorty/characters')
      //     .then( (response)=>{
      //       console.log(response.data)
      //     } )
      // this.getPersonaggi();
    },
    // methods: {
    //   getPersonaggi() {
    //     axios.get('https://api.sampleapis.com/rickandmorty/characters')
    //       .then((response) => {
    //         // //this.dataPersonaggi => recupero l'informazione all'interno di "data"
    //         // //response.data => Abbiamo recuperato l'array di 26 elementi presenti all'interno della response della chiamata GET all'API
    //         // this.dataPersonaggi = response.data
    //       })
    //   }
    // }
  }
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
