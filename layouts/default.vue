<template>
  <div class="site-container">
    <Navbar />
    <div class="site-content container">
      <nuxt />
    </div>
    <Footer />
  </div>
</template>

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
