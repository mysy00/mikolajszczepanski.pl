<template>
  <div class="hello">
    <h1>{{ pageHeader }}</h1>
  
    <h3>
      <span class="keypart">6C7F</span>
      <span class="keypart">A1C3</span>
      <span class="keypart">8812</span>
      <span class="keypart">2B02</span>
      <span class="keypart">D279</span>
      <span class="keypart">86AC</span>
      <span class="keypart">27A3</span>
      <span class="keypart">F144</span>
      <span class="keypart">17A7</span>
      <span class="keypart">1234</span>
    </h3>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    pageHeader: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello {
    text-align: center;
  }
  .keypart {
    display: inline-block;
    white-space: nowrap;
  }
  .keypart:not(:first-child) {
    margin-left: .5rem;
  }
</style>
