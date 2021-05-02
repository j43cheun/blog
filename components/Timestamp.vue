<template>
  <div>
    <t class="is-size-7">
      {{ formattedTimestamp }}
    </t>
  </div>
</template>

<script>
export default {
  props: {
    createdAt: {
      type: String,
      required: false,
      default: null
    },
    updatedAt: {
      type: String,
      required: false,
      default: null
    }
  },
  computed: {
    formattedTimestamp () {
      let formattedTimestamp = ''

      if (this.createdAt != null) {
        formattedTimestamp += this.formatDateTime(this.createdAt)
      }

      return formattedTimestamp
    }
  },
  methods: {
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

</style>
