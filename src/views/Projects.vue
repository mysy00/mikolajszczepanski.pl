<template>
  <section class="projects" id="projects">
    <Project 
      name="Nazwa"
      preview="Podgląd"
      previewThumbnail="//placehold.it/250x350"
      sourceCode="kod źródłowy"
    />
    <Project 
      name="Nazwa"
      preview="Podgląd"
      previewThumbnail="//placehold.it/250x350"
      sourceCode="kod źródłowy"
    />
    <Project 
      name="Nazwa"
      preview="Podgląd"
      previewThumbnail="//placehold.it/250x350"
      sourceCode="kod źródłowy"
    />
  </section>
</template>

<script>
import Project from '@/components/Project.vue'

export default {
  name: 'projects',
  components: { Project }
}
</script>

<style scoped>
.projects {
  position: relative;
  display: flex;
  overflow-x: scroll;
  width: 90%;
  margin: 0 auto;
  padding: 1rem;
  box-sizing: border-box;
  -webkit-overflow-scrolling: touch;
}
.projects::-webkit-scrollbar {
  height: 2vh;
}

.projects::-webkit-scrollbar-track {
  background: rgba(0, 0, 0, .2);
  border-radius: 50px;
}

.projects::-webkit-scrollbar-thumb {
  background: rgba(0, 0, 0, .5);
  border-radius: 50px;
}
</style>

