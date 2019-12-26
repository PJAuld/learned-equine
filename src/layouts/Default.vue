<template>
  <div class="bg">
    <header class="header">
      <div id="logo">
        <g-link to="/">
          <h3>Learned Equine</h3>
        </g-link>
      </div>
      <div id="menu">
        <input class="toggle" type="checkbox" />
        <nav>
          <g-link class="nav_link" to="/">Home</g-link>
          <g-link class="nav_link" to="/blog">Blog</g-link>
          <a class="nav_link" href="https://www.youtube.com" target="_blank">YouTube</a>
          <g-link class="nav_link" to="/about">About</g-link>
          <g-link class="nav_link" to="/contact">Contact</g-link>
        </nav>
      </div>
      <div class="mobile_menu">Menu</div>
    </header>
    <transition name="fade" appear>
      <main>
        <div class="body">
          <slot />
        </div>
      </main>
    </transition>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body, html {
  height: 100%;
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  line-height: 1.5;
}
a, a:hover, a:active, a:focus {
  outline: 0;
  text-decoration: none;
}

h1 {
  text-align: center;
  margin-bottom: 5vh;
}

#logo {
  padding: 18px 5% 18px 5%;
}
h3 {
  color: #5E3B2A;
  font-family: Garamond;
  font-size: 2rem;
  font-style: italic;
}

nav {
  bottom: 0;
  margin: 0 70px 15px 0;
  position: absolute;
  right: 0;
}

.body {
  padding: 120px 10% 5% 10%;
}

.bg {
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 100%;
  position: relative;
}
.fade-enter-active {
  transition: opacity .4s;
}
.fade-enter {
  opacity: 0;
}

.content {
  border-radius: 10px;
  background-color: rgb(240, 231, 218, 0.9);
  position: relative;
  width: 100%;
}

.header {
  background-color: #f1ede1;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  height: 85px;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1;
}

.mobile_menu {
  border: 1px solid #a39d94;
  border-radius: 4px;
  color: #5E3B2A;
  cursor: pointer;
  display: none;
  letter-spacing: 0.1rem;
  padding: 10px;
  position: absolute;
  right: 4%;
  top: 25%;
}
.toggle {
  border: 0;
  display: none;
  height: 46px;
  opacity: 0;
  position: absolute;
  right: 8%;
  top: 25%;
  width: 67px;
  z-index: 2;
}
.mobile_menu:hover {
  background-color: #089b06;
  border: 1px solid #089b06;
  color: #FFFFFF;
  transition-duration: 0.2s;
  transition-timing-function: ease-in-out;
}

.nav_link {
  border: 1px solid #F1EDE1;
  border-radius: 0;
  color: #5E3B2A;
  cursor: pointer;
  letter-spacing: 0.1rem;
  margin-left: 2.5vw;
  padding: 7px;
  text-decoration: none;
  z-index: 1;
}
.nav_link:hover {
  background-color: #089b06;
  border: 1px solid #089b06;
  border-radius: 7%;
  color: #FFFFFF;
  transition-duration: 0.2s;
  transition-timing-function: ease-in-out;
}

.text {
  padding: 5vh 5%;
}

#menu {
  position: relative;
}

@media (max-width: 768px) {
  nav {
    display: none;
    grid-column: 1fr;
    margin-top: 1px;
    position: absolute;
    left: -100%;
    top: 85px;
    width: 200%;
  }
  .toggle:checked ~ nav {
    display: grid;
  }

  .nav_link {
    background-color: #F1EDE1;
    border: 0.5px solid #A39D94;
    margin: -1px;
    padding-left: 3vw;
  }

  .mobile_menu, .toggle {
    display: block;
  }

  h3 {
    font-size: 1.5rem;
  }
  #logo {
    padding: 25px 0 18px 25px;
  }
}

@media (max-width: 425px) {
  h3 {
    font-size: 1.2rem;
  }
  #logo {
    padding: 30px 0 18px 25px;
  }
}
</style>
