<template>
  <v-container class="main">
    <Introduction />
    <About />
    <Trivia />
    <FrequentlyAskedQuestions />
  </v-container>
</template>

<script>
import Introduction from './body/Introduction'
import About from './body/About'
import Trivia from './body/Trivia'
import FrequentlyAskedQuestions from './body/FrequentlyAskedQuestions'
export default {
  name: 'Main',

  components: {
    Introduction,
    About,
    Trivia,
    FrequentlyAskedQuestions
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