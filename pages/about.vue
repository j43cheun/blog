<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        {{ page.title }}
      </h1>
      <t class="is-size-7">Last Updated: {{ formatDateTime(page.updatedAt) }}</t>
    </section>
    <section class="section content">
      <nuxt-content :document="page" />
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    formatDateTime (dateTime) {
      const date = new Date(dateTime)
      const dateOptions = { year: 'numeric', month: 'long', day: 'numeric' }
      const timeOptions = { timeZoneName: 'short' }

      return date.toLocaleDateString('en-US', dateOptions) + ' ' +
             date.toLocaleTimeString('en-US', timeOptions)
    }
  },
  async asyncData ({ $content }) {
    const page = await $content('about').fetch()

    return {
      page
    }
  }
}
</script>

<style>
  .icon.icon-link {
    background-image: url('~assets/svg/hashtag.svg');
    display: inline-block;
    width: 20px;
    height: 20px;
    background-size: 20px 20px;
  }
</style>
