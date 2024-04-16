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
      <li class="list-group-item">Titolo originale: {{ searchType === 'movie' ? item.origina_title : item.original_name
        }}</li>
      <li class="list-group-item">Lingua: {{ item.original_language }}</li>
      <li class="list-group-item">Voto: {{ item.vote_average }}</li>
    </ul>
  </div>

</template>

<style></style>