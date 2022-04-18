<template>
  <div class="heroBlock">
    <v-carousel cycle hide-delimiters>
      <v-carousel-item class="sakmerl"
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row class="title fill-height hidden-xs-only" align="center" justify="center">{{ item.title }}</v-row>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  data() {
    return {
      items: [
        {
          src: require("../assets/images/bg.jpg"),
          title: "We are creative"
        },
        {
          src: require("../assets/images/home_01.jpg"),
          title: "We are hard worker"
        },
        {
          src: require("../assets/images/home_01.jpg"),
          title: "We are professional"
        }
      ]
    };
  }
};
</script>
<style scoped>
.heroBlock {
  position: relative;

  /* .v-window {
    @media only screen and (max-width: 599px) {
      height: 220px !important;
    }
  } */

  /* .v-image__image {
    &:before {
      content: '';
      background: rgba(0, 0, 0, 0.3);
      position: absolute;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      z-index: 1;
    }
  }

  .title {
    color: $white;
    position: relative;
    z-index: 2;
    font: 300 50px/1.6 $primary-font !important;
  } */
}
.sakmerl{
  background-size: cover; 
}
</style>