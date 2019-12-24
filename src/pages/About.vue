<template>
  <Layout>
    <div class="content">
      <div class="text">
        <h1>About</h1>
        <h2>Kellie Auld</h2>
        <div class="section">
          <div class="img_wrapper">
            <g-image class="headshot" src="../assets/images/kellie.jpg" />
          </div>
          <p>{{ PLACEHOLDER }}</p>
        </div>
        <h2>Little Girl</h2>
        <div class="section">
          <div class="img_wrapper">
            <g-image class="headshot" src="../assets/images/lita.jpg" />
          </div>
          <p>{{ PLACEHOLDER }}</p>
        </div>
        <h2>Obi</h2>
        <div class="section">
          <div class="img_wrapper">
            <g-image class="headshot" src="../assets/images/obi.jpg" />
          </div>
          <p>{{ PLACEHOLDER }}</p>
        </div>
        <h2>Parker and Jovi</h2>
        <div class="section">
          <div class="img_wrapper">
            <g-image class="headshot" src="../assets/images/parker_jovi.jpg" />
          </div>
          <p>{{ PLACEHOLDER }}</p>
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

export default {
  data() {
    return {
      PLACEHOLDER,
    }
  },
  metaInfo: {
    title: 'About',
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  margin-bottom: 5vh;
}

h2 {
  margin: 0 0 1vh 5vh;
}

p {
  padding: 1%;
}

.bg {
  background-image: url('../assets/background/about.jpg');
}

.headshot {
  min-height: 100%;
  min-width: 100%;
  position: absolute;
  width: 100%;
}

.img_wrapper {
  margin: auto;
  overflow: hidden;
  padding-bottom: 80%;
  position: relative;
  width: 80%;
}

.section {
  display: grid;
  grid-template-columns: 30% 70%;
  margin-bottom: 5vh;
}
</style>
