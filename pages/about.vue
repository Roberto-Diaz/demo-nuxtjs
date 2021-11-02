<template>
  <div>
    <h1>About</h1>
  </div>
</template>

<script>
export default {
  head () {
    return {
      title: 'About | nuxt app',
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
