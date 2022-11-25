<template>
    <div class="card-cnt d-flex justify-content-center">
        <div class="crd">
            <img alt="" :src="singleAlbum.poster">
            <div class="title">{{singleAlbum.title}}</div>
            <div class="author">{{singleAlbum.author}}</div>
            <div class="year">{{singleAlbum.year}}</div>
        </div>
    </div>
</template>



<script>
export default {
    name: 'CardComp',
    props: {
        singleAlbum: Object
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.card-cnt {
    width: calc( 100% / 5 - 20px);
    margin-bottom: 20px;
    background-color: rgb(47, 58, 70);
    
    
    .crd {
        font-size: 1.5rem;
        height: 250px;
        text-align: center;
        margin-top: 10px;
        color: white;
        
        
        img {
            aspect-ratio: 1/1;
            width: 60%;
        }

        .title{
          padding-top: 10px;
          line-height: 1.5rem;
          font-weight: bold;
          font-size: 1.5rem;
        }
        .author,.year{

          font-size: 0.6rem;
        }
        
    }
}
</style>








