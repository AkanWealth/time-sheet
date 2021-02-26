<template>
  <v-container class="fill-height" fluid>
    <v-row>
      <v-col cols="6">
        <div class="landing">Trace your time at your own pace</div>
        <p>Spend less time making the right and informed decisions</p>
        <v-btn
          color="rgb(51,94,234)
"
          dark
          x-large
          to="/login"
          class="text-decoration-none"
        >
          Login
          <i class="fas fa-angle-double-right"></i>
        </v-btn>
        <v-btn class="landing-btn-2" color="#FF6584" dark x-large> Learn More</v-btn>
      </v-col>

      <v-col cols="6">
        <v-img alt="landingPage" class="landingPic" src="../assets/landingPage.svg" />
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
}
p {
  color: grey;
}
.landing-btn-1 {
  color: #0000ff;
}
.landing-btn-2 {
  margin-left: 1rem;
  padding: 20rem;
}
.landingPic {
  width: 400px;
}
</style>
