<template>
  <div id="app">
    <header class="header header-page">
      <label for="expandNavigation" class="header__expand-navigation-label">
        <img src="https://png.icons8.com/ios/24/ffffff/menu.png" alt="Expand Navigation">
      </label>
      <input class="header__expand-navigation-input" id="expandNavigation" type="checkbox">
      <nav class="header__nav">
        <div class="header__nav__main-section">
          <router-link class="header__nav__link" to="/">
            <span>Home</span>
            <img src="https://png.icons8.com/ios/24/ffffff/home.png">
          </router-link>
          <router-link class="header__nav__link" to="/projects">
            <span>Projects</span>
            <img src="https://png.icons8.com/ios/24/ffffff/file.png">
          </router-link>
          <router-link class="header__nav__link" to="/about">
            <span>About</span>
            <img src="https://png.icons8.com/ios/24/ffffff/question-mark.png">
          </router-link>
        </div>
        <div class="header__nav__socialmedia-section">
          <a class="header__nav__link" href="http://facebook.com/divoskyy">
            <span>Facebook</span>
            <img src="https://png.icons8.com/ios/24/ffffff/facebook.png">
          </a>
          <a class="header__nav__link" href="http://github.com/divosky">
            <span>Github</span>
            <img src="https://png.icons8.com/ios/24/ffffff/github.png">
          </a>
          <a class="header__nav__link" href="http://gitlab.com/divosky">
            <span>GitLab</span>
            <img src="https://png.icons8.com/ios/24/ffffff/gitlab.png">
          </a>
          <a class="header__nav__link" href="http://keybase.io/divosky">
            <span>Keybase</span>
            <img src="https://png.icons8.com/ios/24/ffffff/keybase.png">
          </a>
        </div>
      </nav>
    </header>
    <main class="main-page">
      <router-view/>
    </main>
  </div>
</template>

<script>
export default {
  
}
</script>


<style>
html,
body {
  height: 100%;
  margin: 0;
  background: url(assets/bg.jpg);
  background-attachment: fixed;
  background-size: cover;
}

body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fafafa;
}

body:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #00000066;
}

#app {
  position: relative;
  min-height: 100%;
}

.header {
  background: #000;
}

.header__expand-navigation-label {
  display: block;
  text-align: right;
  padding: 4px;
}

.header__expand-navigation-input {
  display: none;
}

.header__expand-navigation-input:checked+.header__nav {
  display: block;
}

.header__nav {
  display: none;
}

.header__nav__link {
  display: flex;
  justify-content: space-between;
  margin-bottom: .3rem;
  padding: .3rem;
  color: #fff;
  text-decoration: none;
  font-size: 1.3rem;
}

.header__nav__socialmedia-section {
  display: flex;
  justify-content: space-around;
}

.header__nav__socialmedia-section>.header__nav__link>span {
  display: none;
}

/*.header__nav__main-section,
.header__nav__socialmedia-section {
  display: flex;*/

/*justify-items: space-around;
}*/

</style>
