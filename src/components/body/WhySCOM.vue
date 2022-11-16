<template>
  <v-container class="why d-flex flex-column flex-md-row-reverse">
    <div class="why__header text-center">Why do we have SCOM?</div>
    <v-card
      class="why__body pa-7"
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
  name: 'WhySCOM',

  data () {
    return {
      contents: [
        'To showcase SFC culture and to document its history.',
        'To support other ministries in their missions and create a positive experience for everyone involved.'
      ]
    }
  }
})
</script>

<style scoped lang="scss">
.why {
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