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

  <div class="my-card-wrapper py-3">
    <div class="border position-relative" @mouseover="hover = true" @mouseleave="hover = false">
      <img :src="`https://image.tmdb.org/t/p/w300/${item.poster_path}`" alt="" class="w-100"
        v-if="item.poster_path !== null">
      <img src="https://cdn.ttgtmedia.com/rms/onlineimages/404_error-h_half_column_mobile.png" alt="" v-else>
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
            <span>Lingua: </span>
            <img :src="`/flags/4x3/${item.original_language.toLowerCase()}.svg`" alt="" class="rectangle-flag">
          </li>
          <li class="list-group-item bg-transparent text-white">
            <span>Voto: </span>
            <font-awesome-icon icon="fa-solid fa-star color-gold" v-for="n in ratingStars" />
            <font-awesome-icon icon="fa-regular fa-star" v-for="n in (5 - ratingStars)" />
          </li>
          <li class="list-group-item bg-transparent text-white" v-if="item.overview.length">Overview: {{ item.overview
            }}</li>
        </ul>

      </div>
    </div>
  </div>

</template>

<style></style>