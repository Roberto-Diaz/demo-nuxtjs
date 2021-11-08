<template>
  <div class="grid grid-cols-1 lg:grid-cols-4 md:grid-cols-3 gap-4 gap-4">
    <Post
      v-for="(post, index) in posts"
      :id="post.id"
      :key="index"
      :title="post.title"
      :body="post.body"
    />
  </div>
</template>

<script>
import axios from 'axios'
import Post from '../../components/Post.vue'
export default {
  components: {
    Post
  },
  data () {
    return {
      posts: []
    }
  },
  async created () {
    try {
      const res = await axios.get('https://jsonplaceholder.typicode.com/posts')
      this.posts = res.data
    } catch (error) {
      console.log(error)
    }
  }
}
</script>
