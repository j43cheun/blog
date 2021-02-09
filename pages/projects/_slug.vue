<template>
  <Post :post="project" />
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const project = await $content('projects', params.slug).fetch()

    return {
      project
    }
  }
}
</script>
