<template>
  <div>
    <div class="grid grid-cols-1 lg:grid-cols-4 md:grid-cols-3 gap-4 gap-4">
      <div class="bg-gray-100 p-2">
        <p class="text-center">
          titulo
        </p>
        <p class="text-justify">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam recusandae magnam sapiente sint aspernatur! Nulla, cum molestiae? Quisquam, quasi. Modi odit harum iure autem omnis quaerat! Porro excepturi exercitationem pariatur.
        </p>
      </div>
      <div class="bg-gray-100 p-2">
        <p class="text-center">
          titulo
        </p>
        <p class="text-justify">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam recusandae magnam sapiente sint aspernatur! Nulla, cum molestiae? Quisquam, quasi. Modi odit harum iure autem omnis quaerat! Porro excepturi exercitationem pariatur.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
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
