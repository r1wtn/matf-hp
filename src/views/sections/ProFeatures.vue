<template>
  <base-section id="pro-features">
    <v-img
      :src="require('@/assets/logo.svg')"
      class="mx-auto mb-8"
      max-width="128"
    />

    <base-section-heading title="Feature Comparison">
      Get the PRO version of <strong>Daedal</strong> and level up your theme<br />with
      additional components, pages, and Free updates.
    </base-section-heading>

    <v-container>
      <v-row align="center" justify="center">
        <v-col cols="12" md="7">
          <v-simple-table>
            <thead>
              <tr>
                <th />
                <th class="body-1 font-weight-bold text-center">
                  What's in the Demo?
                </th>
                <th class="body-1 font-weight-bold text-center">
                  What's in the PRO version?
                </th>
              </tr>
            </thead>

            <tbody class="body-1">
              <tr v-for="([name, one, two], i) in features" :key="i">
                <td v-text="name" />

                <td class="text-center font-weight-bold">
                  <template v-if="typeof one === 'boolean'">
                    <v-icon :color="one ? 'success' : 'error'">
                      mdi-{{ one ? "check" : "close" }}
                    </v-icon>
                  </template>

                  <template v-else>
                    {{ one }}
                  </template>
                </td>

                <td class="text-center font-weight-bold">
                  <template v-if="typeof two === 'boolean'">
                    <v-icon :color="two ? 'success' : 'error'">
                      mdi-{{ two ? "check" : "close" }}
                    </v-icon>
                  </template>

                  <template v-else>
                    {{ two }}
                  </template>
                </td>
              </tr>
            </tbody>
          </v-simple-table>
        </v-col>

        <v-col cols="12" md="5">
          <v-card elevation="16" class="mb-12">
            <base-img
              max-width="100%"
              src="https://cdn.vuetifyjs.com/images/themes/daedal/daedal-hero.png"
            />
          </v-card>

          <div class="text-center">
            <base-btn
              :tile="false"
              color="primary"
              href="https://store.vuetifyjs.com/product/daedal-responsive-multi-purpose-theme-pro?ref=vtyd-pro-page-features"
              rounded
            >
              Buy Pro Now

              <v-icon right>
                mdi-rocket
              </v-icon>
            </base-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
export default {
  name: "SectionProChart",

  data: () => ({
    features: [
      ["Components", 23, "40+"],
      ["Example Pages", 3, 10],
      ["Bugfixes and Issues", true, true],
      ["Vue CLI Support", true, true],
      ["News, Project, and Pricing Pages", false, true],
      ["6 Months Free Updates", false, true],
      ["Price", "Free", "$60"],
    ],
  }),
};
</script>
