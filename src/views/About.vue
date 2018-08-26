<template>
  <section class="about">
    <section class="box">
      <h3 class="box__title">Skills</h3>
      <div class="box__content">
        <ul class="box__content__list">
          <li class="box__content__list__item">
            <strong>HTML5</strong> — Intermediate</li>
          <li class="box__content__list__item">
            <strong>CSS3</strong> — Intermediate</li>
          <li class="box__content__list__item">
            <strong>SCSS</strong> — Intermediate</li>
          <li class="box__content__list__item">
            <strong>Bootstrap</strong> — Intermediate</li>
          <li class="box__content__list__item">
            <strong>Bulma</strong> — Beginner</li>
          <li class="box__content__list__item">
            <strong>JavaScript</strong> — Beginner</li>
          <li class="box__content__list__item">
            <strong>VueJS</strong> — Beginner</li>
          <li class="box__content__list__item">
            <strong>GIT</strong> — Beginner</li>
          <li class="box__content__list__item">
            <strong>Linus</strong> — Intermediate - daily user</li>
          <li class="box__content__list__item">
            <strong>Windows</strong> — Intermediate</li>
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
            <strong>Languages</strong> — Polish (native), English (written: intermediate; spoken: beginner)</li>
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

<style scoped>
.box {
  margin-bottom: 1rem;
  padding: .1rem 1rem;
  background: #fafafaee;
  box-shadow: 0 10px 20px rgba(0, 0, 0, .19), 0 6px 6px rgba(0, 0, 0, .23);
  color: #060606;
  box-sizing: border-box;
}
.box__content__list {
  list-style: none;
  padding-left: .5rem;
}
.box__content__list__item {
  margin-bottom: .3rem;
}
@supports (display: grid) {
  .about {
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(auto-fit, minmax(145px,1fr));
    grid-auto-rows: auto;
    justify-self: center;
  }
  .box {
    grid-column-end: span 2;
    grid-row-end: span 2;
  }
  @media (min-width: 480px) {
    .about {
      grid-template-columns: repeat(auto-fit, minmax(145px,1fr));
      grid-auto-rows: minmax(120px, auto);
      width: 90%;
      margin: 0 auto;
    }
    .box:nth-child(even) {
      grid-row-end: span 1;
    }
  }
}
</style>