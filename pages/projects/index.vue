<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        My Projects 2
      </h1>
    </section>
    <section class="section">
      <div v-for="project of projects" :key="project.slug">
        <nuxt-link :to="{ name: 'projects-slug', params: { slug: project.slug } }">
          <h2>{{ project.slug }}</h2>
        </nuxt-link>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const projects = await $content('projects', params.slug)
      .sortBy('createdAt', 'asc')
      .fetch()

    return {
      projects
    }
  }
}
</script>
