<template>
  <div class="site-container">
    <div class="site-content">
      <Nuxt />
    </div>
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
