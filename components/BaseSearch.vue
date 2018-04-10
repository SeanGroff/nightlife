<template>
  <v-form>
    <v-text-field
      v-model="city"
      append-icon="search"
      hint="e.g. Los Angeles"
      label="Search"
      loading="accent"
      placeholder="city" />
  </v-form>
</template>

<script>
export default {
  data() {
    return {
      city: ''
    }
  }
}
</script>
