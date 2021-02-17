<template>
  <div>
    <div class="tags mb-0">
      <span v-for="tag of post.tags" :key="tag" class="tag">
        {{ tag }}
      </span>
    </div>
    <div>
      <nuxt-link :to="{ name: slug, params: { slug: post.slug } }" class="is-size-4">
        {{ post.title }}
      </nuxt-link>
      <p class="subtitle is-6">
        {{ post.description }}
      </p>
    </div>
    <Timestamp :created-at="post.date" />
    <github-button
      v-if="post.github != null"
      :href="post.github"
      size="is-small"
      class="mt-2"
    />
    <more-info-button
      v-if="post.info != null"
      :href="post.info"
      size="is-small"
      class="mt-2"
    />
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    },
    slug: {
      type: String,
      required: true
    }
  }
}
</script>
