<template>
  <div class="projects">
    <v-container class="project">
      <h1 class="subheading grey--text mb-1">
        Projects
      </h1>
      <v-img
        :src="projects[page-1].image"
        :lazy-src="projects[page-1].image"
        width="600px"
        height="175px"
        alt="Project Screenshot"
        class="mx-auto"
        contain
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular indeterminate color="accent" />
          </v-row>
        </template>
      </v-img>
      <h2 class="title-section font-weight-regular text-center my-3">
        {{ projects[page-1].title }} | Status: {{ projects[page-1].status }}
      </h2>
      <div class="description-section">
        <p class="mt-3">
          {{ projects[page-1].description }}
        </p>
        <div style="display: inline;">
          Stack:
          <div
            v-for="stack in projects[page-1].tech"
            :key="stack.snackbar"
            style="display: inline;"
          >
            &nbsp;
            <v-tooltip color="accent" top>
              <template v-slot:activator="{ on }">
                <v-icon :color="stack.color" v-on="on">
                  {{ stack.img }}
                </v-icon>
              </template>
              <span>{{ stack.snackbar }}</span>
            </v-tooltip>
          </div>
        </div>
        <br>
        <v-btn
          :href="projects[page-1].url"
          target="_blank"
          outlined
          color="primary"
          class="mt-2"
        >
          See code
        </v-btn>
      </div>
    </v-container>
    <v-pagination
      v-model="page"
      color="primary"
      :length="5"
      class="mt-auto"
    />
  </div>
</template>

<script>
export default {
  data () {
    return {
      snackbarTimeout: 3000,
      page: 1,
      projects: [
        {
          image: 'mainsite.jpg',
          title: 'Main Site',
          status: 'Active',
          description: 'A main site built with Nuxt.js and statically generated.',
          url: 'https://github.com/ZachBaird/MainSiteRefresh',
          tech: [
            {
              snackbar: 'Nuxt.js',
              img: 'mdi-nuxt',
              color: 'teal'
            },
            {
              snackbar: 'Vuetify.js',
              img: 'mdi-vuetify',
              color: 'blue'
            }
          ]
        },
        {
          image: 'caesarcipher.jpg',
          title: 'CaesarCipher',
          status: 'Finished',
          description: 'A Ruby script that runs a CaesarCipher on a string of text.',
          url: 'https://github.com/ZachBaird/CaesarCipher',
          tech: [
            {
              snackbar: 'Ruby',
              img: 'mdi-ruby',
              color: 'red'
            }
          ]
        },
        {
          image: 'oreoweather.jpg',
          title: 'OreoWeather',
          status: 'On hold',
          description: 'A .Net Core weather application for my grandfather.',
          url: 'https://github.com/ZachBaird/OreoWeather',
          tech: [
            {
              snackbar: 'C# .Net Core',
              img: 'mdi-dot-net',
              color: 'purple'
            },
            {
              snackbar: 'Bootstrap',
              img: 'mdi-bootstrap',
              color: 'purple'
            }
          ]
        },
        {
          image: '',
          title: 'Python Automation',
          status: 'Backlog',

          description: 'A series of Python scripts that automate file manipulation, web scraping, and GUI tasks.',
          url: 'https://github.com/ZachBaird/Python_Automation',
          tech: [
            {
              snackbar: 'Python',
              img: 'mdi-language-python-text',
              color: 'green'
            }
          ]
        },
        {
          image: 'djangorealestate.jpg',
          title: 'Realestate app',
          status: 'Bugfix',

          description: 'A real estate application built with the Django framework.',
          url: 'https://github.com/ZachBaird/Real-Estate-App',
          tech: [
            {
              snackbar: 'Python',
              img: 'mdi-language-python-text',
              color: 'green'
            },
            {
              snackbar: 'Bootstrap',
              img: 'mdi-bootstrap',
              color: 'purple'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style>
.projects {
  display: flex;
  flex-direction: column;
  height: 95%;
}

.title-section {
  max-width: 600px;
  width: 70%;
  margin: auto;
  border-bottom: 1px solid #ccc;
}

.description-section {
  max-width: 600px;
  width: 70%;
  margin: auto;
}

i {
  cursor: pointer;
}
</style>
