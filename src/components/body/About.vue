<template>
  <v-container class="about d-flex flex-column flex-md-row">
    <div class="about__header">What is SCOM?</div>
    <v-card
      class="about__body pa-7"
      color="#1D2939"
    >
      <p
        v-for="(content, index) in contents"
        :key="index"
      >
        {{ content }}
      </p>
    </v-card>

  </v-container>
</template>

<script>
export default ({
  name: 'About',

  data () {
    return {
      contents: [
        'SFC Communications functions as the communication arm of the ministry across all programs and areas, both within and even outside the ministry.',
        'SFC Communications ensures that all necessary and essential information are being provided and communicated properly through the right channel, to the right persons at the right time.',
        'SFC Communications has the responsibility to archive all the materials and references that are being used by the ministry for the purpose of evangelization.'
      ]
    }
  }
})
</script>

<style scoped lang="scss">
.about {
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
