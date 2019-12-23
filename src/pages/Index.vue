<template>
  <Layout>
    <div class="body">
      <div class="content">
        <h1 class="title main">Learned Equine</h1>
        <h4 class="title sub">It's pronounced "Learn-ed Equine"</h4>
      </div>
    </div>
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
  background-image: url('../assets/index.jpg');
}

.content {
  background-color: rgb(0, 0, 0, 0);
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
