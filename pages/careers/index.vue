<template>
  <div>
    <div class="bgs">
      <div class="container">
        <v-row>
          <v-col class="left">
            <h2>START YOUR APD CAREER</h2>
            <p class="mt-4">
              What is it like working at APD Bank? We’re reinventing banking and
              building a workplace that's different from the average bank. We
              see great value in our team and invest in the long-term
              professional success.
            </p>
          </v-col>
        </v-row>
      </div>
    </div>
    <div class="content mt-4">
      <v-container>
        <v-row>
          <v-col cols="12" sm="12" md="9" lg="9" xl="9">
            <h1>HOW TO APPLY</h1>
            <hr class="mt-3" />
            <h4 class="mt-5">
              INTERESTED CANDIDATES ARE INVITED TO SUBMIT THEIR COVER LETTERS
              AND CVS (WITH EXPECTED SALARY) TO HR@APDBANK.COM.KH. ** FEMALE
              CANDIDATES ARE STRONGLY ENCOURAGED TO APPLY. **
            </h4>
            <v-btn class="btn mt-4">APPLY NOW</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="job_career mt-4">
      <v-container>
        <v-row>
          <v-col
            v-for="item in items"
            :key="item"
            cols="12"
            sm="12"
            md="4"
            lg="4"
            xl="4"
          >
            <v-card class="mx-auto" max-width="344" outlined>
              <v-list-item three-line>
                <v-list-item-content>
                  <div class="text-overline text-center mb-4">
                    <v-chip class="ma-2" outlined color="primary">
                      Phnom Penh
                    </v-chip>
                    <v-chip class="ma-2" outlined color="error">
                      Full-Time
                    </v-chip>
                  </div>
                  <v-list-item-title class="text-h7 mb-1">
                    {{ item.title }}
                  </v-list-item-title>
                  <v-list-item-subtitle
                    >{{ item.department }}
                  </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-card-actions>
                <v-btn
                  outlined
                  rounded
                  text
                  @click="$router.push('/careers/' + item.slug)"
                >
                  More Detail
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="text-center mt-4 mb-4">
      <v-pagination v-model="page" :length="4" circle></v-pagination>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CareerPage',
  data() {
    return {
      page: 1,
      items: [
        {
          id: '1',
          slug: 'customer-service-officer',
          title: 'CUSTOMER SERVICE OFFICER',
          department: 'OPERATIONS DEPARTMENT',
        },
        {
          id: '2',
          slug: 'assistant-it-security-analyst-manager',
          title: 'ASSISTANT IT SECURITY ANALYST MANAGER',
          department: 'IT DEPARTMENT',
        },
        {
          id: '3',
          slug: 'assistant-it-security-compliance-manager',
          title: 'ASSISTANT IT SECURITY COMPLIANCE MANAGER',
          department: 'IT DEPARTMENT',
        },
        {
          id: '4',
          slug: 'senior-officer-digital-marketing',
          title: 'SENIOR OFFICER, DIGITAL MARKETING',
          department: 'DIGITAL MARKETING DEPARTMENT',
        },
        {
          id: '5',
          slug: 'operations-officer',
          title: 'OPERATIONS OFFICER',
          department: 'OPERATIONS DEPARTMENT',
        },
        {
          id: '6',
          slug: 'chief-cashier',
          title: 'CHIEF CASHIER',
          department: 'OPERATIONS DEPARTMENT',
        },
      ],
    }
  },
}
</script>

<style scoped>
hr {
  border: 3px solid #1976d2;
  width: 60px;
}
.center {
  text-align: center;
}
.btn {
  padding: 10px 20px 9px 20px;
  color: #ffff;
  border-radius: 0 !important;
  background: #144c9d !important;
}
.v-sheet.v-card {
  border-color: #1976d2;
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
  background-image: url('../../assets/images/career.jpg');
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
