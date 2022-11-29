<template>
    <div class="nav-bgd">
        <nav class="d-flex justify-content-center me-5 p-4 align-items-center">
            <div class="me-5">
                <label class="me-3" for="">Seleziona per Autore</label>
                <select name="" id="" @click="$emit('emitSceltaHeader', valueOptionSelected )" v-model="valueOptionSelected">
                       <option  
                       :value="element"
                     v-for="(element,index) in arrayAutoriApptoHeader" 
                     :key="index"
                     >{{element}}</option>
                    </select>
            </div>
    
            <div>
                <label class="me-3" for="">Seleziona per Genere</label>
                <select name="" id="" v-model="valueOptionSelected">
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
    name: 'HeaderComp',
    props: {
        arrayGeneriApptoHeader: Array,
        arrayAutoriApptoHeader: Array
    },

    data() {
        return {

            valueOptionSelected: ''
        }
    },
    mounted() {
        //  this.$emit('emitSceltaHeader', this.valueOptionSelected)
    }
}
</script>

<style lang="scss" scoped>

.nav-bgd{

     background-color: rgb(47, 58, 70);

    nav {
    // width: 50%;
    // margin: 0 auto;
    color: white;
    
    img {
        margin: 10px;
        width: 10%;
    }
}

}

</style>