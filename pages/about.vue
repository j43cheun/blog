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

<style>
  .icon.icon-link {
    background-image: url('~assets/svg/hashtag.svg');
    display: inline-block;
    width: 20px;
    height: 20px;
    background-size: 20px 20px;
  }
</style>
