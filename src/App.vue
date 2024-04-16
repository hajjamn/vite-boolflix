<script>
import axios from 'axios'
import { store } from './store.js'

export default {
  components: {

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

</template>

<style lang="scss">
@use 'bootstrap';
@use './assets/style/general.scss'
</style>
