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
          :link="item.to"
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
        <a :href="resume.to" target="_blank" style="color: inherit; text-decoration: none;">
          <v-list-item>
            <v-list-item-action>
              <v-icon class="primary--text">
                {{ resume.icon }}
              </v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title v-text="resume.title" />
            </v-list-item-content>
          </v-list-item>
        </a>
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
      <nuxt-link style="text-decoration: none; color: inherit;" to="/">
        <v-toolbar-title v-text="title" />
      </nuxt-link>
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
          mdi-github
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
          icon: 'mdi-card-bulleted',
          title: 'Skills',
          to: '/skills'
        },
        {
          icon: 'mdi-ballot',
          title: 'Projects',
          to: '/projects'
        }
      ],
      resume: {
        icon: 'mdi-smart-card',
        title: 'Resume',
        to: 'https://zachbaird.me/ZacharyBairdResume.pdf'
      },
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
