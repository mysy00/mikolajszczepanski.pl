<template>
  <section class="projects__project">
    <div class="project__header">
      <a :href="preview" class="project__header__link">
        <img class="project__header__img" :src="previewThumbnail" alt="">
      </a>
    </div>
    <div class="project__desc">
      <dl class="project__desc__list">
        <dt class="project__desc__list__item-title">{{ nameTitle }}</dt>
        <dd class="project__desc__list__item-desc">{{ name }}</dd>
        <dt class="project__desc__list__item-title"> {{ previewTitle }}</dt>
        <dd class="project__desc__list__item-desc">{{ preview }}</dd>
        <dt class="project__desc__list__item-title">{{ sourceCodeTitle }}</dt>
        <dd class="project__desc__list__item-desc">{{ sourceCode }}</dd>
      </dl>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'Project',
    data: function () {
      return {
        nameTitle: "Name:",
        previewTitle: "Preview:",
        sourceCodeTitle: "Source Code:"
      }
    },
    props: {
      name: String,
      preview: String,
      previewThumbnail: String,
      sourceCode: String
    }
  }
</script>
<style scoped>
  .projects__project {
    display: inline-block;
    background: #fafafaee;
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    color: #060606;
  }
  .projects__project:not(:first-child) {
    margin-left: 1rem;
  }
  .project__header,
  .project__header__img {
    height: 250px;
    width: 350px;
  }

  .project__desc__list {
    display: block;
    flex-wrap: wrap;
    margin: 0;
    padding: .5rem;
  }

  .project__desc__list__item-title {
    font-weight: 700;
  }

  .project__desc__list__item-title,
  .project__desc__list__item-desc {
    display: inline;
    margin: 0;
  }

  .project__desc__list__item-desc:before {
    content: " ";
  }

  .project__desc__list__item-desc:after {
    content: "\A";
    white-space: pre;
  }
</style>