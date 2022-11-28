<template>
    <div>
       <nav class="d-flex justify-content-between">
         <div>
            <img src="../assets/spotify-logo.webp" alt="">
         </div>
         <div>
            <select name="" id="" v-model="valueOptionSelected">
            <option  :value="element"
             v-for="(element,index) in arrayGeneriApptoHeader" 
             :key="index">{{element}}</option>
            </select>
         </div>
       </nav>
    </div>
</template>

<script>
    export default {
        name:'HeaderComp',
        props:{
         arrayGeneriApptoHeader: Array
        },

        data(){
            return{
            
            valueOptionSelected:''
            }
        }
    }
</script>

<style lang="scss" scoped>
nav{
    
   background-color: rgb(47, 58, 70);
    img{
        margin: 10px;
        width: 10%;
    }
}
</style>