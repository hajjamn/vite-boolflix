<script>
import axios from 'axios'

export default {
  components: {

  },
  data() {
    return {
      moviedbKey: '67894cbb91f10ee86602f7bd6b1f20c9',
    }
  }
}
</script>

<template>

  <div class="text-center">
    {{ moviedbKey }}
  </div>

</template>

<style lang="scss">
@use 'bootstrap';
</style>
