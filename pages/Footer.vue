<template>
  <v-footer color="primary vColor pt-4 mt-4" padless>
    <v-row justify="center" no-gutters>
      <v-col cols="12" sm="12" md="3" lg="3" xl="3">
        <v-img
          :src="require('../assets/images/logo.png')"
          contain
          max-width="200px"
          link="/Home"
        />
      </v-col>
      <v-col cols="12" sm="12" md="9" lg="9" xl="9" class="btn-menu">
        <v-btn
          v-for="link in links"
          :key="link"
          color="#1976d2"
          text
          rounded
          class="my-2"
        >
          {{ link }}
        </v-btn>
      </v-col>
      <v-col class="primarys lighten-2 py-4 text-center white--text" cols="12">
        <h6>© 2016 - 2022 Asia-Pacific Development Bank Plc. </h6>
      </v-col>
    </v-row>
  </v-footer>
</template>
<script>
export default {
  name: 'FooterPage',
  data: () => ({
    links: ['Home', 'Personal', 'Business', 'Career', 'Promotion', 'About'],
  }),
}
</script>
<style scoped>
footer.v-footer {
  padding: 0;
}
.vColor {
  background: whitesmoke !important;
}
.v-image.v-responsive.theme--light {
  margin: auto;
}
.btn-menu {
  text-align: center;
}
.primarys {
  background: #0765a3 !important;
}
</style>
