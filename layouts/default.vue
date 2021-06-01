<template>
  <div class="site-container">
    <div class="site-content">
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<style lang='scss' scoped>
// Import Bulma's core
@import "~bulma/sass/utilities/_all";

.site-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.site-content {
  flex: 1;
}

.footer {
  background-color: $white;
  color: $black;
}
</style>
