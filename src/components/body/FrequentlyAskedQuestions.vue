<template>
  <div class="faq">
    <div class="faq__title text-center my-3">
      Frequently Asked Questions
    </div>
    <div class="faq__section">
      <v-expansion-panels
        multiple
        accordion
      >
        <v-expansion-panel
          v-for="(item, index) in faqs"
          :key="index"
          ref="panel"
          class="faq_panel"
        >
          <v-expansion-panel-header
            ref="header"
            class="faq__header py-sm-7 py-md-5"
            color="#003B89"
          >
            {{ item.question }}
          </v-expansion-panel-header>
          <v-expansion-panel-content
            class="faq__content pa-3 pb-sm-4"
            color="#003B89"
          >
            {{ item.answer }}
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </div>
  </div>
</template>

<script>
export default ({
  name: 'FrequentlyAskedQuestions',

  data () {
    return {
      faqs: [
        {
          question: 'How can I get involved?',
          answer: 'We would love you to join our team! You may reach out to the programm coordinator, William Go at 604 832 3251. Instagram: @gilberthoop.'
        },
        {
          question: 'What are the requirements to join SFC Communications (SCOM)?',
          answer: 'We require SFC members who wish to join our team to have completed their Covenant Orientation Weekend and have their household heads consent and approval. Then we as a team will be providing training and guidance.'
        },
        {
          question: 'Which projects and/or activities has the team organized so far?',
          answer: 'On regional level, we have organized activities such as Household Heroes, Give Hope (#givehope) 2020, birthday greetings. On national level, we love to extend our expertise to service teams that are looking for graphics and web designers (e.g. https://sfctnc.herokuapp.com/). Follow our Instagram @cfcsfcgva for more.'
        }
      ]
    }
  }
})
</script>

<style scoped lang="scss">
.faq {
  margin-top: 15%;
  background-color: #003B89;
  width: 100vw;
  position: relative;
  margin-left: -50vw;
  left: 50%;
  padding-bottom: 80px;

  &__section {
    border-color: #fff;
    margin: 64px 18%;

    @media screen and (max-width: 960px) {
      margin: 64px 55px;
    }

    @media screen and (max-width: 620px) {
      margin: 30px 24px;
    }
  }

  &__title {
    font-size: 72px;
    line-height: 90px;
    font-weight: 700;
    padding-top: 120px;

    @media only screen and (max-width: 600px) {
      font-size: 36px;
      line-height: 44px;
    }
  }

  &__header {
    font-size: 32px;
    line-height: 44px;
    border-color: #fff !important;

    @media only screen and (max-width: 600px) {
      font-size: 20px;
      line-height: 30px;
      font-weight: 700 !important;
    }
  }

  &__content {
    font-size: 20px;
    line-height: 30px;

    @media only screen and (max-width: 600px) {
      font-size: 16px;
      line-height: 24px;
    }
  }
}

::v-deep .theme--light.v-expansion-panels .v-expansion-panel {
  background-color: #003B89;
  color: #fff;
}

::v-deep .v-expansion-panels {
  border: 2px solid #A4BCFD;
  border-radius: 5px
}

::v-deep .theme--light.v-expansion-panels .v-expansion-panel-header .v-expansion-panel-header__icon .v-icon {
  color: #A4BCFD;
  font-size: 48px;

  @media only screen and (max-width: 600px) {
    font-size: 32px;
  }
}

::v-deep .theme--light.v-expansion-panels .v-expansion-panel:not(:first-child)::after {
  border-color: #A4BCFD;
}

.anchor {
  display: block;
  position: relative;
  top: -100px;
  visibility: hidden;
}
</style>