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

<style lang='scss' scoped>
// Fonts
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP&family=Saira+Semi+Condensed&display=swap');

$family-primary: 'Saira Semi Condensed';

// Import Bulma and Buefy styles
@import "~bulma/sass/utilities/_all";
@import "~bulma";
@import "~buefy/src/scss/buefy";
</style>
