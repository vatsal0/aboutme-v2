<template>
  <v-app dark>
    <v-navigation-drawer
      :mini-variant="miniVariant"
      fixed
      app
    >
      
      <v-list>
        <v-list-item
          to="/"
          router
          exact
        >
          <v-list-item-action>
            <v-avatar
              size="24px"
            >
              <img
                src="headshot.jpeg"
              >
            </v-avatar>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="'About Me'" />
          </v-list-item-content>
        </v-list-item>
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
      fixed
      app
    >
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      items: [
        {
          icon: 'mdi-medal',
          title: 'Experience',
          to: '/#experience'
        },
        {
          icon: 'mdi-school',
          title: 'Education',
          to: '/#education'
        },
        {
          icon: 'mdi-flask',
          title: 'Projects',
          to: '/#projects'
        }
      ],
      miniVariant: false,
      title: 'Vatsal Baherwani'
    }
  }
}
</script>
