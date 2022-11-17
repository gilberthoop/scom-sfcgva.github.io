<template>
  <v-app-bar
      app
      color="rgba(31, 143, 226, 0.9)"
      elevation="0"
      :height="$vuetify.breakpoint.smAndDown ? '70' : '108'"
      class="app-bar px-0 px-sm-5 px-md-16"
    >
      <div class="d-none d-md-flex align-center pl-16">
        <div
          v-for="(link, index) in links"
          :key="index"
        >
          <a
            class="app-bar__links px-10"
            :href="link.route"
          >
            {{ link.name }}
          </a>
        </div>
      </div>

      <v-dialog 
        v-model="dialog"
        transition="scroll-y-transition"
        hide-overlay
        fullscreen
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            width="50"
            min-width="50"
            height="70"
            min-height="70"
            color="rgba(255, 255, 255, 0)"
            class="app-bar__hamburger d-block d-md-none"
            outlined
            v-bind="attrs"
            v-on="on"
            @click.native="!!dialog"
          >
            <v-icon
              v-if="!dialog"
              large
              color="white"
            >
              mdi-menu
            </v-icon>
            <v-icon
              v-else
              large
              color="white"
            >
              x
            </v-icon>
          </v-btn>
        </template>

        <v-list class="app-bar__links-list">
          <v-list-item
            v-for="(link, index) in links"
            :key="index"
          >
            <a
              class="app-bar__links px-0 px-sm-5"
              :href="link.route"
            >
              {{ link.name }}
            </a>
          </v-list-item>
        </v-list>
      </v-dialog>
  </v-app-bar>
</template>

<script>
export default({
  name: 'AppMenu',

  data () {
    return {
      links: [
        { name: 'SCOM', route: '#about' },
        { name: 'Why we have SCOM', route: '#why-scom' },
        { name: 'Our Teams', route: '#teams' },
        { name: 'Fun Facts', route: '#trivia' },
        { name: 'FAQ', route: '#faq' }
      ]
    }
  }
})
</script>

<style scoped lang="scss">
.app-bar {
  font-size: 20px !important;
  font-family: "Outfit", sans-serif !important;
  font-weight: medium;
  backdrop-filter: blur(10px);

  &__links {
    text-decoration: none;
    color: #fff;
  }

  &__links-list {
    background-color: #003B89 !important;
  }

  &__hamburger {
    position: relative;
    float: right;
  }
}

::v-deep .v-dialog--fullscreen {
  background-color: #003B89;
  top: 70px;
  font-family: "Outfit", sans-serif !important;
  font-size: 30px;
  line-height: 90px;
  font-weight: 500;

  @media only screen and (min-width: 600px) and (max-width: 960px) {
    font-size: 50px;
    line-height: 150px;
  }
}
</style>