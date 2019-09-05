<template>
  <v-app dark class="pixel-font">
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <img class="main-icon" src="@/assets/img/main-icon.png" height="32">
      <v-toolbar-title v-text="title" />

      <v-spacer />
      <!-- GitHub link -->
      <v-btn text icon color="white" v-on:click="goToGitHub">
        <i class="fab fa-github"></i>
      </v-btn>
      <!-- Reload button:href -->
      <v-btn text icon color="white" v-on:click="reloadNoCache">
        <i class="fas fa-sync-alt"></i>
      </v-btn>
      <!-- <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn> -->
    </v-app-bar>
    <!-- Main content -->
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <!-- <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019 Harapeco Map</span>
    </v-footer> -->
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'fas fa-map-marked-alt',
          title: 'Map',
          to: '/'
        },
        {
          icon: 'far fa-edit',
          title: 'How to edit map',
          to: '/howtoedit'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Harapeco Map',
      links: [
        {url: '', name:'GitHub'}
      ],
    }
  },
  methods: {
    reloadNoCache: function() {
      // キャッシュを無視してサーバーからリロード
      window.location.reload(true);
    },
    goToGitHub: function() {
      window.open('https://github.com/tkdev01/harapeco-map');
    },
  }
}
</script>
<style lang="scss" scoped>
@font-face {
	font-family: PixelMplus12-Regular;
	src: url('../assets/font/PixelMplus12-Regular.ttf') format("opentype");
}
.pixel-font {
    font-family: PixelMplus12-Regular;
}
.main-icon {
  margin-right: .5em;
}
</style>