<template>
  <v-card>
    <v-tabs v-model="timerType">
      <v-tab v-for="tab in tabTitles" :key="tab"></v-tab>
    </v-tabs>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      timerType: 0,
      tabsTitles: ["Pomodoro", "Short Break", "Long Break"]
    };
  }
};
</script>
