<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm10
      md8
    >
      <div class="text-center">
        <v-card>
          <v-card-title class="headline">
           A developer who cares
          </v-card-title>
          <v-card-text>
            <p>text content</p>
          </v-card-text>
          <v-card-actions>
            <v-spacer />
            <v-btn
              color="primary"
              nuxt
              to="/inspire"
            >
              See today's inspiration
            </v-btn>
          </v-card-actions>
        </v-card>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>

export default {
  components: {}
}
</script>
