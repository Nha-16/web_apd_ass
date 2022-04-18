<template>
  <v-col cols="12" sm="12" md="3" lg="3" xl="3">
            <div class="center">
              <div class="c-theme-font">
                <i>
                  <v-icon large color="blue darken-2">
                    mdi-message-text
                  </v-icon>
                </i>
                <h1>NEED HELP?</h1>
                <p>Talk with a specialist and apply over the phone.</p>
                <v-btn color="primary" dark> Call 023 211 888 </v-btn>
              </div>
            </div>
          </v-col>
</template>

<script>
export default {
name:"NeedPage"
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
