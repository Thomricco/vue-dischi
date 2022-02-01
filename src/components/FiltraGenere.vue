<template>
    
   <div class="navbar">
       <div class="nav">
            <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Spotify_App_Logo.svg/2048px-Spotify_App_Logo.svg.png" alt="">
        </div>
        <select class="selettore" v-model="selected" @change="$emit('filtra', selected)">
            <option disabled value="">Scegli iltuo genere</option>
            <option>Rock</option>
            <option>Pop</option>
            <option>Jazz</option>
            <option>Metal</option>
            <option value="">Tutti</option>
        </select>
        
   </div>
</template>

<script>
export default {
    data() {
        return {
            selected: ''
        }
    }
}
</script>

<style lang="scss" scoped>

.navbar {
    display: flex;
    background-color: black;
    align-items: center;
    .nav {
    display: flex;
    align-items: center;
    height: 50px;
    background-color: black;
        .logo {
            width: 40px;
        }
    }
    .selettore {
        height: 30px;
        background-color: black;
        color: #fff;
        
    }
}

</style>