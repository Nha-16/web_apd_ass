<template>
  <div>
    <div class="bgs">
      <div class="container">
        <v-row>
          <v-col class="left">
            <h2>{{ items.title }}</h2>
            <p>{{ items.subtitle }}</p>
          </v-col>
        </v-row>
      </div>
    </div>
    <div v-for="item in content" :key="item.title" class="content mt-4" >
      <v-container>
        <v-row>
          <v-col cols="12" sm="12" md="9" lg="9" xl="9">
            <h1>{{ item.title }}</h1>
            <hr class="mt-3" />
            <p class="mt-5">{{ item.subtitle }}</p>
            <ul v-for="lists in item.list" :key="lists">
              <li>{{ lists }}</li>
            </ul>
          </v-col>
          <Needhelp />
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import Needhelp from './Needhelp.vue'
export default {
  name: 'PersonalPage',
  data() {
    return {
      items: 
        {
          title: 'ACCOUNTS THAT GROW WITH YOU',
          subtitle:
            'Start saving today with a Savings account that makes earning interest and growing your wealth easy. Be one step closer to achieving your goals with a Savings Account that offers you freedom and flexibility.',
        },
      content: [
        {
          title: 'EARN MORE INTEREST WITH A SAVINGS ACCOUNT',
          subtitle:
            "Boost your savings with flexible accounts and competitive rates.Earn more on the money you save, plus get exclusive features. APD Bank's Savings Account is designed with flexibility where you can make deposits and withdrawals at any time without restriction on numbers of transaction.",
          list: [
            'USD and KHR currencies.',
            'Interest is calculated and acquired daily, paid monthly.',
            'Free Passbook with every account.',
            'Funds are available for withdrawal at any time.',
            'Unlimited withdrawals over the counter at no cost.',
            'nimum initial deposit and balance is KHR40,000 or USD10.',
            'Withholding Tax of 4% and 14% is applied on interest earned for residence and non-residence respectively.',
          ],
        },
      ],
    }
  },
  components: { Needhelp },
}
</script>

<style scoped>
hr {
  border: 3px solid #1976d2;
  width: 60px;
}
.left {
  /* height: auto; */
  margin-left: 66%;
  background-color: rgba(240, 248, 255, 0.555);
  padding: 40px 50px;
  text-align: justify;

  /* margin: 0auto; */
}
p {
  font-weight: 300px;
  font-size: 17px;
}
.bgs {
  background-image: url('../assets/images/personal.jpg');
  /* height: 500px; */
  background-size: cover;
}
@media screen and (max-width: 600px) {
  .left {
    margin: auto;
    background-color: rgba(255, 255, 255, 0.9) !important;
    text-align: start;
  }
  h2 {
    font-size: 20px;
    text-align: left;
  }
}
</style>
