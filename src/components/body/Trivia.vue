<template>
  <v-container class="trivia d-flex flex-column flex-md-row-reverse">
    <div class="trivia__header text-center">Did you know?</div>
    <v-card
      class="trivia__body pa-7"
      color="#003B89"
    >
      <p
        v-for="(content, index) in contents"
        :key="index"
        class="my-5"
      >
        {{ content }}
      </p>
    </v-card>
  </v-container>
</template>

<script>
export default ({
  name: 'Trivia',

  data () {
    return {
      contents: [
        'You can add your service experience with SCOM to your resume, CV and LinkedIn.',
        'We have a Udemy account with online courses to help you learn graphics & web design and video editing.',
        'We are currently building a free accountability mobile app that is similar to Covenant Eyes.',
        'We have bowling and pub nights.'
      ]
    }
  }
})
</script>

<style scoped lang="scss">
.trivia {
  margin: 15% 0;

  &__header {
    font-size: 60px;
    font-weight: bold;
    margin: auto;
    width: 1000px;
    max-width: 600px;

    @media only screen and (max-width: 960px) {
      margin-bottom: 50px;
      max-width: 100%;
      text-align: center;
    }

    @media only screen and (max-width: 620px) {
      font-size: 45px;
    }
  }

  &__body {
    font-size: 20px;
    color: #fff !important;
    border-radius: 30px;
    width: 100%;

    @media only screen and (max-width: 600px) {
      border-radius: 15px;
    }
  }
}
</style>
