<template>
  <div class="projects">
    <section class="projects__project" v-for="project in projects" :key="project.fullSize">
      <div class="project__header">
        <a :href="project.fullSize" class="project__header__link">
          <img class="project__header__img" :src="project.thumbnail" alt="">
        </a>
      </div>
      <div class="project__desc">
        <dl class="project__desc__list">
          <dt class="project__desc__list__item-title">{{ nameTitle }}</dt>
          <dd class="project__desc__list__item-desc">{{ project.name }}</dd>
          <dt class="project__desc__list__item-title" v-if="project.fullSize"> {{ previewImage }}</dt>
          <dd class="project__desc__list__item-desc" v-if="project.fullSize"><a :href="project.fullSize">Click Here</a></dd>
          <dt class="project__desc__list__item-title" v-if="project.previewLive"> {{ previewLive }}</dt>
          <dd class="project__desc__list__item-desc" v-if="project.previewLive"><a :href="project.previewLive">Click Here</a></dd>
          <dt class="project__desc__list__item-title" v-if="project.sourceCode">{{ sourceCodeTitle }}</dt>
          <dd class="project__desc__list__item-desc" v-if="project.sourceCode"><a :href="project.sourceCode">Click Here</a></dd>
        </dl>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    name: 'Project',
    data: function () {
      return {
        nameTitle: "Name:",
        previewImage: 'Full Size:',
        previewLive: 'Live Preview:',
        sourceCodeTitle: 'Source Code:',
        projects: [{
          name: 'Old portfolio, the point was to made it look like a real DE',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-1.png',
          fullSize: './img/projects/1.png'
        },
        {
          name: 'One of first portfolios',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-2.png',
          fullSize: './img/projects/2.png'
        },
        {
          name: 'Multilangual website for a SA:MP Server, the goal was to help new players',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-3.png',
          fullSize: './img/projects/3.png'
        },
        {
          name: 'Signature & Userbar generator for a SA:MP Server',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-4.png',
          fullSize: './img/projects/4.png'
        },
        {
          name: 'A tiny school project to get a better mark',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-5.png',
          fullSize: './img/projects/5.png'
        },
        {
          name: 'One of first portfolios',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-6.png',
          fullSize: './img/projects/6.png'
        },
        {
          name: 'Mybb theme written basically from scratch, based on bootstrap 4',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-7.png',
          fullSize: './img/projects/7.png'
        },
        {
          name: 'Mybb theme written basically from scratch for a SA:MP EXM Community, based on bootstrap 4',
          previewLive: '',
          sourceCode: '',
          thumbnail: './img/projects/small-8.png',
          fullSize: './img/projects/8.png'
        }
      ]
      }
    }
  }
</script>

<style scoped>
.projects {
  -webkit-overflow-scrolling: touch;
}

.projects__project {
  margin-bottom: 1rem;
  background: #fafafaee;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
  color: #060606;
}

.project__header,
.project__header__img {
  width: 100%;
  height: auto;
  max-height: 300px;
}

.project__desc__list {
  display: block;
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
/*  .projects {
    position: relative;
    display: flex;
    overflow-x: scroll;
    margin: 0 auto;
    padding: 1rem 0;
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

  .projects__project {
    display: inline-block;
    background: #fafafaee;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
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
@media (max-width: 480px) {
  .projects {
    flex-direction: column;
  }
  .projects__project:not(:first-child) {
    margin-left: 0;
  }
  .projects__project {
    margin-bottom: 1rem;
  }
}
*/
</style>