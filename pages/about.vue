<template>
  <Post :post="post" />
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const post = await $content('about').fetch()

    return {
      post
    }
  }
}
</script>
