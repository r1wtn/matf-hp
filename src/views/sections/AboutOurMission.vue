<template>
  <base-section id="about-our-mission">
    <base-section-heading
      color="grey lighten-2"
      title="Mission"
      size="display-3"
      weight="black"
    />

    <v-container>
      <v-row>
        <v-col v-for="card in cards" :key="card.title" cols="12" md="4">
          <base-info-card v-bind="card" />
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
export default {
  name: "SectionAboutOurMission",

  data: () => ({
    cards: [
      {
        title: "Grow your Revenue",
        subtitle: "Best Productivity",
        text:
          "Similique sunt in culpa qui officia deserunt mollitia animi, id est laborut dolorum fuga.harum quidem rerum facilis estexpedita distinctio.",
        callout: "01",
      },
      {
        title: "Affordable Prices",
        subtitle: "Special Offers",
        text:
          "Similique sunt in culpa qui officia deserunt mollitia animi, id est laborut dolorum fuga.harum quidem rerum facilis estexpedita distinctio.",
        callout: "02",
      },
      {
        title: "Target Setting",
        subtitle: "Income Flow",
        text:
          "Similique sunt in culpa qui officia deserunt mollitia animi, id est laborut dolorum fuga.harum quidem rerum facilis estexpedita distinctio.",
        callout: "03",
      },
    ],
  }),
};
</script>
