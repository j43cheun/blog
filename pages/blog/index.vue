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
    <Footer />
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
