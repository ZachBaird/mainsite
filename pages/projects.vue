<template>
  <v-container>
    <div class="projects">
      <p class="font-weight-regular display-1">
        The following are either finished or active projects
      </p>
      <v-container class="my-5">
        <v-layout row wrap justify-space-around justify-space-between>
          <v-flex xs12 sm6 md4 class="mx-2 my-5">
            <v-card flat>
              <v-responsive class="pt-4">
                <v-img src="v.png" width="100" />
              </v-responsive>
              <v-card-text>
                <div class="subheading">
                  Project Title
                </div>
                <div class="info--text">
                  Project Description
                </div>
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6 md4 class="mx-2 my-5">
            <v-card flat>
              <v-responsive class="pt-4">
                <v-img src="v.png" width="100" />
              </v-responsive>
              <v-card-text>
                <div class="subheading">
                  Project Title
                </div>
                <div class="info--text">
                  Project Description
                </div>
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6 md4 class="mx-2 my-5">
            <v-card flat>
              <v-responsive class="pt-4">
                <v-img src="v.png" width="100" />
              </v-responsive>
              <v-card-text>
                <div class="subheading">
                  Project Title
                </div>
                <div class="info--text">
                  Project Description
                </div>
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6 md4 class="mx-2 my-5">
            <v-card flat>
              <v-responsive class="pt-4">
                <v-img src="v.png" width="100" />
              </v-responsive>
              <v-card-text>
                <div class="subheading">
                  Project Title
                </div>
                <div class="info--text">
                  Project Description
                </div>
              </v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </v-container>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>
