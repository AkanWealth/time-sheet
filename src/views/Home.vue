<template>
  <v-container fluid fill-height>
    <v-row>
      <v-col cols="12" md="4">
        <!-- <v-layout> -->
        <v-flex>
          <div class="landing">Trace your time at your own pace</div>
          <p>Spend less time making the right and informed decisions</p>
          <v-btn
            style="margin-left: 2rem; margin-top: 1rem"
            color="#335eea"
            dark
            x-large
            to="/login"
            class="text-decoration-none"
            id="loginBtn"
          >
            Login
            <i class="fas fa-angle-double-right"></i>
          </v-btn>
          <v-btn
            style="margin-left: 1rem; margin-top: 1rem"
            color="#FF6584"
            to="/register"
            class="text-decoration-none"
            dark
            outlined
            x-large
            id="getStarted"
          >
            Get Started</v-btn
          >
        </v-flex>
        <!-- <v-flex> -->
      </v-col>
      <v-col cols="6" xs12 sm8 md4 lg4>
        <v-img alt="landingPage" id="landingPic" src="../assets/landingPage.svg" />
        <!-- </v-flex>
        </v-layout> -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
.landing {
  color: #ff6584;
  font-size: 2.3rem;
  margin-top: 5rem;
}
p {
  color: grey;
}
#landingPic {
  width: 400px;
  /* float: right; */
  margin-top: 5rem;
  margin-left: 8rem;
}
#loginBtn {
  border-bottom-color: #ff6584;
}
</style>
