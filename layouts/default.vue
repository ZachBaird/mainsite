<template>
  <v-app dadrk>
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
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-switch
        label="Theme"
        v-model="$vuetify.theme.dark"
        :color="$vuetify.theme.themes.dark.info"
        class="switch-center ma-0"
        inset
        hide-details
      >
      </v-switch>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019</span>
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
          title: 'Main',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      title: 'Zach Baird'
    }
  }
}
</script>

<style scoped>
.switch-center {
  display: flex;
  justify-content: center;
}

.switch-center .v-input__slot {
  margin-bottom: 0 !important;
}

.switch-center .v-messages {
  min-height: 0 !important;
}
</style>
