<template>
  <Layout>
    <div class="content">
      <div class="text">
        <h1>Blog Posts</h1>
        <ul>
          <BlogPost
              v-for="edge in $page.allPosts.edges"
              :key="edge.node.id"
              :id="edge.node.id"
              :title="edge.node.title"
              :body="edge.node.body" />
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
import BlogPost from '~/components/BlogPost.vue';

export default {
  components: {
    BlogPost,
  },
  metaInfo: {
    title: 'Blog'
  }
};
</script>

<style scoped>
ul {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.bg {
  background-image: url('../assets/background/blog.jpg');
}

.blog_link {
  text-decoration: none;
}
</style>
