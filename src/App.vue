<template>
    <div id="app">
        <HeaderComp
        :arrayGeneriApptoHeader="arrayGeneri"
        :arrayAutoriApptoHeader="arrayAutori"
        />
        <MainComp
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
         arrayGeneri:[],
         arrayAutori:[]
        }
    },
    mounted() {

    },
    methods: {
     listaGeneri(arrayGeneriMaintoApp){
     this.arrayGeneri = arrayGeneriMaintoApp
     },
     listaAutori(arrayAutoriMaintoHeader){
     this.arrayAutori = arrayAutoriMaintoHeader
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
