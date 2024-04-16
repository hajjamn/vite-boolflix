<script>

export default {
  data() {
    return {
    }
  },
  props: {
    item: Object,
  }
}

</script>

<template>

  <div>
    <ul class="list-group">
      <li class="list-group-item">Titolo: {{ item.title }}</li>
      <li class="list-group-item">Titolo originale: {{ item.original_title }}</li>
      <li class="list-group-item">Lingua: {{ item.original_language }}</li>
      <li class="list-group-item">Voto: {{ item.vote_average }}</li>
    </ul>
  </div>

</template>

<style></style>