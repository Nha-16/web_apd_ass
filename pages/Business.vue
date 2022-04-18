<template>
  <div>
    <div class="bgs">
      <div class="container">
        <v-row>
          <v-col class="left" v-for="data in datas" :key="data">
            <h2>{{ data.title }}</h2>
            <p>
              {{ data.subtitle }}
            </p>
          </v-col>
        </v-row>
      </div>
    </div>
    <div class="content mt-4">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            sm="12"
            md="9"
            lg="9"
            xl="9"
            v-for="content in contents"
            :key="content"
          >
            <h1>{{ content.title }}</h1>
            <hr class="mt-3" />
            <p class="mt-5">
              {{ content.subtitle }}
            </p>
            <ul>
              <li v-for="item in content.list" :key="item">{{ item }}</li>
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
  name: 'BusinessPage',
  data() {
    return {
      datas: [
        {
          title: 'YOUR STAFF PAID ACCURATELY AND ON TIME',
          subtitle:
            'Handing over your payroll is easier than you imagine with APD Bank. Focus on growing your business and say good-bye to time-consuming payroll management.',
        },
      ],
      contents: [
        {
          title: 'SIMPLIFIED PAYROLL SERVICE FOR EVERYONE',
          subtitle:
            "Payroll is a bulk payment of wages and salaries to the company's employees — usually by a credit to their Payroll Account. On the other hand, payroll service is developed to cut down the risk from carrying bulk physical cash for customers from places to places to pay to its employees. This would be a benefit to both the organization and their employees who work in the Kingdom of Cambodia.",
          list: [
            'Offered in Khmer Riel or US Dollars.',
            'Cost and time saving on payroll processing.',
            'Improve transparency in salary payments to employees.',
            'Risk reduction of carrying cash, counting error and counterfeit notes.',
            'Provide the customize options for salary payments to Payroll Account of the employees.',
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
.bgs {
  background-image: url('../assets/images/bnner.jpg');
  /* height: 500px; */
  background-size: cover;
}
h2 {
  font-size: 20px;
  text-align: left;
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
