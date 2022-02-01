<template>
    <header>
        
        <div class="container">
            <div class="containar-album">
                <album-box v-for="(album, index) in albums" 
                :key=(index)
                :album="album" />
            </div>
        </div>
        
    </header>
</template>


<script>
import AlbumBox from './AlbumBox.vue'

export default {
    components: {
        AlbumBox,
    },
    props: {
        albums: Array
    },
    
}
</script>

<style lang="scss" scoped>
    header {
    background-color: #1E2D3B;
        
        .container {
            width: 1200px;
            margin: 0 auto;
            
            .containar-album {
                margin: 0 auto;
                width: 1000px;
                padding-top: 50px;
                padding-bottom: 50px;
                margin: 0 auto;
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                
            }
            }


    }
</style>