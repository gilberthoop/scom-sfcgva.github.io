<template>
  <v-container class="team">
    <div
      id="teams"
      class="anchor">
    </div>

    <div class="team__header mb-10">
      <div class="team__header-title mb-7">
        Our Teams
      </div>

      <div class="team__header-subtitle mb-12 mb-md-10">
        Each team plays a vital role in how SFC Communications should function. The teams are as follow:
      </div>
    </div>

    <div class="team__section d-flex flex-column flex-md-row justify-space-between">
      <div class="mr-0 mr-md-4">
        <v-card
          v-for="(team, index) in teamA"
          :key="index"
          class="team__section d-flex flex-column mb-9 pa-6 mx-2"
          color="#003B89"
          :height="$vuetify.breakpoint.smAndDown ? 'auto' :'190px'"
          :max-width="$vuetify.breakpoint.smAndDown ? '100%' : '625px'"
        >
          <div class="team__section-title mb-2">
            {{ team.name }}
          </div>

          <div class="team__section-b-description mb-2">
            {{ team.description }}
          </div>
        </v-card>
      </div>

      <div class="ml-0 ml-md-4">
        <v-card
          v-for="(team, index) in teamB"
          :key="index"
          class="team__section d-flex flex-column mb-9 pa-8"
          color="#003B89"
          :height="$vuetify.breakpoint.smAndDown ? 'auto' :'190px'"
          :max-width="$vuetify.breakpoint.smAndDown ? '100%' : '625px'"
        >
          <div class="team__section-title mb-2">
            {{ team.name }}
          </div>

          <div class="team__section-b-description mb-2">
            {{ team.description }}
          </div>
        </v-card>
      </div>
    </div>
  </v-container>
</template>

<script>
export default ({
  name: 'Teams',

  data () {
    return {
      teamA: [
        {
          name: 'Multimedia',
          description: 'We create graphic designs and videos to promote SFC events, such as Prayer Assembly, Christian Life Program (CLP), Covenant Orientation Weekend (COW), etc.'
        },{
          name: 'Social Media Communications',
          description: 'We capture, post and share Instagram and Facebok posts and stories, as well as announce SFC events on any level: national, regional, chapter.'
        }
      ],
      teamB: [
        {
          name: 'Events',
          description: 'We coordinate with event heads to ensure that events run smoothly in front of the audience and behind the scenes.'
        },
        {
          name: 'Documentation & Archives',
          description: 'We capture and store multimedia resources, such as photos and videos for Multimedia and Social Media Communications to use and promote.'
        }
      ]
    }
  }
})
</script>

<style scoped lang="scss">
.team {
  margin: 10% 0 30%;

  @media screen and (max-width: 960px) {
    margin-bottom: 0;
  }

  &__header-title {
    font-size: 72px;
    font-weight: 700;
    line-height: 90px;

    @media only screen and (max-width: 600px) {
      font-size: 36px;
      line-height: 44px;
    }
  }

  &__header-subtitle {
    font-size: 24px;
    line-height: 32px;
    max-width: 600px;

    @media only screen and (max-width: 960px) {
      max-width: 100%;
    }
  }

  &__section {
    color: #fff;
    border-radius: 14px;
    height: 270px;

    @media (max-width: 1200px) {
      height: 295px;
    }

    @media only screen and (max-width: 1000px) {
      height: 300px;
    }

    @media only screen and (max-width: 960px) {
      height: auto;
    }

    &-title {
      font-size: 36px;
      font-weight: 500;
      line-height: 44px;

      @media only screen and (max-width: 600px) {
        font-size: 24px;
        line-height: 32px;
      }
    }

    &-description {
      font-size: 20px;
      line-height: 30px;
    }
  }
}

.anchor {
  display: block;
  position: relative;
  top: -150px;
  visibility: hidden;
}
</style>