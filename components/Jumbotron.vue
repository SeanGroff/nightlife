<template>
  <v-jumbotron
    fluid
    color="primary">
    <v-container>
      <v-layout align-center>
        <v-flex text-xs-center>
          <h1 class="display-3">Going Out Tonight?</h1>
          <p class="subheading">
            Let your friends know where you're going out tonight.
            Need help figuring out where to go?
            Use the city search to see where people are going!
          </p>
          <search class="search" />
        </v-flex>
      </v-layout>
    </v-container>
  </v-jumbotron>
</template>

<script>
import Search from '@/components/Search'

export default {
  components: {
    Search
  }
}
</script>

<style scoped>
.search {
  width: 300px;
  margin: 0 auto;
}
</style>
