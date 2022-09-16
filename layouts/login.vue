<template>
  <v-app>
    <v-main>
      <v-row class="fill-height ma-0">
        <v-col class="primary d-flex justify-center align-center"
          ><Picture :src="img" max-height="500" max-width="500"
        /></v-col>
        <v-col class="d-flex justify-center align-center" cols="5"
          ><router-view></router-view>
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
import team_up from "~/static/img/team_up.png";
export default {
  data() {
    return {
      img: team_up,
    };
  },
};
</script>

<style></style>
