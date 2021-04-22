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
  background: linear-gradient( rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25) ), url('/gallery/garbage_bin_embedded_system.jpg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
</style>
