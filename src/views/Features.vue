<template>
  <div class="Features">
    <v-container class="fill-height" fluid style="min-height: 434px">
      <v-fade-transition>
        <v-row>
          <v-col cols="6" sm="4">
            <v-card flat>
              <v-card-title class="title">Time Tracking </v-card-title>
              <v-card-text
                >Easy time time tracking and monitoring process for day day to day
                activities and tasks.</v-card-text
              >
            </v-card>
          </v-col>

          <v-col cols="6" sm="4">
            <v-card flat>
              <v-card-title class="title"> Report Sheet </v-card-title>
              <v-card-text
                >Keep accountability for time spent on out report page.</v-card-text
              >
            </v-card>
          </v-col>

          <v-col cols="6" sm="4">
            <v-card flat>
              <v-card-title class="title"> Productive Management </v-card-title>
              <v-card-text
                >Assign and receive task, make task to suit your comfort.</v-card-text
              >
            </v-card>
          </v-col>
          <v-col cols="6" sm="4">
            <v-card flat>
              <v-card-title class="title"> Calendar </v-card-title>
              <v-card-text
                >Stay up to date and manage event and tasks on Pace Calendar.</v-card-text
              >
            </v-card>
          </v-col>
          <v-col cols="6" sm="4">
            <v-card flat>
              <v-card-title class="title"> Billing Management </v-card-title>
              <v-card-text
                >Cost your billing on hourly employee work hour basics.</v-card-text
              >
            </v-card>
          </v-col>
          <v-col cols="6" sm="4">
            <v-card flat>
              <v-card-title class="title"> Todo-List </v-card-title>
              <v-card-text
                >Break down tasks into smaller bit to improve work
                Productivity</v-card-text
              >
            </v-card>
          </v-col>
        </v-row>
      </v-fade-transition>
      <v-container class="fill-height" fluid>
        <v-row style="margin-top: 3rem">
          <v-col cols="6">
            <v-layout justify-center>
              <v-flex>
                <div id="dashboard">Admin Dashboard</div>
                <p style="color: #7171e0">
                  Dashboard with bar-chart showing the most active employee and report of
                  daily activity
                </p>
                <ul>
                  <li>Bar-chart</li>
                  <li>Dashboard Timer & Name of employee</li>
                  <li>View Active employee</li>
                </ul>
              </v-flex>
            </v-layout>
          </v-col>
          <v-img alt="featureImage" class="dashboard" src="../assets/dashboard.png" />
        </v-row>
      </v-container>
    </v-container>
  </div>
</template>
<style>
#dashboard {
  font-size: 2rem;
}
.dashboard {
  width: 500px;
}
</style>
