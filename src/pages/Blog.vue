<template>
  <Layout>
    <div class="content">
      <div class="text">
        <h1>Blog Posts</h1>
        <ul>
          <li v-for="edge in $page.allPosts.edges" :key="edge.node.id">
            {{ edge.node.title }}
            <br />
            {{ edge.node.body }}
            <br />
            <g-link class="blog_link" :to="`blog/${edge.node.id}`">{{ edge.node.id }}</g-link>
          </li>
        </ul>
      </div>
    </div>
  </Layout>
</template>

<page-query>
  query {
    allPosts {
      edges {
        node {
          id
          title
          body
        }
      }
    }
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: 'Blog'
  }
}
</script>

<style scoped>
.bg {
  background-image: url('../assets/background/blog.jpg');
}

.blog_link {
  text-decoration: none;
}
</style>
