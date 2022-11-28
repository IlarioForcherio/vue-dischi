<template>
    <div id="app">
        <HeaderComp
        @emitSceltaHeader="sceltaUtente"
        :arrayGeneriApptoHeader="arrayGeneriApp"
        :arrayAutoriApptoHeader="arrayAutoriApp"
        />
        <MainComp
        :selezioneApptoMain="opzioneSelezionata"
        @emitAutoriMain="listaAutori" 
        @emitGeneriMain="listaGeneri" />
        <FooterComp />
    </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'
import FooterComp from './components/FooterComp.vue'
// import axios from   'axios'
export default {
    name: 'App',
    components: {
        HeaderComp,
        MainComp,
        FooterComp,
    },
    data() {
        return{
         arrayGeneriApp:[],
         arrayAutoriApp:[],
         opzioneSelezionata:""
        }
    },
    mounted() {

    },
    methods: {
     listaGeneri(arrayGeneriMaintoApp){
     this.arrayGeneriApp = arrayGeneriMaintoApp
     },

     listaAutori(arrayAutoriMaintoHeader){
     this.arrayAutoriApp = arrayAutoriMaintoHeader
     },

     sceltaUtente(sceltaHeadertoApp){
      this.opzioneSelezionata = sceltaHeadertoApp
     }


    }
}
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    
}
</style>
