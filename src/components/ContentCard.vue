<script>

export default {
  components: {
  },
  data() {
    return {
      hover: false
    }
  },
  props: {
    item: Object,
    searchType: String,
  },
  computed: {
    ratingStars() {
      return Math.ceil(this.item.vote_average * 0.5)
    }
  }
}

</script>

<template>

  <div class="w-50 p-2">
    <div class="border w-auto position-relative" @mouseover="hover = true" @mouseleave="hover = false">
      <img :src="`https://image.tmdb.org/t/p/w300/${item.poster_path}`" alt="" class="mw-100">
      <div class="my-overlay position-absolute top-0 start-0 w-100 h-100 bg-dark overflow-y-scroll"
        :class="hover === false ? 'd-none' : ''">
        <ul class="list-group list-group-flush h-100 justify-content-start">
          <li class="list-group-item bg-transparent text-white">Titolo: {{ searchType === 'movie' ? item.title :
            item.name }}</li>
          <li class="list-group-item bg-transparent text-white">Titolo originale: {{ searchType === 'movie' ?
            item.original_title :
            item.original_name
            }}</li>
          <li class="list-group-item bg-transparent text-white">
            <span>Lingua:</span>
            <img :src="`/flags/4x3/${item.original_language.toLowerCase()}.svg`" alt="" class="rectangle-flag">
          </li>
          <li class="list-group-item bg-transparent text-white">
            <span>Voto: </span>
            <i class="fa-solid fa-star color-gold" v-for="n in ratingStars">Stellina</i>
          </li>
          <li class="list-group-item bg-transparent text-white" v-if="item.overview.length">Overview: {{ item.overview
            }}</li>
        </ul>

      </div>
    </div>
  </div>

</template>

<style></style>