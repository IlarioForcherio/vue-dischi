<template>
    <div class="main-cnt">
        <div class="main d-flex flex-wrap ">
            <CardComp v-for="(album ,index) in arrayAlbum" 
             :key="index"
             :Title="album.title.toUpperCase()"
             :singleAlbum="album"
               />
        </div>
    </div>
</template>



<script>
import CardComp from '../components/CardComp.vue'
import axios from 'axios'

export default {
    name: 'MainComp',
    components: {

        CardComp

    },
    data() {
        return {
            arrayAlbum: [],
        }
    },
    mounted() {

        this.getPersonaggi();
    },
    methods: {
        getPersonaggi() {
            axios.get("https://flynn.boolean.careers/exercises/api/array/music")
                .then((resp) => {
                    //console.log(resp.data.response)
                    this.arrayAlbum = resp.data.response;
                })
        }
    }

}
</script>

<style lang="scss" scoped>


.main-cnt{
   background-color: rgb(30, 45, 59);
}
.main{
    
    width: 60%;
    margin:0px auto;
    padding: 90px 0;
    
}

</style>