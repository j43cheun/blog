<template>
  <div class="site-container">
    <Navbar />
    <div class="site-content">
      <nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: 'Justin Cheung'
      }
    }
  }
</script>

<style scoped>
  .site-container {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  .site-content {
    flex: 1;
  }
</style>
