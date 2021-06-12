<template>
  <div class="Pricing">
    <h2 id="pricing" style="color: #ff6584">Pricing</h2>
    <div style="font-size: 2.2rem; text-align: center">
      Optimized for businesses of all sizes.
    </div>
    <div style="color: #7171e0; text-align: center">
      Flexible monthly pricing for project and teams of all sizes. Get billing in your
      local currency.
    </div>
    <v-layout class="container" justify-space-around>
      <v-card outlined width="300" color="#000000c7 ">
        <v-card-title style="color: #ff6584; font-size: 1.7rem">Free</v-card-title>
        <v-card-subtitle style="color: #ffffff">#0 / monthly</v-card-subtitle>
        <v-btn
          style="width: 100%"
          class="text-decoration-none"
          to="/"
          dark
          color="#7171e0"
          >Get Started</v-btn
        >
        <v-card-title style="color: #ffffff">Features</v-card-title>
        <v-card-text style="color: #ffffff; font-size: 1rem">
          <ul>
            <li>Time Reminder</li>
            <li>Workspace for 3 staff</li>
            <li>Limited Todo List</li>
            <li>Limited Request</li>
          </ul>
        </v-card-text>
      </v-card>
      <v-card outlined width="300" style="margin-left: 2rem">
        <v-card-title style="color: #ff6584; font-size: 1.7rem">Basic</v-card-title>
        <v-card-subtitle>#12,000 / monthly</v-card-subtitle>
        <v-btn
          style="width: 100%"
          class="text-decoration-none"
          to="/"
          dark
          color="#ff6584
"
          >Get Started</v-btn
        >
        <v-card-title>Features</v-card-title>
        <v-card-text style="color: grey; font-size: 1rem">
          <ul>
            <li>Time Reminder</li>
            <li>Workspace for 7 staff</li>
            <li>Todo List</li>
            <li>Request</li>
          </ul>
        </v-card-text>
      </v-card>
      <v-card outlined width="300" style="margin-left: 2rem">
        <v-card-title style="color: #ff6584; font-size: 1.7rem">Premium</v-card-title>
        <v-card-subtitle>#32,000 / monthly</v-card-subtitle>
        <v-btn
          style="width: 100%"
          class="text-decoration-none"
          to="/"
          dark
          color="#ff6584
"
          >Get Started</v-btn
        >
        <v-card-title class="container">Features</v-card-title>
        <v-card-text style="color: grey; font-size: 1rem">
          <ul>
            <li>Time Reminder</li>
            <li>Unlimited staff</li>
            <li>Unlimited Todo List</li>
            <li>Request</li>
          </ul>
        </v-card-text>
      </v-card>
    </v-layout>
  </div>
</template>
<style scoped>
#pricing {
  text-align: center;
}
</style>
