<template>
  <Post :post="post" />
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const post = await $content('blog', params.slug).fetch()

    return {
      post
    }
  },
  head () {
    return {
      title: this.post.title
    }
  }
}
</script>
