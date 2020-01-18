<template>
  <v-container>
    <div class="skills-container">
      <p class="font-weight-semibold headline">
        Skills
      </p>
      <p class="font-weight-light mb-0">
        Front-end
      </p>
      <div class="skills">
        <div class="front-end-markup-and-styling col-xs-12 col-md-6">
          <div class="language">
            <v-icon color="orange">
              mdi-language-html5
            </v-icon>
            <span>HTML</span>
          </div>
          <div class="language">
            <v-icon color="blue">
              mdi-language-css3
            </v-icon>
            <span>CSS</span>
          </div>
          <div class="language">
            <v-icon color="pink">
              mdi-sass
            </v-icon>
            <span>SASS</span>
          </div>
          <div class="language">
            <v-icon color="purple">
              mdi-bootstrap
            </v-icon>
            <span>Bootstrap</span>
          </div>
        </div>
        <div class="js-and-friends col-xs-12 col-sm-6 col-md-6">
          <div class="language">
            <v-icon color="yellow darken-1">
              mdi-language-javascript
            </v-icon>
            <span>JavaScript</span>
          </div>
          <div class="language">
            <v-icon color="green">
              mdi-vuejs
            </v-icon>
            <span>Vue.js</span>
          </div>
          <div class="language">
            <v-icon color="teal">
              mdi-nuxt
            </v-icon>
            <span>Nuxt.js</span>
          </div>
          <div class="language">
            <v-icon color="blue">
              mdi-vuetify
            </v-icon>
            <span>Vuetify.js</span>
          </div>
          <div class="language">
            <v-icon color="purple lighten-1">
              mdi-react
            </v-icon>
            <span>React.js (& Redux)</span>
          </div>
        </div>
        <p class="font-weight-light mb-0 mt-2 col-12 pl-0 mb-0 pb-0">
          Back-end
        </p>
        <div class="back-end col-12 pt-0">
          <div class="dotnet col-xs-12 col-sm-6 col-md-6 pl-0">
            <div class="language">
              <v-icon color="purple">
                mdi-language-csharp
              </v-icon>
              <span>C#</span>
            </div>
            <div class="language">
              <v-icon color="purple">
                mdi-dot-net
              </v-icon>
              <span>.NET & .NET Core</span>
            </div>
          </div>
          <div class="django col-xs-12 col-sm-6 col-md-6">
            <div class="language">
              <v-icon color="green">
                mdi-language-python-text
              </v-icon>
              <span>Python (& Django)</span>
            </div>
          </div>
          <div class="ruby col-xs-12 col-sm-6 col-md-6 pl-0">
            <div class="language">
              <v-icon color="red">
                mdi-ruby
              </v-icon>
              <span>Ruby</span>
            </div>
          </div>
        </div>
        <p class="font-weight-light mb-0 mt-2 col-12 pl-0 mb-0 pb-0">
          DevOps
        </p>
        <div class="devops">
          <div class="platform col-xs-12 col-sm-4 col-md-4">
            <v-icon color="orange">
              mdi-linux
            </v-icon>
            <span>Linux</span>
          </div>
          <div class="platform col-xs-12 col-sm-4 col-md-4">
            <v-icon color="blue">
              mdi-windows
            </v-icon>
            <span>Windows</span>
          </div>
          <div class="platform col-xs-12 col-sm-4 col-md-4">
            <v-icon color="red">
              mdi-git
            </v-icon>
            <span>Git</span>
          </div>
          <div class="platform col-xs-12 col-sm-4 col-md-4">
            <v-icon color="blue">
              mdi-azure
            </v-icon>
            <span>Azure (& Azure DevOps)</span>
          </div>
        </div>
      </div>
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

<style scoped>
.skills-container {
  max-width: 650px;
  width: 70%;
  margin: auto;
}

.skills {
  display: flex;
  align-content: space-between;
  flex-wrap: wrap;
}

.back-end {
  display: flex;
  flex-wrap: wrap;
  align-items: space-between;
}

.devops {
  display: flex;
  align-content: space-around;
  flex-wrap: wrap;
}

.language {
  display: flex;
  margin-bottom: 5px;
}

.platform {
  padding-top: 10px;
}

.language span {
  margin-left: 5px;
}

@media(max-width: 650px) {
  .back-end {
    flex-direction: column;
  }
  .back-end div {
    padding-left: 0;
  }
}
</style>
