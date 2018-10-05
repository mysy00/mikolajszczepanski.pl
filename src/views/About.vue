<template>
  <section class="about">
    <section class="box">
      <h3 class="box__title">Main Skills</h3>
      <div class="box__content">
        <ul class="box__content__list">
          <li class="box__content__list__item">
            <strong>HTML5</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="3"/></li>
          <li class="box__content__list__item">
            <strong>CSS3</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="3"/></li>
          <li class="box__content__list__item">
            <strong>SCSS</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="3"/></li>
          <li class="box__content__list__item">
            <strong>Bootstrap</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="3"/></li>
          <li class="box__content__list__item">
            <strong>Bulma</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="2"/><Star iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="1"/></li>
          <li class="box__content__list__item">
            <strong>JavaScript</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="2"/><Star iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="1"/></li>
          <li class="box__content__list__item">
            <strong>VueJS</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="1"/><Star iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="2"/></li>
          <li class="box__content__list__item">
            <strong>GIT</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="1"/><Star iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="2"/></li>
          <li class="box__content__list__item">
            <strong>Linux</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="2"/><Star iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="1"/></li>
          <li class="box__content__list__item">
            <strong>Windows</strong> — <StarFilled iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="2"/><Star iconColor="var(--star-color)" iconWidth="20" iconHeight="20" :amount="1"/></li>
        </ul>
      </div>
    </section>

    <section class="box">
      <h3 class="box__title">Certificates</h3>
      <div class="box__content">
        <ul class="box__content__list">
          <li class="box__content__list__item">
            <i>2018-05</i> — Certificate of Competence, an IT Technician</li>
          <li class="box__content__list__item">
            <i>2018-04</i> — NDG Linux Essentials course in the Cisco Networking Academy</li>
          <li class="box__content__list__item">
            <i>2017-12</i> — IT Essentials in the Cisco Networking Academy</li>
        </ul>
      </div>
    </section>

    <section class="box">
      <h3 class="box__title">Additional</h3>
      <div class="box__content">
        <ul class="box__content__list">
          <li class="box__content__list__item">
            <strong>Languages</strong> — Polish (native), English (intermediate)</li>
          <li class="box__content__list__item">
            <strong>Interests</strong> — Technology; coding specific elements for games, including (but not limited to): websites,
            scripts for servers; watching tv series and playing games</li>
          <li class="box__content__list__item">
            <strong>Driving License</strong> — B Category</li>
        </ul>
      </div>
    </section>

    <section class="box">
      <h3 class="box__title">Employment History</h3>
      <div class="box__content">
        <ul class="box__content__list">
          <li class="box__content__list__item">
            <i>2018-05 to 2018-06</i> — Informix - IT Service</li>
        </ul>
      </div>
    </section>
  </section>
</template>

<script>
import Star from '@/components/icons/Star'
import StarFilled from '@/components/icons/StarFilled'

export default {
  name: 'about',
  mounted: function() {  
    document.title = localStorage.pageTitle + ' | About Me'
  },
  components: {
    Star,
    StarFilled
  }
}
</script>

<style scoped>
:root {
  --star-color: black;
}

.box {
  box-sizing: border-box;
  padding: .1rem 1rem;
  margin-bottom: 1rem;
  color: #060606;
  background: #fafafaee;
  box-shadow: var(--box-shadow);
}

.box__content__list {
  padding-left: .5rem;
  list-style: none;
}

.box__content__list__item {
  margin-bottom: .3rem;
}

@supports (display: grid) {
  .about {
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(auto-fit, minmax(195px, 1fr));
    grid-auto-rows: auto;
    justify-self: center;
  }
  .box {
    grid-column-end: span 2;
    grid-row-end: span 2;
  }
  @media (min-width: 480px) {
    .about {
      width: 90%;
      margin: 0 auto;
      grid-auto-rows: minmax(120px, auto);
    }
    .box:nth-child(even) {
      grid-row-end: span 1;
    }
  }
}
</style>