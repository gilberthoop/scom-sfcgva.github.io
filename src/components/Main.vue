<template>
  <v-container class="main">
    <Introduction />
    <About />
  </v-container>
</template>

<script>
import Introduction from './body/Introduction'
import About from './body/About'
export default {
  name: 'Main',

  components: {
    Introduction,
    About
  }
}
</script>

<style lang="scss" scoped>
.main {
  font-family: "Outfit", sans-serif;
  color: white;
  margin-bottom: 60px;

  @media only screen and (max-width: 960px) {
    padding: 50px;
  }

  @media only screen and (max-width: 600px) {
    padding: 15px;
  }
}
</style>