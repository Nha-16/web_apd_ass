<template>
  <div>
    <v-carousel cycle hide-delimiters>
      <v-carousel-item
        height="600"
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
      >
      </v-carousel-item>
    </v-carousel>
    <div v-for="item in content" :key="item">
      <v-container class="mt-4">
        <v-row>
          <v-col cols="12" sm="6" md="6" xs="6" xl="6">
            <v-img class="mt-6" height="400" :src="item.src"></v-img>
          </v-col>
          <v-col class="mt-8" cols="12" sm="6" md="6" xs="6" xl="6">
            <h1>{{ item.title }}</h1>
            <p class="mt-2">{{ item.des }}</p>
            <ul v-for="lists in item.list" :key="lists">
              <li>{{ lists }}</li>
            </ul>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      items: [
        {
          src: require('../assets/images/bg3.jpg'),
        },
        {
          src: require('../assets/images/bg1.jpg'),
        },
        {
          src: require('../assets/images/bg2.jpg'),
        },
      ],
      content: [
        {
          id: '1',
          title: 'DEPOSITS',
          src: require('../assets/images/home_01.jpg'),
          des: 'Managing your finance is an around-the-clock job. That’s why we make it possible for you to customize your account. Save your money when you choose the account features you need.',
          list: ['Current Accounts', 'Savings Accounts', 'Term Deposits'],
        },
        {
          id: '2',
          title: 'LOANS',
          src: require('../assets/images/home_02.jpg'),
          des: 'Give it a name and choose a house of your choice. You focus on the home, we’ll focus on the loan. With great loan rates, fast collateral assessment and an expert team, we’ll take care of the heavy lifting.',
          list: ['Home Loans', 'Term Loans', 'Overdraft'],
        },
        {
          id: '3',
          title: 'REMITTANCE',
          src: require('../assets/images/home_03.jpg'),
          des: 'Managing your finance is an around-the-clock job. That’s why we make it possible for you to customize your account. Save your money when you choose the account features you need.',
          list: ['Telegraphic Transfer', 'FAST Payment'],
        },
      ],
    }
  },
}
</script>

<style scoped>
.v-image.v-responsive.theme--light {
  border-radius: 0px 50px 0px 50px;
}
</style>
