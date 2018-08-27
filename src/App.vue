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
            <span class="header__nav__link__title">Home</span>
            <img src="https://png.icons8.com/ios/24/ffffff/home.png">
          </router-link>
          <router-link class="header__nav__link" to="/projects">
            <span class="header__nav__link__title">Projects</span>
            <img src="https://png.icons8.com/ios/24/ffffff/file.png">
          </router-link>
          <router-link class="header__nav__link" to="/about">
            <span class="header__nav__link__title">About</span>
            <img src="https://png.icons8.com/ios/24/ffffff/question-mark.png">
          </router-link>
        </div>
        <div class="header__nav__socialmedia-section">
          <a class="header__nav__link" href="http://facebook.com/divoskyy">
            <span class="header__nav__link__title">Facebook</span>
            <img src="https://png.icons8.com/ios/24/ffffff/facebook.png">
          </a>
          <a class="header__nav__link" href="http://github.com/divosky">
            <span class="header__nav__link__title">Github</span>
            <img src="https://png.icons8.com/ios/24/ffffff/github.png">
          </a>
          <a class="header__nav__link" href="http://gitlab.com/divosky">
            <span class="header__nav__link__title">GitLab</span>
            <img src="https://png.icons8.com/ios/24/ffffff/gitlab.png">
          </a>
          <a class="header__nav__link" href="http://keybase.io/divosky">
            <span class="header__nav__link__title">Keybase</span>
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
:root {
 --primary-color: #1082E8;
 --box-shadow: 0 10px 20px rgba(0, 0, 0, .19), 0 6px 6px rgba(0, 0, 0, .23); 
}
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
  color: #fafafa;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body:before {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
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
  padding: 4px;
  text-align: right;
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
  padding: .3rem;
  margin-bottom: .3rem;
  font-size: 1.3rem;
  color: #fff;
  text-decoration: none;
}

.header__nav__socialmedia-section {
  display: flex;
  justify-content: space-around;
}

.header__nav__socialmedia-section>.header__nav__link>span {
  display: none;
}

@supports (display: grid) {
  body {
    overflow: hidden;
  }
  #app {
    display: grid;
    height: 100%;
    overflow-x: hidden;
    overflow-y: auto;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto 1fr;
  }
  .header {
    grid-column: 1 / span 12;
    grid-row: 1;
  }
  .main-page {
    align-self: center;
    margin-top: 1rem;
    grid-column: 1 / span 12;
    grid-row: 2;
  }
  @media (min-width: 480px) {
    .header {
      position: fixed;
      top: 0;
      bottom: 0;
      display: flex;
      width: min-content;
      grid-column: 1;
      grid-row: 1 / span 2;
    }
    .header__expand-navigation-label {
      display: none;
    }
    .header__nav {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .header__nav__socialmedia-section {
      display: block;
    }
    .header__nav__link {
      position: relative;
    }
    .header__nav__link:not(:last-child) {
      margin-bottom: .5rem;
    }
    .header__nav__link__title {
      position: absolute;
      left: 105%;
      display: none;
      padding: .3rem;
      font-size: .7rem;
      background: #2a2a2a;
      border-radius: 3px;
    }
    .header__nav__link:hover>.header__nav__link__title {
      display: block;
    }
    .main-page {
      grid-column: 2 / span 12;
    }
  }
}
</style>
