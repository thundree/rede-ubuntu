<template>
  <v-flex class="pa-0 d-flex flex-row align-center justify-center">
    <div>
      <v-switch
        v-model="$vuetify.theme.dark"
        color="gray"
        class="mt-3"
        label="Dark mode"
      />
    </div>
    <div class="ml-auto social-media">
      <a href="#" target="_blank" rel="noopener noreferrer">
        <v-icon>mdi-instagram</v-icon>
      </a>
    </div>
  </v-flex>
</template>

<script>
export default {
  name: 'AppBarContent',
  data() {
    return {}
  },
  watch: {
    '$vuetify.theme.dark'(newVal) {
      localStorage.setItem('dark-theme', newVal === true)
    }
  },
  created() {
    if (process.client) {
      this.$vuetify.theme.dark = localStorage.getItem('dark-theme') === 'true'
    }
  }
}
</script>

<style lang="scss" scoped>
.social-media {
  a {
    text-decoration: none;
  }
}
</style>
