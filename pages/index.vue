<template>
  <v-container>
    <jumbotron />
    <v-card :v-if="bars && bars.length">
      <v-container
        fluid
        style="min-height: 0;"
        grid-list-lg
      >
        <v-layout
          row
          wrap
          justify-center
        >
          <v-flex
            v-for="bar in bars"
            :key="bar.id"
            xs12
            md6
          >
            <bar-card :bar="bar" />
          </v-flex>
        </v-layout>
      </v-container>
    </v-card>
  </v-container>
</template>

<script>
import BarCard from '@/components/BarCard'
import Jumbotron from '@/components/Jumbotron'

export default {
  components: {
    BarCard,
    Jumbotron
  },
  data() {
    return {
      bars: [
        {
          id: '123lhsdfgkjh2a',
          name: 'Cool Tavern',
          description:
            'A cool place to have a drink, enjoy live music, and eat great food.',
          image: 'http://via.placeholder.com/350x350',
          attendees: 2,
          url: 'https://www.google.com'
        },
        {
          id: '123lzxcvfgkj234',
          name: 'Johns Pub',
          description:
            'Live music, local bands, local beers, come enjoy the local scene!',
          image: 'http://via.placeholder.com/350x350',
          attendees: 0,
          url: 'https://www.yahoo.com'
        }
      ]
    }
  }
}
</script>
