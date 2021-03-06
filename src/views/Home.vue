<template>
  <div class="fill-height" fluid>
    <v-row>
      <v-col cols="12">
        <v-layout>
          <v-flex>
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
          </v-flex>
          <v-flex>
            <v-img alt="landingPage" class="landingPic" src="../assets/landingPage.svg" />
          </v-flex>
        </v-layout>
      </v-col>
    </v-row>
  </div>
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
  width: 450px;
}
@media (max-width: 425px) {
  .fill-height {
    max-width: 100%;
  }
  .landing {
    margin-top: 15rem;
    font-size: 1.8rem;
  }
  .landingPic {
    margin-top: 2rem;
    margin-left: -8rem;
    margin-right: 0.1rem;
  }
}
@media (max-width: 767px) {
  .container {
    max-width: 100%;
  }
}
</style>
