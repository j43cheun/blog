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
        formattedTimestamp += this.formatDate(this.createdAt)
      }

      if (this.createdAt != null &&
          this.updatedAt != null) {
        formattedTimestamp += ' ⋅ '
      }

      if (this.updatedAt != null) {
        formattedTimestamp += 'Last Updated: ' +
                              this.formatDateTime(this.updatedAt)
      }

      return formattedTimestamp
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

</style>
