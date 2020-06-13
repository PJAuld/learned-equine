<template>
  <Layout>
    <div class="content">
      <div class="text">
        <h1>About</h1>
        <div class="about">
          <div class="entity">
            <h2>Kellie Auld</h2>
            <div class="section a">
              <div class="img_wrapper">
                <g-image class="headshot" src="../assets/images/kellie.jpg" />
              </div>
              <p class="left">{{ PLACEHOLDER }}</p>
            </div>
          </div>
          <div class="entity">
            <h2 class="title_right">Little Girl</h2>
            <div class="section b">
              <div class="img_wrapper">
                <g-image class="headshot" src="../assets/images/lita.jpg" />
              </div>
              <p class="right">{{ PLACEHOLDER }}</p>
            </div>
          </div>
          <div class="entity">
            <h2>Obi</h2>
            <div class="section a">
              <div class="img_wrapper">
                <g-image class="headshot" src="../assets/images/obi.jpg" />
              </div>
              <p class="left">{{ PLACEHOLDER }}</p>
            </div>
          </div>
          <div class="entity">
            <h2 class="title_right">Parker and Jovi</h2>
            <div class="section b">
              <div class="img_wrapper">
                <g-image class="headshot" src="../assets/images/parker_jovi.jpg" />
              </div>
              <p class="right">{{ BUNNY_PLACEHOLDER }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Layout>
</template>

<script>
const PLACEHOLDER = `Lorem ipsum dolor sit amet, consectetur adipisicing elit,
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
    ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip
    ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
    voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
    occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit
    anim id est laborum.`;
const BUNNY_PLACEHOLDER = `Bunny bunny bunny bunny bunny bunny bunny bunny
    bunny bunny bunny bunny bunny bunny bunny bunny bunny bunny bunny
    bunny bunny bunny bunny bunny bunny bunny bunny bunny bunny bunny
    bunny bunny bunny bunny bunny bunny bunny bunny bunny bunny bunny`

export default {
  data() {
    return {
      BUNNY_PLACEHOLDER,
      PLACEHOLDER,
    }
  },
  metaInfo: {
    title: 'About',
  }
}
</script>

<style scoped>
.bg {
  background-image: url('../assets/background/about.jpg');
}

h1 {
  text-align: center;
  margin-bottom: 5vh;
}

h2 {
  margin: 0 0 1vh 6vh;
  padding-top: 2vh;
}
p {
  padding: 1%;
}

.entity {
  border: 1px solid #a39d94;
  border-radius: 10px;
  height: auto;
  margin: 5px;
  padding: 2px;
}

.img_wrapper {
  margin: auto;
  overflow: hidden;
  padding-bottom: 80%;
  position: relative;
  width: 80%;
}
.headshot {
  min-height: 100%;
  min-width: 100%;
  position: absolute;
  width: 100%;
}

.right {
  padding-left: 2.5vw;
}
.left {
  padding-right: 2.5vw
}

.section {
  display: grid;
  margin-bottom: 5vh;
}
.a {
  grid-template-columns: 30% 70%;
}
.b {
  grid-template-columns: 70% 30%;
}

.title_right {
  text-align: right;
  padding-right: 2.5vw;
}

@media (max-width: 425px) {
  h2, .title_right {
    margin-left: 0;
    text-align: center;
  }
  .a, .b {
    grid-template-columns: 100%;
  }
}
</style>
