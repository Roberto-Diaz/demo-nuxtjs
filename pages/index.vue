<template>
  <div>
    <h1>Welcome to my nuxt demo</h1>
  </div>
</template>

<script>
export default {
  head () {
    return {
      title: 'Welcome | nuxt app',
      meta: [{
        hid: 'description',
        name: 'description',
        content: 'Website about demo nuxt'
      }],
      htmlAttrs: { lang: 'en' }
    }
  }
}
</script>
