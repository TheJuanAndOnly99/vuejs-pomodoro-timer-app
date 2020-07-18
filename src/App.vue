<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row>
          <v-col sm="6" offset-sm="3">
            <Pomodoro :dialog="dialog" />
            <v-btn @click="dialog = true" absolute top right dark small color="secondary">
              <v-icon left>mdi-cog-outline</v-icon>Settings
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Pomodoro from "./components/Pomodoro";

export default {
  name: "App",

  components: {
    Pomodoro
  },

  data() {
    return {
      dialog: false
    };
  }
};
</script>
