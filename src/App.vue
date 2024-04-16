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
  }
}
</script>

<template>

  <div class="text-center">
    {{ store.moviedbKey }}
  </div>
  <AppHeader />
  <AppContent />

</template>

<style lang="scss">
@use 'bootstrap';
@use './assets/style/general.scss'
</style>
