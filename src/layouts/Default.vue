<template>
  <div class="bg">
    <header class="header">
      <div id="logo">
        <h3>Learned Equine</h3>
      </div>
      <div id="menu">
        <nav>
          <g-link class="nav_link" to="/">Home</g-link>
          <g-link class="nav_link" to="/blog">Blog</g-link>
          <g-link class="nav_link" to="https://www.youtube.com" target="_blank">YouTube</g-link>
          <g-link class="nav_link" to="/about/">About</g-link>
          <g-link class="nav_link" to="/contact/">Contact</g-link>
        </nav>
      </div>
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

h1 {
  text-align: center;
  margin-bottom: 5vh;
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

.content {
  background-color: rgb(240, 231, 218, 0.9);
  position: relative;
  width: 100%;
}

.fade-enter-active {
  transition: opacity .4s;
}

.fade-enter {
  opacity: 0;
}

.header {
  background-color: rgb(241, 237, 225, 1);
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  height: 85px;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1;
}

.nav_link {
  color: #5E3B2A;
  letter-spacing: 0.1rem;
  margin-left: 2.5vw;
  padding: 7px;
  text-decoration: none;
}

.nav_link:hover {
  background-color: #089b06;
  color: #FFFFFF;
  transition-duration: 0.2s;
  transition-timing-function: ease-in-out;
}

.text {
  padding: 5vh 5%;
}

#logo {
  padding: 18px 33px 18px 66px;
}

#menu {
  position: relative;
}
</style>
