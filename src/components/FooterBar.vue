<template>
  <v-footer app absolute padless>
    <v-card class="flex" flat tile>
      <v-card-title class="primary">
        <strong class="subheading">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 black--text text-center" style="height: 21rem">
        {{ new Date().getFullYear() }} — <strong>AkanWealth</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
