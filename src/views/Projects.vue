<template>
    <Project />
</template>

<script>
import Project from '@/components/Project.vue'

export default {
  name: 'projects',
  components: { Project },
  mounted: function() {  
    document.title = localStorage.pageTitle + ' | Projects'  
  }
}
</script>

<style scoped>

</style>

