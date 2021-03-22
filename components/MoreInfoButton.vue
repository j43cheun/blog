<template>
  <b-button
    tag="a"
    :href="href"
    :size="size"
    icon-left="information-outline"
    :type="type"
    :outlined="outlined"
    rounded
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
    },
    type: {
      type: String,
      required: false,
      default: ''
    },
    outlined: {
      type: Boolean,
      required: false,
      default: false
    }
  }
}
</script>
