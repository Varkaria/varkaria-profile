<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="4">
      <v-card>
        <v-card-title class="headline">
          Skills
        </v-card-title>
        <v-card-text>
          <v-list flat class="mb-8" disabled>
            <v-list-item-group>
              <v-list-item
                v-for="(item, i) in skills"
                :key="i"
                :href="item.percent"
              >
                <v-list-item-content>
                  <v-list-item-title v-text="item.text"></v-list-item-title>
                  <v-list-item-subtitle>
                    <v-progress-linear
                      :color="item.color + ' lighten-2'"
                      buffer-value="100"
                      :value="item.percent"
                      height="10"
                      class="mt-2"
                    ></v-progress-linear>
                  </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    skills: [
      {
        text: "HTML",
        color: 'blue',
        percent: 100
      },
      {
        text: "CSS",
        color: 'blue',
        percent: 80
      },
      {
        text: "Javascript",
        color: 'yellow',
        percent: 70
      },
      {
        text: "Vue (Nuxt.js)",
        color: 'green',
        percent: 80
      },
      {
        text: "Python",
        color: 'yellow',
        percent: 90
      },
      {
        text: "Frontend",
        color: 'green',
        percent: 90
      },
      {
        text: "Backend",
        color: 'yellow',
        percent: 80
      }
    ]
  })
};
</script>
