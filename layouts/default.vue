<template>
  <v-app>
    <v-app-bar app flat absolute>
      <AppBarContent />
    </v-app-bar>
    <!--  -->
    <v-app-bar color="orange" app inverted-scroll elevate-on-scroll>
      <AppBarContent />
    </v-app-bar>
    <!--  -->
    <v-main class="mt-12 pt-4">
      <v-container>
        <Nuxt />
        <Nuxt />
        <Nuxt />
        <Nuxt />
        <Nuxt />
      </v-container>
    </v-main>
    <!--  -->
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import AppBarContent from '~/components/AppBarContent.vue'

export default {
  components: { AppBarContent },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped></style>
