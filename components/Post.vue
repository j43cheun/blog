<template>
  <div class="container">
    <section class="section">
      <span v-for="tag of post.tags" :key="tag" class="tag">
        {{ tag }}
      </span>
      <div>
        <h1 class="title">
          {{ post.title }}
        </h1>
        <h2 class="subtitle">
          {{ post.description }}
        </h2>
      </div>
      <Timestamp :created-at="post.date" :updated-at="post.updatedAt" />
      <github-button
        v-if="post.github != null"
        :href="post.github"
        class="mt-5"
      />
    </section>
    <section class="section content">
      <nuxt-content :document="post" />
    </section>
  </div>
</template>

<script>
import GithubButton from './GithubButton.vue'
export default {
  components: { GithubButton },
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
