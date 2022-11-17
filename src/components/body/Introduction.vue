<template>
  <v-container class="intro">
    <div class="intro__contents d-flex">
      <div class="intro__contents--wide">
        <p class="intro__contents--title">
          CFC-Singles for Christ
          <br/>Greater Vancouver Area
        </p>
        <p class="intro__contents--subtitle mt-5">
          Communications
        </p>
      </div>
      <div class="intro__contents--narrow">
        <v-img
          class="intro__contents--image"
          :src="logo"
          max-height="300"
          max-width="300"
        />
      </div>
    </div>
  </v-container>
</template>

<script>
export default ({
  name: 'Introduction',
  
  data () {
    return {
      logo: '/images/intro/website.gif'
    }
  }
})
</script>

<style scoped lang="scss">
.intro {
  height: 100vh;
  padding: 150px 0;
  line-height: 1.2;

  @media screen and (max-width: 620px) {
    padding-top: 45px;
  }

  &__contents {
    font-size: 50px;

    @media screen and (max-width: 1270px) {
      flex-direction: column;
    }

    &--wide {
      width: 70%;

      @media screen and (max-width: 1270px) {
        width: 100%;
      }
    }

    &--narrow {
      border-radius: 50%;

      @media screen and (max-width: 1270px) {
        align-self: end;
        margin-top: 10px;
      }

      @media screen and (max-width: 620px) {
        align-self: center;
      }
    }

    &--title {
      font-size: 30px;

      @media screen and (max-width: 560px) {
        text-align: center;
      }
    }

    &--subtitle {
      font-size: 80px;
      font-weight: bold;
      color: #003B89;

      @media screen and (max-width: 700px) {
        font-size: 60px;
      }

      @media screen and (max-width: 500px) {
       text-align: center;
       font-size: 50px;
      }

      @media screen and (max-width: 400px) {
       text-align: center;
       font-size: 35px;
      }
    }

    &--image {
      border-radius: 50%;
    }
  }
}
</style>