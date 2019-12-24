<template>
  <Layout>
    <div class="content_title">
      <h1 class="title main">Learned Equine</h1>
      <h4 class="title sub">It's pronounced "Learn-ed"</h4>
    </div>
    <!-- <div class="content">
      <div class="text">

      </div>
    </div> -->
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Home',
  }
}
</script>

<style scoped>
.bg {
  background-image: url('../assets/background/index.jpg');
}

.content_title {
  margin-bottom: 50vh;
  position: relative;
  width: 100%;
}

.main {
  font-family: Garamond;
  font-size: 3rem;
  font-weight: bold;
}

.sub {
  font-style: italic;
}

.title {
  color: #FFFFFF;
  text-align: center;
}
</style>
