<template>
  <div id="app">
    <filtra-genere @filtra="filterResult"/>
    <main-container :albums="albumFiltrati"/>
                             <!--albums-->
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'
import FiltraGenere from './components/FiltraGenere.vue'
import axios from 'axios'


export default {
  name: 'App',
  components: {
    MainContainer,
    FiltraGenere,

  },
  data () {
    return {
      albums: [],
      albumFiltrati: [],
    }
  },
  mounted () {
    axios.get ('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.albums = response.data.response
      this.albumFiltrati = response.data.response
    })
  },
  methods: {
    filterResult(keyword) {
      console.log("casino", keyword);
      this.albumFiltrati = this.albums.filter((album) => {
        return album.genre.toLowerCase().includes(keyword.toLowerCase())
      })
    }

  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
@import './style/main.scss';

</style>
