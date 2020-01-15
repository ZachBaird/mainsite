<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
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
            <v-icon class="primary--text">
              {{ item.icon }}
            </v-icon>
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
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
      />
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-switch
        v-model="$vuetify.theme.dark"
        label="Theme"
        class="primary--text switch-center ma-0"
        color="primary"
        inset
        hide-details
      />
    </v-app-bar>
    <v-content mx-4 mb-4>
      <nuxt />
    </v-content>
    <v-footer
      :fixed="fixed"
    >
      <span>&copy; 2020</span>
      <v-spacer />
      <a href="https://github.com/ZachBaird" target="_blank" class="mr-1">
        <v-icon color="purple">
          mdi-github-circle
        </v-icon>
      </a>
      <a href="https://www.linkedin.com/in/zachary-baird-b7a9a9138?trk=people-guest_profile-result-card_result-card_full-click" target="_blank">
        <v-icon color="blue">
          mdi-linkedin
        </v-icon>
      </a>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      success: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-human-greeting',
          title: 'About',
          to: '/about'
        },
        {
          icon: 'mdi-ballot',
          title: 'Projects',
          to: '/projects'
        },
        {
          icon: 'mdi-lightbulb',
          title: 'Inspire',
          to: '/inspire'
        },
        {
          icon: 'mdi-contact-mail-outline',
          title: 'Resume',
          to: '/ZacharyBairdResume.pdf'
        }
      ],
      title: 'Zach Baird'
    }
  }
}
</script>

<style scoped>
footer a {
  text-decoration: none;
}
</style>
