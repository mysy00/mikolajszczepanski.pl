<template>
  <div id="app">
    <header class="header header-page">
      <label for="expandNavigation" class="header__expand-navigation-label">
        <menuhamburger
          iconColor="#fff"
          iconWidth="24"
          iconHeight="24"
          :amount="1"
        />
      </label>
      <input
        class="header__expand-navigation-input"
        id="expandNavigation"
        type="checkbox"
      />
      <nav class="header__nav">
        <div class="header__nav__main-section">
          <router-link class="header__link" to="/">
            <span class="header__link-title">Home</span>
            <home
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </router-link>
          <router-link class="header__link" to="/projects">
            <span class="header__link-title">Projects</span>
            <briefcase
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </router-link>
          <router-link class="header__link" to="/about">
            <span class="header__link-title">About</span>
            <about
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </router-link>
        </div>
        <div class="header__socialmedia-section">
          <!-- <a class="header__link" href="http://facebook.com/divoskyy">
            <span class="header__link-title">Facebook</span>
            <facebook
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </a> -->
          <a class="header__link" href="http://github.com/mysy00">
            <span class="header__link-title">Github</span>
            <github
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </a>
          <a class="header__link" href="http://gitlab.com/mysy00">
            <span class="header__link-title">GitLab</span>
            <gitlab
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </a>
          <a class="header__link" href="http://keybase.io/divosky">
            <span class="header__link-title">Keybase</span>
            <keybase
              iconColor="var(--nav-icon-color)"
              iconWidth="24"
              iconHeight="24"
              :amount="1"
            />
          </a>
        </div>
      </nav>
    </header>
    <main class="main-page">
      <router-view />
    </main>
  </div>
</template>

<script>
import menuhamburger from "@/components/icons/MenuHamburger";
import home from "@/components/icons/Home";
import briefcase from "@/components/icons/Briefcase";
import about from "@/components/icons/About";
import facebook from "@/components/icons/Facebook";
import github from "@/components/icons/Github";
import gitlab from "@/components/icons/Gitlab";
import keybase from "@/components/icons/Keybase";

export default {
  components: {
    menuhamburger,
    home,
    briefcase,
    about,
    facebook,
    github,
    gitlab,
    keybase,
  },
  created: function () {
    localStorage.pageTitle = document.title;
  },
};
</script>

<style>
:root {
  --primary-color: #1082e8;
  --box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
  --nav-icon-color: #bbb;
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
  font-family: "Avenir", Helvetica, Arial, sans-serif;
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
  content: "";
  background: #00000066;
}

#app {
  position: relative;
  min-height: 100%;
}

.header {
  background: #000;
  user-select: none;
}

.header__expand-navigation-label {
  display: block;
  padding: 4px;
  text-align: right;
}

.header__expand-navigation-input {
  display: none;
}

.header__expand-navigation-input:checked + .header__nav {
  display: block;
}

.header__nav {
  display: none;
}

.header__link {
  display: flex;
  justify-content: space-between;
  padding: 0.3rem;
  margin-bottom: 0.3rem;
  font-size: 1.3rem;
  color: #fff;
  text-decoration: none;
}

.router-link-exact-active > .header__link-icon,
.router-link-exact-active > .header__link-title {
  --nav-icon-color: --primary-color;
  color: var(--primary-color);
  fill: var(--primary-color);
}

.header__socialmedia-section {
  display: flex;
  justify-content: space-around;
}

.header__socialmedia-section > .header__link > span {
  display: none;
}

.offscreen {
  position: absolute;
  left: -10000px;
  top: auto;
  width: 1px;
  height: 1px;
  overflow: hidden;
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
    .header__socialmedia-section {
      display: block;
    }
    .header_link {
      position: relative;
    }
    .header__link:not(:last-child) {
      margin-bottom: 0.5rem;
    }
    .header__link-title {
      position: absolute;
      left: 105%;
      display: none;
      padding: 0.3rem;
      font-size: 0.7rem;
      background: #2a2a2a;
      border-radius: 3px;
    }
    .header__link:hover > .header__link-title {
      display: block;
    }
    .main-page {
      grid-column: 2 / span 12;
    }
  }
}
</style>
