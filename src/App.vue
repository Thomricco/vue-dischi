<template>
  <div id="app">
    <main-container :album="album" />
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'


export default {
  name: 'App',
  components: {
    MainContainer,

  },
  data () {
    return {
      album: []
    }
  },
  mounted () {
    axios.get ('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.album = response.data.response
    })
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
@import './style/main.scss';

</style>
