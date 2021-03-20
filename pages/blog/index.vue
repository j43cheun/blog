<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        Blog
      </h1>
    </section>
    <section class="section">
      <div v-for="post of posts" :key="post.slug" class="mb-6">
        <Result :post="post" slug="blog-slug" />
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
