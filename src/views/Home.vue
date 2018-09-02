<template>
  <section class="home">
    <HelloWorld pageHeader="Mikołaj Szczepański"/>
  </section>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  mounted: function () {
    document.title = localStorage.pageTitle
  }
}
</script>

<style scoped>

</style>
