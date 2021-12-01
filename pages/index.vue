<template>
  <nav id="navbar">
    <v-app-bar class="white" flat app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="font-weight-bold"
        ><router-link to="/" style="text-decoration: none" class="tekst"
          ><v-icon class="yt">mdi-youtube</v-icon>YouTube</router-link
        ></v-toolbar-title
      >
      <v-spacer></v-spacer>
      <v-text-field
        flat
        hide-details
        append-icon="mdi-magnify"
        placeholder="Search"
        outlined
        dense
        v-model="searchText"
        @click:append="search"
        class="hidden-sm-and-down"
      ></v-text-field><v-icon>mdi-microphone</v-icon>

      <v-spacer></v-spacer>
      <v-menu offsetY>
      </v-menu>

      <v-tooltip bottom>
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on"> <v-icon size="25">mdi-apps</v-icon></v-btn>
        </template>
        <span>YouTube apps</span>
      </v-tooltip>
      <v-tooltip bottom>
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on"> <v-icon size="25">mdi-dots-vertical</v-icon></v-btn>
        </template>
        <span>Settings</span>
      </v-tooltip>

      <v-menu offset-y left>
        <template v-slot:activator="{ on }">
          <v-btn small color="red" v-on="on" class="white--text suur" outlined>
            <v-icon>mdi-account</v-icon>Sign In
          </v-btn>
        </template>
      </v-menu>
    </v-app-bar>
    <div id="chips">
      <v-chip>All</v-chip>
      <v-chip>African bullfrogs</v-chip>
      <v-chip>Spiders</v-chip> 
      <v-chip>Aquariums</v-chip>
      <v-chip>Ambient music</v-chip>       
      <v-chip>Eating</v-chip>
      <v-chip>Chill-out music</v-chip>
      <v-chip>Deep house</v-chip>
      <v-chip>Live</v-chip>
      <v-chip>Music</v-chip>
      <v-chip>Fireplaces</v-chip>
      <v-chip>Terrestrial Animals</v-chip>
      <v-chip>Hamsters</v-chip>
    </div>
    <div class="content">
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190" alt=""> 
                <div class="time">3:13</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201">
                <div class="below">
                    <h2>Inimesed</h2>
                    <p class="username">Inimene</p>
                    <p>422 views &bull; 1 days ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=1" alt=""> 
                <div class="time">5:55</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=1">
                <div class="below">
                    <h2>Ahvid</h2>
                    <p class="username">Ahv</p>
                    <p>88 views &bull; 1 days ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=2" alt=""> 
                <div class="time">0:22</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=2">
                <div class="below">
                    <h2>Sead</h2>
                    <p class="username">Siga</p>
                    <p>666666 views &bull; 2 years ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=3" alt=""> 
                <div class="time">7:33</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=3">
                <div class="below">
                    <h2>Linnud</h2>
                    <p class="username">Lind</p>
                    <p>444 views &bull; 9 days ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=4" alt=""> 
                <div class="time">1:48</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=4">
                <div class="below">
                    <h2>Joon</h2>
                    <p class="username">Joons</p>
                    <p>666 views &bull; 15 days ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=5" alt=""> 
                <div class="time">30:22</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=5">
                <div class="below">
                    <h2>Teeme ära talgud</h2>
                    <p class="username">Eesti</p>
                    <p>32 views &bull; 7 years ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=6" alt=""> 
                <div class="time">3:55</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=6">
                <div class="below">
                    <h2>Uued pinalid</h2>
                    <p class="username">Dolores</p>
                    <p>53677 views &bull; 7 months ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
        <div class="vid">
            <div class="preview">
                <img src="https://picsum.photos/350/190?random=7" alt=""> 
                <div class="time">6:28</div>
                <div class="hovicons">
                    <v-icon>mdi-clock-outline</v-icon>
                    <v-icon>mdi-view-stream-outline</v-icon>
                </div>
            </div>
            <div class="inform">
                <div class="left">
                <img class="profile" src="https://picsum.photos/201?random=7">
                <div class="below">
                    <h2>Vroom Vroom</h2>
                    <p class="username">MumsCar</p>
                    <p>216892 views &bull; 3 years ago</p>

                    </div>
                </div>
                    <v-icon></v-icon>

                </div>
        </div>
    </div>

                         
    <v-navigation-drawer
      v-model="drawer"
      app
      :clipped="$route.name !== 'Watch'"
      :temporary="$route.name === 'Watch'"
      id="nav" class="navi"
    >
      <div tag="div" class="v-navigation-drawer__content" v-bar>
        <v-list dense nav class="py-0" tag="div">
          <v-divider class="hidden-lg-and-up"></v-divider>
          <div v-for="parentItem in items" :key="parentItem.header">
            <v-subheader
              v-if="parentItem.header"
              class="pl-3 py-4 subtitle-1 font-weight-bold text-uppercase"
              >{{ parentItem.header }}</v-subheader
            >
            <v-list-item
              v-for="(item, i) in parentItem.pages"
              :key="item.title"
              link
              class="mb-0"
              router
              :to="item.link"
              exact
              active-class="active-item"
            >
              <v-list-item-icon v-if="parentItem.header !== 'Subscriptions'">
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>
              <v-list-item-avatar v-else class="mr-5">
                <img
                  :src="`https://randomuser.me/api/portraits/men/${i}.jpg`"
                />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title class=" font-weight-medium subtitle-2">{{
                  item.title
                }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-divider class="mt-2 mb-2"></v-divider>
          </div>

          <span v-for="link in links" :key="link.text">
            <span v-if="link.text === 'Terms'" class="mb-2 d-block"> </span>
            <v-btn
              href
              router
              :to="link.link"
              text
              class="text-capitalize px-1"
              small
              >{{ link.text }}</v-btn
            >
          </span>
        </v-list>
      </div>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    items: [
      {
        header: null,
        pages: [
          { title: 'Home', link: '/', icon: 'mdi-home' },
          { title: 'Trending', link: '/trending', icon: 'mdi-fire' },
          {
            title: 'Subscriptions',
            link: '#s',
            icon: 'mdi-youtube-subscription'
          }
        ]
      },
      {
        header: null,
        pages: [
          {
            title: 'Library',
            link: '#l',
            icon: 'mdi-play-box-multiple'
          },
          {
            title: 'History',
            link: '/history',
            icon: 'mdi-history'
          }
        ]
      },
      {
        header:'Sign in ',
        pages: [
          {
            title:'SIGN IN',
            icon: 'mdi-account'
          }
        ]
      },
      {
        header: 'BEST OF YOUTUBE',
        pages: [
          {
            title:'Music',
            icon:'mdi-music'
          },
          {
            title:'Sports',
            icon: 'mdi-trophy-variant'
          },
          {
            title:'Gaming',
            icon: 'mdi-youtube-gaming'
          },
          {
            title:'News',
            icon: 'mdi-newspaper'
          },
          {
            title:'Live',
            icon: 'mdi-access-point'
          },
          {
            title:'360 Video',
            icon: 'mdi-domino-mask'
          }
        ]
      },
      {
        header: '',
        pages: [
          {
            title: 'Browse Channels',
            icon: 'mdi-plus-circle-outline'
          }
        ]
      },
      {
        header: 'MORE FROM YOUTUBE',
        pages: [
          {
            title: 'YouTube Premium',
            link: '#',
            icon: 'mdi-youtube'
          },
          {
            title: 'Live',
            link: '#',
            icon: 'mdi-access-point'
          }
        ]
      },
      {
        header: null,
        pages: [
          {
            title: 'Setting',
            link: '#',
            icon: 'mdi-cog'
          },
          {
            title: 'Report history',
            link: '#',
            icon: 'mdi-flag'
          },
          {
            title: 'Help',
            link: '#',
            icon: 'mdi-help-circle'
          },
          {
            title: 'Send feedback',
            link: '#',
            icon: 'mdi-message-alert'
          }
        ]
      }
    ],
    links: [
      { text: 'About', link: '#' },
      { text: 'Press', link: '#' },
      { text: 'Copyrignt', link: '#' },
      { text: 'Contact us', link: '#' },
      { text: 'Creators', link: '#' },
      { text: 'Advertise', link: '#' },
      { text: 'Developers', link: '#' },
      { text: 'Terms', link: '#' },
      { text: 'Privacy', link: '#' },
      { text: 'Policy & Safety', link: '#' },
      { text: 'Test new features', link: '#' }
    ],
    searchText: ''
  }),
  methods: {
    search() {
      if (!this.searchText) return
      this.$router.push({
        name: 'Search',
        query: { 'search-query': this.searchText }
      })
    }
  },
  mounted() {
    this.drawer = this.$vuetify.breakpoint.mdAndDown ? false : true
    this.drawer = this.$route.name === 'Watch' ? false : this.drawer
  }
}
</script>

<style lang="scss">
#navbar {
  font-family: 'Helvetica';
  .active-item {
    .v-list-item__icon {
      color: red !important;
    }
  }
  .v-navigation-drawer__border {
    width: 0 !important;
  }

  .vuebar-element {
    height: 250px;
    width: 100%;
    max-width: 500px;
    background: #dfe9fe;
  }

  .vb > .vb-dragger {
    z-index: 5;
    width: 10px;
    right: 0;
  }

  .vb > .vb-dragger > .vb-dragger-styler {
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-transform: rotate3d(0, 0, 0, 0);
    transform: rotate3d(0, 0, 0, 0);
    -webkit-transition: background-color 100ms ease-out, margin 100ms ease-out,
      height 100ms ease-out;
    transition: background-color 100ms ease-out, margin 100ms ease-out,
      height 100ms ease-out;

    margin: 5px 5px 5px 0;
    border-radius: 20px;
    height: calc(100% - 10px);
    display: block;
  }

  .v-navigation-drawer__content:hover .vb > .vb-dragger > .vb-dragger-styler {
    width: 10px;
    background-color: #e0e0e0;
  }

  .vb.vb-scrolling-phantom > .vb-dragger > .vb-dragger-styler {
    background-color: rgb(255, 255, 255);
    background-color: rgba(255, 255, 255, 0.3);
  }

  .vb > .vb-dragger:hover > .vb-dragger-styler {
    margin: 0px;
    width: 10px;
  }

  .vb.vb-dragging > .vb-dragger > .vb-dragger-styler {
    background-color: rgb(255, 255, 255);
    margin: 0px;
    height: 100%;
  }

  .vb.vb-dragging-phantom > .vb-dragger > .vb-dragger-styler {
    background-color: rgb(255, 255, 255);
  }
  .v-navigation-drawer {
    background-color: rgba(255, 255, 255, 0.3);
  }
  .tekst {
    color: white !important;
  }
  .yt{
    color: red !important;
  }
  .suur{
    height: 40px;
    color: blue !important;
  }
  .content {
    margin-top: 20px;
    margin-left: 20px;
    height: 80vh;
    padding: 3%;
    font-family: sans-serif;
    display: flex;
    flex-wrap: wrap;
  } 
  .vid {
    margin: 10px 10px 10px 10px;
    display: flex;
    flex-direction: column;
    width: fit-content;
    cursor: pointer;
  }
  .vid .inform {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
.below {
    display: inline;
    width: 96px;
    margin-left: 8px;
}
.vid .inform h2, .vid .inform p{
    margin: 0;
    padding: 0;
    white-space: nowrap;
}
.inform h2 {
    font-size: 16px;
    color: white;
    cursor: pointer;
}
.inform p{
    color: #aaaaaa;
}
p.username:hover{
    color: white;
}
.inform .v-icon {
    margin-top: 5px;
    color: #aaaaaa;
}
.preview .time {
    font-size: .8em;
    position: absolute;
    transform: translate(300px, -30px);
    padding: 3px;
    padding-right: 5px;
    border-radius: 3px;
    color: white;
    background-color: rgba(0, 0, 0, 0.733);
}
.hovicons {
    position: absolute;
    display: flex;
    flex-direction: column;
    transform: translate(310px, -190px);
    opacity: 0;
}
.vid:hover .hovicons {
    opacity: 1;
}
.hovicons .v-icon{
    color: white;
    background-color: rgba(0, 0, 0, 0.733);
    margin-bottom: 5px;
    padding: 4px 4px 4px 4px;
    border-radius: 3px;
}
.left {
    width: 160px;
}
.left .v-icon{
    margin-right: 20px;
}
img.profile {
    height: 2.2em;
    border-radius: 50%;
}
.left {
    display: flex;
    flex-direction: row;
    align-items: center;
}
}
</style>