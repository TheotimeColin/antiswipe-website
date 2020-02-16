<template>
  <div id="app">
      <homepage class="Homepage" />
  </div>
</template>

<script>
import homepage from './pages/homepage.vue'

export default {
  name: 'app',
  components: { homepage }
}
</script>

<style lang="scss">
    @import "@/assets/scss/index.scss";
</style>