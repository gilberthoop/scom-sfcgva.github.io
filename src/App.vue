<template>
  <v-app class="app">
    <AppMenu />
    <v-main>
      <Main/>
    </v-main>
  </v-app>
</template>

<script>
import Main from './components/Main';
import AppMenu from './components/header/AppMenu'

export default {
  name: 'App',

  components: {
    Main,
    AppMenu
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss" scoped>
.app {
  background-color: #1f8fe2;
}
</style>