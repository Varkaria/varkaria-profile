<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="4">
      <v-card>
        <v-card-title class="headline">
          About me
        </v-card-title>
        <v-card-text>
          <p>
            Hi My name is Pavaresorn Malai (Few) aka Varkaria. 
            I'm 16 from Thailand. nice to meet you everyone!!
          </p>
          <p>
            I love to code, playing games such as Apex Legends, Quaver and
            osu!, I'm Interest in Rhythm Arcade Backend, Programing and anything what i want to do
          </p>
          <v-list flat class="mb-8">
            <v-subheader>My current working</v-subheader>
            <v-list-item-group>
              <v-list-item v-for="(item, i) in items" :key="i" :href="item.link">
                <v-list-item-icon>
                  <v-icon v-text="item.icon"></v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title v-text="item.text"></v-list-item-title>
                  <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
          <div class="text-xs-right">
            <small>&mdash; Varkaria (Pavaresorn Malai)</small>
          </div>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/">Home</v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      items: [
        { 
        text: 'osu!Akatsuki', 
        subtitle: 'an osu! private server with relax and big active community (Frontend Developer)', 
        icon: 'mdi-account-supervisor-circle',
        link: 'https://akatsuki.pw/' 
        },
        { 
        text: 'guweb', 
        subtitle: 'a frontend continue in gulag-web project from modern stack, gulag 🧶', 
        icon: 'mdi-github',
        link: 'https://github.com/Varkaria/guweb' 
        },
        { 
        text: 'oturna', 
        subtitle: 'a tournament frontend, management for click the circles tournament. osu!', 
        icon: 'mdi-github',
        link: '' 
        },
        { 
        text: 'OMTHPL2021', 
        subtitle: 'osu!mania thailand tournament with pro league system (Designer, Developer)', 
        icon: 'mdi-basketball',
        link: 'https://omthpl.varkaria.tech/'
        },
        { 
        text: 'TEC Season 1', 
        subtitle: 'osu!standard thailand tournament with technical system (Designer) ', 
        icon: 'mdi-basketball',
        link: 'https://osu.ppy.sh/community/forums/topics/1237294' 
        }
      ],
    }),
  }
</script>