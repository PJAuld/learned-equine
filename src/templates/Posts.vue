<template>
  <Layout>
    <div class="content">
      <div class="back">
        <g-link class="back_link" :to="`blog`">Back</g-link>
      </div>
      <div class="text">
        <h1>{{ $page.posts.title }}</h1>
        <p>{{ $page.posts.body }}</p>
      </div>
    </div>
  </Layout>
</template>

<page-query>
query Posts ($id: ID!) {
  posts (id: $id) {
    title
    body
  }
}
</page-query>

<style scoped>
.back {
  position: relative;
  padding: 3px 0 0 9px;
}

.back_link {
  text-decoration: none;
}

.bg {
  background-image: url('../assets/background/blog.jpg');
}

.text {
  padding-top: 2vh;
}
</style>
