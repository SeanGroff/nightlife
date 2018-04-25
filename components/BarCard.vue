<template>
  <v-card
    color="cyan darken-2"
    class="white--text"
    @click="$emit('card-click', bar.url)"
  >
    <v-container
      fluid
      grid-list-lg
    >
      <v-layout row>
        <v-flex xs7>
          <div>
            <div class="headline">{{ bar.name }}</div>
            <div>{{ bar.description }}</div>
            <v-card-actions>
              <v-btn
                color="success"
                style="{marginRight: auto}"
                @click="$emit('is-going-click')"
              >
                Not Going
              </v-btn>
              <v-badge
                overlap
                color="orange"
              >
                <span slot="badge">
                  {{ bar.attendees }}
                </span>
                <v-icon
                  medium
                  color="white lighten-1"
                >
                  face
                </v-icon>
              </v-badge>
            </v-card-actions>
          </div>
        </v-flex>
        <v-flex xs5>
          <v-card-media
            :src="bar.image"
            height="125px"
            contain
          />
        </v-flex>
      </v-layout>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name: 'BarCard',
  props: {
    bar: {
      type: Object,
      required: true,
      default() {
        return {
          id: '',
          name: '',
          description: '',
          image: '',
          attendees: 0,
          url: ''
        }
      }
    }
  }
}
</script>
