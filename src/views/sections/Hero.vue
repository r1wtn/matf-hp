<template>
  <section id="hero">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/soybean_3d.png')"
      class="white--text"
      gradient="to right, rgba(5, 11, 31, .6), rgba(5, 11, 31, .7)"
    >
      <v-container class="fill-height px-4 py-12">
        <v-responsive
          class="d-flex align-center"
          height="100%"
          max-width="700"
          width="100%"
        >
          <base-heading title="数理が拓く新しい農業" />

          <!-- <base-body>
            MATF (Mathematical Agronomy Task-Force)
            は「数理農学」の研究を促進する有志の研究会です。
          </base-body> -->

          <base-subtitle :title="title" size="subtitle-1" />

          <v-btn class="my-5" x-large rounded color="indigo"
            >MATFのミッション</v-btn
          >
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
export default {
  name: "SectionHero",

  provide: {
    theme: { isDark: true },
  },

  data() {
    return {
      title:
        "MATF (Mathematical Agronomy Task-Force)は「数理農学」の研究を促進する有志の研究会です。",
    };
  },

  computed: {
    minHeight() {
      const height = this.$vuetify.breakpoint.mdAndUp ? "100vh" : "80vh";

      return `calc(${height} - ${this.$vuetify.application.top}px)`;
    },
  },
};
</script>
