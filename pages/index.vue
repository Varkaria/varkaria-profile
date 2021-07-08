<template>
  <v-container>
    <h1 class="v-heading text-center text-h3 text-sm-h1">Hi Varkaria</h1>
    <h4 class="font-weight-light text-h4 text-sm-h4 text-center mb-8">Pavaresorn Malai</h4>
    <v-row justify="center">
        <v-btn text large v-for="(item, i) in items" 
        :key="i" :href="item.to">{{ item.title }}</v-btn>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "osu!",
          to: "https://osu.ppy.sh/users/4211179"
        },
        {
          title: "Twitter",
          to: "https://twitter.com/varkarism"
        },
        {
          title: "Steam",
          to: "https://steamcommunity.com/id/SoyuraSan/"
        },
        {
          title: "Youtube",
          to: "https://www.youtube.com/channel/UCRx2HJWCqqY6MNbsR4y3SLQ"
        },
        {
          title: "Twitch",
          to: "https://twitch.tv/varkaria"
        },
        {
          title: "Facebook",
          to: "https://www.facebook.com/"
        },
        {
          title: "Github",
          to: "https://github.com/Varkaria"
        }
      ],
    };
  }
};
</script>
