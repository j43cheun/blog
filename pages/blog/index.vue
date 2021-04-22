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
              Blog
            </h1>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div v-for="post of posts" :key="post.slug" class="mb-6">
          <Result :post="post" slug="blog-slug" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const posts = await $content('blog', params.slug)
      .sortBy('date', 'desc')
      .fetch()

    return {
      posts
    }
  },
  head () {
    return {
      title: 'Blog - Justin Cheung'
    }
  }
}
</script>

<style scoped>
.hero {
  background: linear-gradient( rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25) ), url('/gallery/uw_campus_canada_goose.JPG');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
</style>
