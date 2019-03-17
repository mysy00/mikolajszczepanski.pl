<template>
  <section class="projects">
    <section class="projects__project" v-for="project in projects" :key="project.fullSize">
      <div class="project__header">
        <a :href="project.fullSize" class="project__header__link">
          <div class="project__header__img" :style="'background: url(' + project.thumbnail + '); background-size: cover;'"></div>
        </a>
      </div>
      <div class="project__desc">
        <dl class="project__desc__list">
          <dt class="project__desc__list__item-title">{{ nameTitle }}</dt>
          <dd class="project__desc__list__item-desc">{{ project.name }}</dd>

          <dt class="project__desc__list__item-title" v-if="project.fullSize"> {{ previewImage }}</dt>
          <dd class="project__desc__list__item-desc" v-if="project.fullSize">
            <a :href="project.fullSize">Click Here</a>
          </dd>

          <dt class="project__desc__list__item-title" v-if="project.previewLive"> {{ previewLive }}</dt>
          <dd class="project__desc__list__item-desc" v-if="project.previewLive">
            <a :href="project.previewLive">Click Here</a>
          </dd>
          
          <dt class="project__desc__list__item-title" v-if="project.sourceCode">{{ sourceCodeTitle }}</dt>
          <dd class="project__desc__list__item-desc" v-if="project.sourceCode">
            <a :href="project.sourceCode">Click Here</a>
          </dd>
        </dl>
      </div>
    </section>
  </section>
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
          name: 'Old portfolio, the point was to make it look and behave like a real DE',
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
        },
        {
          name: 'Mybb theme written basically from scratch for a SA:MP Gang. Theme based on bootstrap 4',
          previewLive: 'https://immfamily.pl',
          sourceCode: '',
          thumbnail: './img/projects/small-9.jpg',
          fullSize: './img/projects/9.png'
        },
        {
          name: 'Front-end for a SA:MP server',
          previewLive: 'https://divosky.github.io/dayz-help/',
          sourceCode: 'https://github.com/divosky/dayz-help/',
          thumbnail: './img/projects/small-10.png',
          fullSize: './img/projects/10.png'
        },
        {
          name: 'Personal multilangual webpage',
          previewLive: 'https://nowitam.pl/',
          sourceCode: 'https://github.com/divosky/nowitam.pl/',
          thumbnail: './img/projects/small-11.png',
          fullSize: './img/projects/11.png'
        },
        {
          name: 'Find information about a country',
          previewLive: '',
          sourceCode: 'https://github.com/Divosky/country-info',
          thumbnail: './img/projects/small-12.png',
          fullSize: './img/projects/12.png'
        }
      ]
      }
    }
  }
</script>

<style scoped>
.projects {
  overflow: hidden;
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
  box-sizing: border-box;
  margin-bottom: 1rem;
  color: #060606;
  background: #fafafaee;
  box-shadow: var(--box-shadow);
}

.project__header,
.project__header__img {
  width: 100%;
  height: auto;
  max-height: 300px;
}

.project__desc__list {
  display: block;
  padding: .5rem;
  margin: 0;
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
  white-space: pre;
  content: "\A";
}

@media (min-width: 480px) {
  .projects {
    display: flex;
    box-sizing: border-box;
    width: 90%;
    padding: 1rem 0;
    margin: 0 auto;
    overflow-x: scroll;
  }
  .projects__project {
    display: inline-block;
  }
  .projects__project:not(:first-child) {
    margin-left: 1rem;
  }
  .project__header,
  .project__header__img {
    width: 352px;
    height: 198px;
  }
}
</style>