<script>

export default {
  data() {
    return {
    }
  },
  props: {
    item: Object,
    searchType: String,
  }
}

</script>

<template>

  <div>
    <ul class="list-group">
      <li class="list-group-item">Titolo: {{ searchType === 'movie' ? item.title : item.name }}</li>
      <li class="list-group-item">Titolo originale: {{ searchType === 'movie' ? item.original_title : item.original_name
        }}</li>
      <li class="list-group-item">
        <span>Lingua:</span>
        <img :src="`/flags/4x3/${item.original_language.toLowerCase()}.svg`" alt="" class="rectangle-flag">
      </li>
      <li class="list-group-item">Voto: {{ item.vote_average }}</li>
    </ul>
  </div>

</template>

<style></style>