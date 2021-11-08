<template>
  <nuxt-link :to="'/posts/'+id">
    <div class="bg-gray-100 p-2 shadow-lg hover:bg-gray-200">
      <h2 class="text-center text-xl">
        {{ title }}
      </h2>
      <p class="text-justify">
        {{ body }}
      </p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: 'Post',
  props: {
    title: {
      type: String,
      required: true
    },
    body: {
      type: String,
      required: true
    },
    id: {
      type: Number,
      required: true
    }
  }
}
</script>
