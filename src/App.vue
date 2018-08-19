<template>
  <div id="app">
    <header class="header header-page">
      <nav class="header__nav">
        <router-link class="header__nav__link" to="/">
          Home
          <img src="https://png.icons8.com/ios/24/ffffff/home.png">
        </router-link>
        <router-link class="header__nav__link" to="/projects">
          Projects
          <img src="https://png.icons8.com/ios/24/ffffff/file.png">
        </router-link>
        <router-link class="header__nav__link" to="/about">
          About
          <img src="https://png.icons8.com/ios/24/ffffff/question-mark.png">
        </router-link>
      </nav>
      <div class="header__social-media">
        <a class="header__social-media__link" href="http://facebook.com/divoskyy">
          Facebook
          <img src="https://png.icons8.com/ios/24/ffffff/facebook.png">
        </a>
        <a class="header__social-media__link" href="http://github.com/divosky">
          Github
          <img src="https://png.icons8.com/ios/24/ffffff/github.png">
        </a>
        <a class="header__social-media__link" href="http://gitlab.com/divosky">
          GitLab
          <img src="https://png.icons8.com/ios/24/ffffff/gitlab.png">
        </a>
        <a class="header__social-media__link" href="http://keybase.io/divosky">
          Keybase
          <img src="https://png.icons8.com/ios/24/ffffff/keybase.png">
        </a>
      </div>
    </header>
    <main class="main-page">
      <router-view/>
    </main>
  </div>
</template>

<style>
html,
body {
  height: 100%;
  margin: 0;
  background: url(assets/bg.jpg);
  background-size: cover;
}
body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fafafa;
}
body:before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 100%;
  height: 100%;
  background: #00000066;
}
#app {
  position: relative;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: 2fr;
  min-height: 100%;
}
.header-page {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  grid-column: 1;
  grid-row: 1 / span 2;
  background: black;
  width: 133px;
  left: -100px;
  transition: 1s ease-in-out;
}
.header-page:hover {
  left: 0;
  transition: .13s ease-in-out;
}
.header__nav,
.header__social-media {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
}
.header__nav__link,
.header__social-media__link {
  display: flex;
  justify-content: space-between;
  color: #fafafa;
  text-decoration: none;
  margin-top: 1rem;
  padding: .3rem;
  font-size: 1.3rem;
}
.main-page {
  grid-column: 1 / span 12;
  grid-row: 1;
  justify-self: center;
  align-self: center;
}
</style>
