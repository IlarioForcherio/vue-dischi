<template>
    <div>
       <nav class="d-flex justify-content-between align-items-center">
         <div>
            <img src="../assets/spotify-logo.webp" alt="">
         </div>
            <div>
            <label for="">Seleziona per Autore</label>
            <select name="" id=""  
            @click="$emit('emitSceltaHeader', valueOptionSelected )"
             v-model="valueOptionSelected">
            <option  
            :value="element"
             v-for="(element,index) in arrayAutoriApptoHeader" 
             :key="index"
             >{{element}}</option>
            </select>
         </div>
         <div>
            <label for="">Seleziona per Genere</label>
            <select name="" id=""  v-model="valueOptionSelected">
            <option  
            :value="element"
             v-for="(element,index) in arrayGeneriApptoHeader" 
             :key="index"
             >{{element}}</option>
            </select>
         </div>
       </nav>
    </div>
</template>

<script>
    export default {
        name:'HeaderComp',
        props:{
         arrayGeneriApptoHeader: Array,
         arrayAutoriApptoHeader: Array
        },

        data(){
            return{
            
            valueOptionSelected:''
            }
        },
        mounted(){
            //  this.$emit('emitSceltaHeader', this.valueOptionSelected)
        }
    }
</script>

<style lang="scss" scoped>
nav{
    color:white;
   background-color: rgb(47, 58, 70);
    img{
        margin: 10px;
        width: 10%;
    }
}
</style>