<template>
  <div>
    <section class="hero is-halfheight is-dark" :style="heroImage">
      <div class="hero-head">
        <Navbar />
      </div>
      <div class="hero-body">
        <div class="container">
          <div class="tags mb-0">
            <span v-for="tag of post.tags" :key="tag" class="tag is-white is-rounded">
              {{ tag }}
            </span>
          </div>
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
            type="is-white"
            outlined
          />
          <more-info-button
            v-if="post.info != null"
            :href="post.info"
            class="mt-5"
            type="is-white"
            outlined
          />
        </div>
      </div>
    </section>
    <section class="section content-section">
      <div class="container">
        <div class="content">
          <nuxt-content :document="post" />
        </div>
      </div>
    </section>
    <Footer />
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
  data () {
    return {
      heroImage: {
        backgroundImage: this.post.image == null ? '' : `linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url(${this.post.image})`,
        backgroundSize: 'cover',
        backgroundPosition: 'center'
      }
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
.icon.icon-link:after {
  content: '#';
}
.content-section {
  min-height: 30vh;
}
</style>
