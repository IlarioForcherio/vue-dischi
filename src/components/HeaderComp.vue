<template>
    <div>
       <nav class="d-flex justify-content-between">
         <div>
            <img src="../assets/spotify-logo.webp" alt="">
         </div>
         <div></div>
       </nav>
    </div>
</template>

<script>
    export default {
        name:'HeaderComp'
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