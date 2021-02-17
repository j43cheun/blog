<template>
  <b-button
    tag="a"
    :href="href"
    :size="size"
    icon-left="information-outline"
    type="is-light is-info"
  >
    More Info
  </b-button>
</template>

<script>
export default {
  props: {
    href: {
      type: String,
      required: true
    },
    size: {
      type: String,
      required: false,
      default: 'is-default'
    }
  }
}
</script>
