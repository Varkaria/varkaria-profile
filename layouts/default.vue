<template>
  <v-app dark>
    <v-app-bar fixed hide-on-scroll app flat color="transparent">
      <v-tabs centered class="ml-n9" color="grey darken-1">
        <v-tab v-for="(item, i) in items" :key="i" router exact :to="item.to">
          {{ item.title }}
        </v-tab>
      </v-tabs>
    </v-app-bar>
    <v-main>
      <v-container fill-height fluid>
        <v-slide-y-transition mode="out-in">
          <Nuxt />
        </v-slide-y-transition>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Home",
          to: "/",
        },
        {
          title: "About",
          to: "/about",
        },
        {
          title: "Projects",
          to: "/projects",
        },
        {
          title: "Skills",
          to: "/skills",
        }
      ],
    };
  },
};
</script>


<style>
#app {
  background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url(~assets/background.jpg)
    no-repeat center center fixed !important;
  background-size: cover;
}
</style>