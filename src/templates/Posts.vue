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
a {
  color: inherit;
  padding: 0 5px;
}

a:hover {
  background-color: #089b06;
  border: 1px solid #089b06;
  border-radius: 7%;
  color: #FFFFFF;
  transition-duration: 0.2s;
  transition-timing-function: ease-in-out;
}

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
