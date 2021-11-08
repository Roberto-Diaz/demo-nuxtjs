<template>
  <div>
    <h1>Post Detail</h1>
    <pre>{{ post }}</pre>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
      post: {}
    }
  },
  async created () {
    try {
      const res = await axios.get('https://jsonplaceholder.typicode.com/posts/' + this.$route.params.id)
      this.post = res.data
    } catch (error) {
      console.log(error)
    }
  }
}
</script>
