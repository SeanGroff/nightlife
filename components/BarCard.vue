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
              <v-layout row>
                <v-flex
                  d-flex
                  justify-space-between
                >
                  <v-btn
                    color="success"
                    @click="$emit('is-going-click')"
                  >
                    Not Going
                  </v-btn>
                  <v-badge>
                    <span slot="badge">{{ bar.attendees }}</span>
                    <div>Going</div>
                  </v-badge>
                </v-flex>
              </v-layout>
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
