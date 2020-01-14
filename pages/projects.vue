<template>
  <div class="projects">
    <h1 class="subheading grey--text">
      Projects
    </h1>
    <v-container class="my-5 project">
      <v-img
        :src="projects[page-1].image"
        width="100px"
        alt="Project Screenshot"
        class="mx-auto"
      />
      <h2 class="font-weight-regular text-center my-1">
        {{ projects[page-1].title }} | Status: {{ projects[page-1].status }}
      </h2>
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
          <v-icon color="primary">
            {{ stack.img }}
          </v-icon>
        </div>
      </div>
    </v-container>
    <v-spacer />
    <v-pagination
      v-model="page"
      color="primary"
      :length="5"
    />
  </div>
</template>

<script>
export default {
  data () {
    return {
      page: 1,
      projects: [
        {
          image: 'v.png',
          title: 'Main Site',
          status: 'Active',
          description: 'A main site built with Nuxt.js and statically generated.',
          url: 'https://google.com',
          tech: [
            {
              snackbar: 'Nuxt.js',
              img: 'mdi-nuxt'
            },
            {
              snackbar: 'Vuetify.js',
              img: 'mdi-vuetify'
            }
          ]
        },
        {
          image: 'v.png',
          title: 'CaesarCipher',
          status: 'Finished',
          description: 'A Ruby script that runs a CaesarCipher on a string of text.',
          url: 'https://google.com',
          tech: [
            {
              snackbar: 'Ruby',
              img: 'mdi-ruby'
            }
          ]
        },
        {
          image: 'v.png',
          title: 'OreoWeather',
          status: 'On hold',
          description: 'A .Net Core weather application for my grandfather. Consumes the Dark Sky API and allows him to avoid the slow & cluttered, existing weather sites.',
          url: 'https://google.com',
          tech: [
            {
              snackbar: 'C# .Net Core',
              img: 'mdi-dot-net'
            },
            {
              snackbar: 'Bootstrap',
              img: 'mdi-bootstrap'
            }
          ]
        },
        {
          image: 'v.png',
          title: 'Python Automation',
          status: 'On hold',

          description: 'A series of Python scripts that automate file manipulation, web scraping, and GUI tasks.',
          url: 'https://google.com',
          tech: [
            {
              snackbar: 'Python',
              img: 'mdi-language-python-text'
            }
          ]
        },
        {
          image: 'v.png',
          title: 'Realestate app',
          status: 'On hold',

          description: 'A real estate application built with the Django framework.',
          url: 'https://google.com',
          tech: [
            {
              snackbar: 'Django',
              img: 'mdi-django'
            },
            {
              snackbar: 'Python',
              img: 'mdi-language-python-text'
            },
            {
              snackbar: 'Bootstrap',
              img: 'mdi-bootstrap'
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
  margin: 10px 15px 0 15px;
}

.projects .project {
  height: 70%;
}
</style>
