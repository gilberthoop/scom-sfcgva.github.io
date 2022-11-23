<template>
  <v-container class="form d-flex flex-column flex-md-row">
    <div
      id="form"
      class="anchor"
    >
    </div>

    <div class="form__header">Ask for help!</div>
    <v-card
      class="form__body pa-7"
      color="#003B89"
    >
      <p
        v-for="(content, index) in contents"
        :key="index"
      >
        {{ content }}
      </p>

      <div class="text-center">
        <v-btn
          class="my-3 text-capitalize"
          color="primary"
          large
        >
          <a
            class="form__link"
            href="https://docs.google.com/forms/d/e/1FAIpQLSf9lo3blCxC9rzRHcsPNgt4IiwBgNkX24fRFotfXhjffBXfjg/viewform?usp=pp_url"
            target="_blank"
          >
            Send a request
          </a>
        </v-btn>
      </div>
    </v-card>
  </v-container>
</template>

<script>
export default({
  name: 'RequestForm',

  data () {
    return {
      contents: [
        'SCOM acts to support the ministry of CFC-Singles for Christ in enabling the mission effectively. We serve to translate the faith and maximize the ministry\'s potential to bring Christ to different social media platforms.',
        'In order to serve you better, please open the link to the request form and fill it out. A member of our team will respond to your request within 24 hours.'
      ]
    }
  }
})
</script>


<style scoped lang="scss">
.form {
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

  &__link {
    text-decoration: none;
    color: white;
    font-size: 20px;
  }
}

.anchor {
  display: block;
  position: relative;
  top: -150px;
  visibility: hidden;
}
</style>