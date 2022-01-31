<template>
    
    <div class="album">
        <img :src="albums.poster" class="box-img" alt="">
        <p class="text-title">{{albums.title}}</p>
        <p class="text-author">{{albums.author}}</p>
        <p class="text-years">{{albums.year}}</p>
    </div>
        
    
</template>


<script>
export default {
    props: {
        albums: Object
    }
    
}
</script>

<style lang="scss" scoped>

.album {
    width: 150px;
    height: 300px;
    text-align: center;
    background-color: #2E3A46;
    margin: 10px;
    padding: 10px;
    padding-top: 20px;
    .text-title {
        color: #fff;
        font-size: 20px;
        padding-bottom: 10px;
        text-transform:uppercase;
    }
    .text-author {
        color: gray;
        font-size: 15px;
    }
    .text-years {
        color: gray;
        font-size: 12px;
    }
    .box-img {
        width: 120px;
        height: 120px;
        margin-bottom: 10px;
    }
}
</style>