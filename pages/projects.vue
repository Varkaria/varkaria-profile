<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="4">
      <v-card>
        <v-card-title class="headline">
          Projects
        </v-card-title>
          <v-card-text>
            <v-list flat class="mb-4">
            <v-subheader>Active</v-subheader>
            <v-list-item-group>
              <v-list-item v-for="(item, i) in active" :key="i" :href="item.link">
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
          <v-list flat class="mb-8" disabled>
            <v-subheader>Deprecated</v-subheader>
            <v-list-item-group>
              <v-list-item v-for="(item, i) in deprecated" :key="i" :href="item.link">
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
          </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      active: [
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
        text: 'bulma-hsl', 
        subtitle: 'a little framework for who want to customise color easier 👽', 
        icon: 'mdi-github',
        link: 'https://github.com/Varkaria/bulma-hsl' 
        },
        { 
        text: 'foobar2000-rpc-album', 
        subtitle: 'a discord rich presence for foobar2000 with album picture in status', 
        icon: 'mdi-github',
        link: 'https://github.com/Varkaria/foobar2000-rpc-album' 
        }
      ],
      deprecated: [
        { 
        text: 'osu!gakugulag', 
        subtitle: 'an osu! private server with gulag stack (before i joined gulag team)', 
        icon: 'mdi-account-supervisor-circle',
        link: '' 
        },
        { 
        text: 'osu!juyuri', 
        subtitle: 'an osu! private server thailand community', 
        icon: 'mdi-account-supervisor-circle',
        link: '' 
        },
        { 
        text: 'osu!lumilous', 
        subtitle: 'an osu! private server thailand community with Varkaria x Lumilous', 
        icon: 'mdi-account-supervisor-circle',
        link: '' 
        },
        { 
        text: 'osu!yeethailand', 
        subtitle: 'an first osu! private server i made it', 
        icon: 'mdi-account-supervisor-circle',
        link: '' 
        },
      ],
    }),
  }
</script>