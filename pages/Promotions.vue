<template>
  <v-container grid-list-xs>
    <h1>Promotions</h1>
    <hr />
    <div class="mt-5">
      <v-row>
        <v-col v-for="item in items" :key="item.id" xs12 md6>
          <v-card class="mx-auto" max-width="350">
            <v-img class="white--text align-end" height="250px" :src="item.src">
            </v-img>
            <v-card-subtitle class="p-2">
              <h2>{{ item.title }}</h2>
            </v-card-subtitle>
            <v-card-text class="text--primary">
              <div>
                {{ item.discription }}
              </div>
            </v-card-text>
            <v-card-actions>
              <v-btn icon>
                <v-icon>mdi-heart</v-icon>
              </v-btn>
              <v-btn icon>
                <v-icon>mdi-bookmark</v-icon>
              </v-btn>
              <v-btn icon>
                <v-icon>mdi-share-variant</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <div class="center">
        <div class="c-theme-font">
          <i>
            <v-icon large color="blue darken-2"> mdi-message-text </v-icon>
          </i>
          <h1>NEED HELP?</h1>
          <p>Talk with a specialist and apply over the phone.</p>
          <v-btn color="primary" dark> Call 023 211 888 </v-btn>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'PromotionPage',
  data: () => ({
    items: [
      {
        id: 1,
        src: 'https://apdbank.com.kh/pic/promo/Promotion_july_21_EN.jpg',
        title: 'WE REWARD FOR SAVINGS',
        discription:
          'YOU ARE REWARDED WITH MANY REWARDS AFTER PLACING A MINIMUM DEPOSIT OF USD70,000 WITH APD BANK TODAY.',
      },
      {
        id: 2,
        src: 'https://apdbank.com.kh/pic/promo/photo_2021-05-12_11-43-07.jpg',
        title: 'IPHONES AWAIT',
        discription:
          'YOU ARE REWARDED WITH MANY REWARDS AFTER PLACING A MINIMUM DEPOSIT OF USD70000 WITH APD BANK TODAY.',
      },
      {
        id: 3,
        src: 'https://apdbank.com.kh/pic/promo/photo_2021-02-18_09-19-52.jpg',
        title: 'FLY FOR FREE (EXPIRED)',
        discription:
          'OPEN A TERM DEPOSIT ACCOUNT WITH US TODAY TO GET FREE HELICOPTER RIDE FROM APD BANK.',
      },
      {
        id: 4,
        src: 'https://apdbank.com.kh/pic/promo/20210225_Prosperity_Promotion_for_Website-09.jpg',
        title: 'PROSPERITY CAMPAIGN ',
        discription:
          'YOU ARE REWARDED WITH MANY REWARDS AFTER PLACING A MINIMUM DEPOSIT OF USD70000 WITH APD BANK TODAY.',
      },
      {
        id: 5,
        src: 'https://apdbank.com.kh/pic/promo/Promotion_july_21_EN.jpg',
        title: 'WE REWARD FOR SAVINGS',
        discription:
          'YOU ARE REWARDED WITH MANY REWARDS AFTER PLACING A MINIMUM DEPOSIT OF USD70,000 WITH APD BANK TODAY.',
      },
      {
        id: 6,
        src: 'https://apdbank.com.kh/pic/promo/photo_2021-03-23_16-32-52.jpg',
        title: 'IPHONES AWAIT',
        discription:
          'YOU ARE REWARDED WITH MANY REWARDS AFTER PLACING A MINIMUM DEPOSIT OF USD70000 WITH APD BANK TODAY.',
      },
    ],
  }),
}
</script>

<style scoped>
hr {
  border: 3px solid #1976d2;
  /* border-radius: 5px; */
  width: 65px;
}
.for-mg {
  margin-top: 20px;
}
.center {
  margin-top: 35px;
  margin-bottom: 25px;
  text-align: center;
}
</style>
