<template>
  <div>
    <section class="hero is-halfheight is-dark">
      <div class="hero-head">
        <Navbar />
      </div>
      <div class="hero-body">
        <div class="container">
          <div>
            <h1 class="title">
              My Projects
            </h1>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div v-for="post of posts" :key="post.slug" class="mb-6">
          <Result :post="post" slug="projects-slug" />
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const posts = await $content('projects', params.slug)
      .sortBy('date', 'desc')
      .fetch()

    return {
      posts
    }
  },
  head () {
    return {
      title: 'My Projects - Justin Cheung'
    }
  }
}
</script>

<style scoped>
.hero {
  background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url('/gallery/garbage_bin_embedded_system.JPG');
  background-size: cover;
  background-position: center;
}
</style>
