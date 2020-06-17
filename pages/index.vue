<template>
  <v-container fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm12 md6>
        <div class="text-right mx-auto br-1">
          <p class="display-3 font-weight-medium">
            Zach Baird
          </p>
          <p class="text--secondary display-1 font-weight-regular mb-0">
            Fullstack Web Developer
          </p>
        </div>
      </v-flex>
      <v-flex>
        <div class="d-none d-sm-block text--secondary headline ml-8 pl-2 py-4 font-weight-light flex-column" style="border-left: 1px solid #ccc;">
          <p>
            Hello, welcome to my site.
          </p>
          <p>
            Want to see
            <v-btn text small color="primary" to="/projects" style="padding: 5px;">
              projects
            </v-btn>
            ?
          </p>
          <p>
            Want to see
            <v-btn text small color="primary" to="/skills" style="padding: 5px;">skills</v-btn>
            ?
          </p>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  components: {}
}
</script>

<style scoped>
.ml-3 p {
  display: block;
}
</style>
