<template>
  <v-app dark>
    <!-- HEADER -->
    <div>
      <v-container>
        <v-toolbar flat class="mainHeader" elevation="2">
          <v-toolbar-title>
            <v-img
              :src="require('../assets/images/logo.png')"
              contain
              max-width="200px"
              link="/Home"
            />
          </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items class="hidden-xs-only">
            <v-btn class="btnn" text to="/">Home</v-btn>
            <v-btn text to="/Personal">Personal</v-btn>
            <v-btn text to="/Business">Business</v-btn>
            <v-btn text to="/careers">Career</v-btn>
            <v-btn text to="/Promotions">Promotion</v-btn>
            <v-btn text to="/About">About</v-btn>
          </v-toolbar-items>
          <div class="hidden-sm-and-up">
            <v-menu offset-y>
              <template v-slot:activator="{ on }">
                <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
              </template>
              <v-list class="responsiveMenu">
                <v-list-item>
                  <v-list-item-title>
                    <router-link to="/">Home</router-link>
                  </v-list-item-title>
                </v-list-item>
                <v-list-item>
                  <v-list-item-title
                    ><router-link to="/Personal"
                      >Personal</router-link
                    ></v-list-item-title
                  >
                </v-list-item>
                <v-list-item>
                  <v-list-item-title
                    ><router-link to="/Business"
                      >Business</router-link
                    ></v-list-item-title
                  >
                </v-list-item>
                <v-list-item>
                  <v-list-item-title
                    ><router-link to="/careers"
                      >Career</router-link
                    ></v-list-item-title
                  >
                </v-list-item>
                <v-list-item>
                  <v-list-item-title
                    ><router-link to="/Promotions"
                      >Promotion</router-link
                    ></v-list-item-title
                  >
                </v-list-item>
                <v-list-item>
                  <v-list-item-title
                    ><router-link to="/About"
                      >About</router-link
                    ></v-list-item-title
                  >
                </v-list-item>
              </v-list>
            </v-menu>
          </div>
        </v-toolbar>
      </v-container>
    </div>

    <!-- Main Page -->
    <v-main>
      <Nuxt />
    </v-main>

    <Footer />
  </v-app>
</template>

<script>
import Footer from '../pages/Footer.vue'
// import Footer from '../pages/Footer.vue'
export default {
  name: 'DefaultLayout',
  data() {
    return {
      dialog: false,
      clipped: false,
      drawer: false,
      fixed: false,
      menu: [
        {
          icon: 'home',
          title: 'Home',
          link: '/inspire',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Personal',
          link: '/Personal',
        },
        {
          icon: 'warning',
          title: 'Business',
          link: '/Business',
        },
        {
          icon: 'warning',
          title: 'Digital',
          link: '/careers',
        },
        {
          icon: 'warning',
          title: 'Promotions',
          link: '/Promotions',
        },
        {
          icon: 'warning',
          title: 'About',
          link: '/About',
        },
      ],
      nav: [
        {
          icon: 'home',
          text: 'Home',
          title: 'Back to Home page',
          active: true,
        },
        {
          icon: 'info',
          text: 'About',
          title: 'About this demo',
          active: false,
        },
        {
          icon: 'assignment_turned_in',
          text: 'Todos',
          title: 'Some stuff that needs doing',
          active: false,
        },
        {
          icon: 'email',
          text: 'Contact',
          title: 'Our Contact info',
          active: false,
        },
      ],
      // miniVariant: false,
      // right: true,
      // rightDrawer: false,
      // title: 'Vuetify.js',
    }
  },
  components: { Footer },
}
</script>

<style scoped>
.cursor {
  cursor: pointer;
}
a.v-btn--active {
  color: #2d609b !important;
}
.btnn :hover {
  color: black !important;
}
</style>
