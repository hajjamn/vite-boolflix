<script>
import ContentCard from './ContentCard.vue'
import { store } from '../store.js'

export default {
  components: {
    ContentCard
  },
  data() {
    return {
      store,
    }
  }
}

</script>

<template>

  <main class="bg-secondary">
    <div class="container">
      <div class="row">
        <div class="col-6">
          <h2 class="text-center">Film</h2>
          <div class="row">
            <ContentCard v-for="movie in store.movieSearchResults" :item="movie" :searchType="'movie'" :key="movie.id">
            </ContentCard>
          </div>
        </div>

        <div class="col-6">
          <h2 class="text-center">TV</h2>
          <ContentCard v-for="tv in store.tvSearchResults" :item="tv" :searchType="'tv'" :key="tv.id"></ContentCard>
        </div>
      </div>
    </div>

  </main>


</template>

<style></style>