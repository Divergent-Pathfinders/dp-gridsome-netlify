<template>
  <Layout>
    <PostList
      v-for="edge in $page.allPost.edges"
      :key="edge.node.id"
      :post="edge.node"
    />
  </Layout>
</template>

<page-query>
query {
  allPost {
    edges {
      node {
        path
        title
        excerpt
      }
    }
  }
}
</page-query>

<script>
import PostList from '../components/postlist';
export default {
  components: { PostList },
  metaInfo: {
    title: 'My blog'
  }
}
</script>