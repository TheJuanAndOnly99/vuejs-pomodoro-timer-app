<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row>
          <v-col sm="6" offset-sm="3">
            <Pomodoro :dialog="dialog" :closeDialog="closeDialog" />
          </v-col>
          <v-btn @click="dialog = true" absolute top right dark small color="secondary">
            <v-icon left>mdi-cog-outline</v-icon>Settings
          </v-btn>
          <v-switch
            v-model="switch1"
            @change="changeTheme"
            inset
            absolute
            top
            right
            dark
            small
            color="black"
          >
            <template v-slot:label>
              <v-icon right>mdi-brightness-6</v-icon>
            </template>
          </v-switch>
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
  props: {
    switch1: {
      type: Boolean,
      required: true
    }
  },
  data() {
    return {
      dialog: false
    };
  },
  methods: {
    closeDialog() {
      this.dialog = false;
    },
    changeTheme() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    }
  }
};
</script>
