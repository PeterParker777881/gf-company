<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/app/Header.vue'
export default {
  components: { Header }
}
</script>

<style lang="scss">
.container {
  max-width: 1342px;
  padding: 0 15px;
  margin: 0 auto;
}
</style>
