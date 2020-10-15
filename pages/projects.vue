<template>
  <div class="projects">
    <v-container class="project">
      <div
        v-for="project in projects"
        :key="project.title"
        class="mb-10"
      >
        <v-img
          v-show="project.image"
          :src="project.image"
          :lazy-src="project.image"
          height="175px"
          alt="Project Screenshot"
          class="mx-auto medium-screen-dimensions"
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
          {{ project.title }} | Status: {{ project.status }}
        </h2>
        <div class="description-section">
          <p class="mt-3">
            {{ project.description }}
          </p>
          <div class="project-tech">
            <div style="display: inline;">
              Stack:
              <div
                v-for="stack in project.tech"
                :key="stack.snackbar"
                style="display: inline; text-align: center;"
              >
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
              :href="project.url"
              target="_blank"
              outlined
              color="primary"
            >
              See code
            </v-btn>
            <v-btn
              v-show="project.liveSite"
              :href="project.liveUrl"
              target="_blank"
              outlined
              color="accent"
            >
              {{ project.liveText }}
            </v-btn>
          </div>
        </div>
        <v-divider class="mt-8" />
      </div>
    </v-container>
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
          status: 'Finished',
          description: 'A main site built with Nuxt.js and statically generated.',
          url: 'https://github.com/ZachBaird/mainsite',
          liveSite: true,
          liveUrl: '/',
          liveText: 'You\'re on it!',
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
          url: 'https://github.com/ZachBaird/caesarcipher',
          liveSite: false,
          liveUrl: '',
          tech: [
            {
              snackbar: 'Ruby',
              img: 'mdi-language-ruby',
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
          liveSite: true,
          liveUrl: 'https://darkskyui.azurewebsites.net',
          liveText: 'See live site',
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
          description: 'Python scripts for automation.',
          url: 'https://github.com/ZachBaird/Python_Automation',
          live: false,
          liveUrl: '',
          tech: [
            {
              snackbar: 'Python',
              img: 'mdi-language-python',
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
          live: false,
          liveUrl: '',
          tech: [
            {
              snackbar: 'Python',
              img: 'mdi-language-python',
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

@media(min-width: 750px) {
  .medium-screen-dimensions {
    width: 80% !important;
    height: auto !important;
  }
  .project-tech a {
    margin-top: 8px;
    margin-right: 5px;
  }
}

@media(max-width: 650px) {
  .description-section p {
    margin-bottom: 0 !important;
  }
  .project-tech {
    align-items: center;
    margin-top: 5px;
    padding: 20px 0;
  }

  .project-tech a {
    margin-top: 10px !important;
    margin-right: 20px;
    justify-self: center;
  }

  .medium-screen-dimensions {
    width: 70%;
    max-width: 370px;
  }
}
</style>
