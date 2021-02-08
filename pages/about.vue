<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        {{ page.title }}
      </h1>
    </section>
    <section class="section content">
      <nuxt-content :document="page" />
    </section>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('about').fetch()

    return {
      page
    }
  }
}
</script>
