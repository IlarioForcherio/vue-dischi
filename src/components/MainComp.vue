<template>
    <div class="main-cnt">
        <div class="main d-flex flex-wrap ">
            <CardComp
             v-for="(album ,index) in arrayAlbum" 
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
            arrayGeneri:[]
        }
    },
    mounted() {

        this.getAlbums();
    },
    methods: {
        getAlbums() {
            axios.get("https://flynn.boolean.careers/exercises/api/array/music")
                .then((resp) => {
                    //console.log(resp.data.response)
                    //oarray di oggetti albums 
                    this.arrayAlbum = resp.data.response;
                    //estraggo solo il genere
                    this.arrayAlbum.forEach((singoloAlbum)=>{

                        if(this.arrayGeneri.includes(singoloAlbum.genre)){

                        }

                        this.arrayGeneri.push(singoloAlbum.genre)
                       
                    })
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