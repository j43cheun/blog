<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        My Projects
      </h1>
    </section>
    <section class="section">
      <div v-for="post of posts" :key="post.slug" class="mb-6">
        <Result :post="post" slug="projects-slug" />
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
