<template>
  <div class="icon icon-star">
    <svg v-for="(star, index) in amount" :key="index" version="1.1" xmlns="http://www.w3.org/2000/svg" :width="iconWidth" :height="iconHeight" viewBox="0 0 24 24">
      <title>Star Filled</title>
      <path :fill="iconColor" d="M23 9c-0.1-0.4-0.4-0.6-0.8-0.7l-6.4-0.9-2.9-5.8c-0.3-0.7-1.5-0.7-1.8 0l-2.9 5.7-6.3 1c-0.4 0-0.7 0.3-0.9 0.7-0.1 0.4 0 0.8 0.3 1l4.6 4.5-1.1 6.4c-0.1 0.4 0.1 0.8 0.4 1s0.7 0.3 1.1 0.1l5.7-3 5.7 3c0.2 0 0.3 0 0.5 0s0.4-0.1 0.6-0.2c0.3-0.2 0.5-0.6 0.4-1l-1.1-6.4 4.6-4.5c0.3-0.2 0.4-0.6 0.3-0.9zM16.3 13.4c-0.2 0.3-0.3 0.6-0.3 0.9l0.8 4.9-4.4-2.3c-0.3-0.2-0.6-0.2-0.9 0l-4.4 2.3 0.9-4.9c0-0.3-0.1-0.6-0.3-0.9l-3.6-3.4 4.9-0.7c0.3 0 0.6-0.3 0.8-0.5l2.2-4.5 2.2 4.4c0.1 0.3 0.4 0.5 0.8 0.5l4.9 0.7-3.6 3.5z"></path>
      <path :fill="iconColor" d="M16.4,13.5c-0.2,0.3-0.3,0.6-0.3,1l0.8,5.2l-4.6-2.4c-0.3-0.2-0.6-0.2-0.9,0l-4.6,2.4l0.9-5.2c0-0.3-0.1-0.6-0.3-1L3.6,9.8
	l5.2-0.7c0.3,0,0.6-0.3,0.8-0.5l2.3-4.8l2.3,4.7C14.3,8.8,14.6,9,15,9l5.2,0.7C20.2,9.7,16.4,13.5,16.4,13.5z"></path>
    </svg>
  </div>
</template>

<script>
export default {
  props: [
    'iconColor',
    'iconWidth',
    'iconHeight',
    'amount'
  ]
}
</script>

<style scoped>
  .icon {
    display: inline-block;
  }
</style>