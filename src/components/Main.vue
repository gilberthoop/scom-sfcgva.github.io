<template>
  <v-container class="main">
    <Introduction />
    <About />
    <WhySCOM />
    <RequestForm />
    <Teams />
    <Trivia />
    <FrequentlyAskedQuestions />
  </v-container>
</template>

<script>
import Introduction from './body/Introduction'
import About from './body/About'
import RequestForm from './body/RequestForm'
import Teams from './body/Teams'
import WhySCOM from './body/WhySCOM'
import Trivia from './body/Trivia'
import FrequentlyAskedQuestions from './body/FrequentlyAskedQuestions'
export default {
  name: 'Main',

  components: {
    Introduction,
    About,
    RequestForm,
    Teams,
    WhySCOM,
    Trivia,
    FrequentlyAskedQuestions
  }
}
</script>

<style lang="scss" scoped>
.main {
  font-family: "Outfit", sans-serif;
  color: white;

  @media only screen and (max-width: 960px) {
    padding: 50px 50px 0 50px;
  }

  @media only screen and (max-width: 600px) {
    padding: 15px;
  }
}
</style>