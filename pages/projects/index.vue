<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        Projects
      </h1>
    </section>
    <section class="section">
      <div v-for="project of projects" :key="project.slug" class="mb-6">
        <div class="tags mb-0">
          <span v-for="tag of project.tags" :key="tag" class="tag">
            {{ tag }}
          </span>
        </div>
        <nuxt-link :to="{ name: 'projects-slug', params: { slug: project.slug } }" class="is-size-4">
          {{ project.title }}
        </nuxt-link>
        <p class="subtitle is-6 mb-0">
          {{ project.description }}
        </p>
        <Timestamp :created-at="project.date" class="mb-5" />
        <b-button
          tag="a"
          :href="project.link"
          icon-left="github"
        >
          GitHub
        </b-button>
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
