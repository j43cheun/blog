<template>
  <b-button
    tag="a"
    :href="href"
    icon-left="github"
  >
    GitHub
  </b-button>
</template>

<script>
export default {
  props: {
    href: {
      type: String,
      required: true
    }
  }
}
</script>
