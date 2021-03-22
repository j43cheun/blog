<template>
  <section class="hero is-fullheight is-dark">
    <div class="hero-head">
      <Navbar />
    </div>
    <div class="hero-body">
      <div class="container has-text-centered">
        <p class="title">
          Justin Cheung
        </p>
        <p class="subtitle">
          Software Developer / Amateur Photographer
        </p>
        <b-button tag="router-link" to="/about" type="is-white" outlined rounded>
          About Me
        </b-button>
        <b-button tag="router-link" to="/projects" type="is-white" outlined rounded>
          My Projects
        </b-button>
      </div>
    </div>
    <div class="hero-footer">
      <Footer />
    </div>
  </section>
</template>

<script>
export default {
  head () {
    return {
      title: 'Justin Cheung'
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~bulma/sass/utilities/_all";
@import "~bulma";
@import "~buefy/src/scss/buefy";

$footer-background-color: rgba(0, 0, 0, 0);

.hero {
  background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url('../static/gallery/seattle_amazon_spheres_exterior.JPG');
  background-size: cover;
  background-position: center;
}

.footer {
  background: transparent;
}

</style>
