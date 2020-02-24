<template>
  <v-row justify="center">
    <v-col cols="12" sm="4" align="center">
      <v-avatar size="200" class="elevation-8">
        <img src="@/assets/kammradt.png" alt="Kammradt" />
      </v-avatar>
    </v-col>
    <v-col cols="12" sm="8" :align="align">
      <v-card height="200" outlined color="clean">
        <span class="darker--text main-title">Kammradt</span>
        <br />
        <span class="darker--text main-subtitle">💻 Software Developer 🖥️</span>
        <v-card-actions>
          <v-row>
            <v-col cols="12" :align="align">
              <v-btn
                class="mr-3"
                v-for="btn in buttons"
                :key="btn.icon"
                color="primary"
                large
                depressed
                :href="btn.link"
                target="_blank"
              >
                <v-icon dark v-text="btn.icon" />
              </v-btn>
            </v-col>
          </v-row>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    buttons: [
      { icon: "mdi-git", link: "https://github.com/kammradt" },
      { icon: "mdi-linkedin", link: "https://linkedin.com/in/vinicius-kammradt" }
    ]
  }),
  computed: {
    align() {
      return this.$vuetify.breakpoint.mdAndUp ? "left" : "center";
    }
  }
};
</script>


<style>
.main-title {
  font-size: 4rem;
}
.main-subtitle {
  font-size: 1.2rem;
}
</style>