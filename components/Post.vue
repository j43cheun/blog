<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        {{ post.title }}
      </h1>
      <t class="is-size-7">
        {{ formatDate(post.date) }} ⋅ Last Updated: {{ formatDateTime(post.updatedAt) }}
      </t>
    </section>
    <section class="section content">
      <nuxt-content :document="post" />
    </section>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  },
  methods: {
    formatDate (dateTime) {
      const date = new Date(dateTime)
      const dateOptions = { year: 'numeric', month: 'long', day: 'numeric' }

      return date.toLocaleDateString('en-US', dateOptions)
    },
    formatDateTime (dateTime) {
      const date = new Date(dateTime)
      const dateOptions = { year: 'numeric', month: 'long', day: 'numeric' }
      const timeOptions = { timeZoneName: 'short' }

      return date.toLocaleDateString('en-US', dateOptions) + ' ' +
             date.toLocaleTimeString('en-US', timeOptions)
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
