<template>
  <div id="app">
      <Homepage class="Homepage" />
  </div>
</template>

<script>
import Homepage from './pages/Homepage.vue'

export default {
  name: 'app',
  components: { Homepage }
}
</script>

<style lang="scss">
    @import "@/assets/scss/index.scss";
</style>