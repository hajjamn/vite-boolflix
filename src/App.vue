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
      console.log(`Sto facendo la ricerca di ${store.currentSearch}`)
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
    }
  }
}
</script>

<template>

  <AppHeader @search="searchContent()" />
  <AppContent />

</template>

<style lang="scss">
@use 'bootstrap';
@use './assets/style/general.scss'
</style>
