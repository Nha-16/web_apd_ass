<template>
  <div>
    <div class="bgs">
      <div class="container">
        <v-row>
          <v-col v-for="text in texts" :key="text.title" class="left">
            <h2>{{ text.title }}</h2>
            <p>
              {{ text.subtitle }}
            </p>
          </v-col>
        </v-row>
      </div>
    </div>
    <div class="content mt-4">
      <v-container>
        <v-row>
          <v-col cols="12" sm="12" md="9" lg="9" xl="9">
            <h1>AN ALTERNATIVE TO THE BANKING OF THE PAST</h1>
            <hr class="mt-3" />
            <p v-for="list in lists" :key="list" class="mt-5">
              {{ list }}
            </p>
          </v-col>
          <v-col cols="12" sm="12" md="3" lg="3" xl="3">
            <div class="center">
              <div class="c-theme-font">
                <h3>FOSTERING BRIGHT IDEAS THROUGH DIVERSITY AND INCLUSION</h3>
              </div>
            </div>
          </v-col>
        </v-row>
        <v-row>
          <v-col
            v-for="item in abt"
            :key="item.title"
            class="mt-4"
            cols="12"
            sm="12"
            md="4"
            lg="4"
            xl="4"
          >
            <div class="abt">
              <v-img :src="item.src" contain width="70px" />
              <h2 class="mt-4 mb-4">{{ item.title }}</h2>
              <p>{{ item.subtitle }}</p>
            </div>
          </v-col>
        </v-row>
        <h2 class="mt-8">MANAGEMENT TEAM</h2>
        <hr class="mt-3" />
      </v-container>
    </div>
    <v-main class="mt-5">
      <div class="block"></div>
      <div class="block">
        <v-container>
          <v-row>
            <v-col
              v-for="item in items"
              :key="item.id"
              class="d-flex child-flex"
              cols="12"
              sm="4"
            >
              <v-card flat tile class="mx-auto">
                <v-img
                  :src="item.src"
                  aspect-ratio="1"
                  class="grey lighten-2"
                ></v-img>
                <v-card-text class="text--primary text-center">
                  <div class="title">{{ item.name }}</div>
                  <p>{{ item.title }}</p>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </v-main>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  data() {
    return {
      items: [
        {
          id: 1,
          src: require('../assets/images/team1.jpg'),
          name: 'Thoo Kim Seng',
          title: 'Chief Executie Officer',
        },
        {
          id: 2,
          src: require('../assets/images/team2.jpg'),
          name: 'Chua Thiam Yew',
          title: 'Deputy Chief Executive Officer',
        },
        {
          id: 3,
          src: require('../assets/images/team3.jpg'),
          name: 'Svay Pisal',
          title: 'Head of Operations',
        },
        {
          id: 4,
          src: require('../assets/images/team4.jpg'),
          name: 'Ung Kongheng',
          title: 'Head of Strategy and Planning',
        },
        {
          id: 5,
          src: require('../assets/images/team5.jpg'),
          name: 'Chheu Tech',
          title: 'Head of Finance and Treasury',
        },
        {
          id: 6,
          src: require('../assets/images/team2.jpg'),
          name: 'Chheu Tech',
          title: 'Head of Finance and Treasury',
        },
      ],
      texts: [
        {
          title: "WE'RE BUILDING A BANK, TOGETHER",
          subtitle:
            "While money's important, it's not what matters most. It's the connections we share and the relationships we build. And that's why we do things a little differently. By solving your problems,treating you fairly and being totally transparent, we believe we can make banking better.",
        },
      ],
      banner: [
        {
          src: require('../assets/images/abu.jpg'),
        },
      ],
      lists: [
        'Across our personal and business accounts, we help customers improve their financial health, give them more control, and connect people seamlessly across the world. Asia-Pacific Development Bank Plc. (APD Bank) was established in 2016 as a specialized bank with its registered office in the capital of Cambodia, Phnom Penh and upgraded to Commercial Bank in 2019.',
      ],
      abt: [
        {
          id: 1,
          src: require('../assets/images/crown-solid.svg'),
          title: '5 YEARS',
          subtitle:
            'APD Bank was established in 2016 as a specialized and later converted into a commercial bank in 2019.',
        },
        {
          id: 2,
          src: require('../assets/images/circle-dollar-to-slot-solid.svg'),
          title: '$77.5 MIL OF CAPITAL',
          subtitle:
            'With a registered capital of $77.5 million USD all deposits and customers are protected.',
        },
        {
          id: 3,
          src: require('../assets/images/money-check-dollar-solid.svg'),
          title: '$176.3 MIL OF ASSETS',
          subtitle:
            'APD has $176.3 million USD in terms of total assets as per the 2020 annual report.',
        },
      ],
    }
  },
}
</script>

<style scoped>
hr {
  border: 3px solid #1976d2;
  border-radius: 5px;
  width: 65px;
}
.c-theme-font {
  text-align: center;
  background-color: #144c9d !important;
  padding: 40px;
  color: white;
}
.center {
  text-align: center;
}
.left {
  /* height: auto; */
  margin-left: 66%;
  background-color: rgba(240, 248, 255, 0.555);
  padding: 40px 50px;
  text-align: justify;
  /* margin: 0auto; */
}
.bgs {
  background-image: url('../assets/images/bnner.jpg');
  /* height: 500px; */
  background-size: cover;
}
@media screen and (max-width: 600px) {
  .left {
    margin: auto;
    background-color: rgba(255, 255, 255, 0.9) !important;
    text-align: start;
  }
  .abt {
    text-align: center;
    margin: auto;
  }
  h2.mt-4.mb-4 {
    text-align: center;
  }
  h2 {
    font-size: 20px;
    text-align: left;
  }
  .v-image.v-responsive.theme--light {
    margin: auto;
  }
}
</style>
