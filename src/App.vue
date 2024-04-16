<script>
import axios from 'axios'
import { store } from './store.js'
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'

export default {
  components: {
    AppHeader,
    AppContent,
  },
  data() {
    return {
      store,
    }
  },
  methods: {
    searchContent() {
      axios
        .get('https://api.themoviedb.org/3/search/movie', {
          params: {
            api_key: store.queryKey,
            query: store.currentSearch,
          }
        })
        .then((res) => {
          console.log(res.data)
          store.movieSearchResults = res.data.results
        })

      axios
        .get('https://api.themoviedb.org/3/search/tv', {
          params: {
            api_key: store.queryKey,
            query: store.currentSearch,
          }
        })
        .then((res) => {
          console.log(res.data)
          store.tvSearchResults = res.data.results
        })
    }
  }
}
</script>

<template>
  <i class="fa-solid fa-star"></i>
  <AppHeader @search="searchContent()" />
  <AppContent />

</template>

<style lang="scss">
@use 'bootstrap';
@use './assets/style/general.scss';
/* @use 'font-awesome'; */
</style>
