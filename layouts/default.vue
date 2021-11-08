<template>
  <div>
    <Navigation />
    <div class="container mx-auto py-2 px-4">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import Navigation from '../components/Navigation.vue'

export default {
  components: {
    Navigation
  }
}
</script>
