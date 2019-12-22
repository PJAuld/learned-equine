<template>
  <Layout>
    <div class="body">
      <div class="content">
        <h1>Blog Posts</h1>
        <ul>
          <li v-for="edge in $page.allPosts.edges" :key="edge.node.id">
            {{ edge.node.title }}
            <br/>
            {{ edge.node.fields.body }}
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
          fields {
            body
          }
        }
      }
    }
  }
</page-query>

<style scoped>
ul {
  padding: 0 5%;
}

.bg {
  background-image: url('../assets/blog.jpg');
}
</style>
