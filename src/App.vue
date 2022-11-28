<template>
    <div id="app">
        <HeaderComp/>
        <MainComp @emitGeneri="listaGeneri" />
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
         arrayGeneri:[]
        }
    },
    mounted() {

    },
    methods: {
     listaGeneri(arrayGeneriMain){
     this.arrayGeneri = arrayGeneriMain
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
