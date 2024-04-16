<script>

export default {
  data() {
    return {
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

  <div class="m-auto">
    <div class="border w-auto">
      <img :src="`https://image.tmdb.org/t/p/w500/${item.poster_path}`" alt="" class="w-50">
    </div>
    <ul class="list-group d-none">
      <li class="list-group-item">Titolo: {{ searchType === 'movie' ? item.title : item.name }}</li>
      <li class="list-group-item">Titolo originale: {{ searchType === 'movie' ? item.original_title : item.original_name
        }}</li>
      <li class="list-group-item">
        <span>Lingua:</span>
        <img :src="`/flags/4x3/${item.original_language.toLowerCase()}.svg`" alt="" class="rectangle-flag">
      </li>
      <li class="list-group-item">
        <span>Voto: </span>
        <i class="fa-solid fa-star" v-for="n in ratingStars">Stellina</i>
      </li>
    </ul>
  </div>

</template>

<style></style>