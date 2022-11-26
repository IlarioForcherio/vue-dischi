<template>
    <div class="crd-cnt d-flex justify-content-center">
        <div class="crd">
              <img alt="" :src="singleAlbum.poster">
              <div class="title">{{Title}}</div>
              <div class="author">{{singleAlbum.author}}</div>
              <div class="year">{{singleAlbum.year}}</div>   
        </div>
    </div>
</template>



<script>
export default {
    name: 'CardComp',
    props: {
        singleAlbum: Object,
        Title: String
    }
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.crd-cnt{ 
    
     width:calc(100% / 5 - 10px);
     padding:10px 20px;
     
     
    

    .crd{

        padding: 10px ;
        background-color: rgb(47, 58, 70);
        color: white;
        text-align: center;
        
        
        .title{
         
         padding-top:10px;
         line-height: 1.2rem;
         font-size:1rem;   
         font-weight: bold;
        }
        .author,.year{
            color: rgb(125, 118, 112);
            font-size:0.7rem;

        }
        
       
        img{
            
            aspect-ratio: 1/1;
            width: 110px;
            
        }
    }
}



</style>








