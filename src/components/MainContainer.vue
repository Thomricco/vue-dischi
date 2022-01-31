<template>
    <header>
        <div class="nav">
            <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Spotify_App_Logo.svg/2048px-Spotify_App_Logo.svg.png" alt="">
        </div>
        <div class="container">
            <div class="containar-album">
                <album-box v-for="(albums, index) in album" 
                :key=(index)
                :albums="albums" />
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
        album: Array
    }
    
}
</script>

<style lang="scss" scoped>
    header {
    background-color: #1E2D3B;
        .nav {
                height: 50px;
                background-color: black;
                .logo {
                    width: 50px;
                }
            }
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