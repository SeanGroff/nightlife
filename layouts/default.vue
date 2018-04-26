<template>
  <v-app dark>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile-content>
          <v-list-tile-title>{{ loggedIn ? 'Log out' : 'Login' }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar
      app
      dense
    >
      <v-toolbar-side-icon
        class="hidden-md-and-up"
        @click.stop="drawer = !drawer"
      />
      <v-toolbar-title>
        Night Life
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-items
        class="hidden-sm-and-down"
      >
        <v-btn
          flat
          color="info"
          href="http://localhost:3334/auth/google"
        >
          {{ loggedIn ? 'Log out' : 'Login' }}
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      loggedIn: false
    }
  }
}
</script>
