<template>
  <v-container fill-height>
    <v-layout align-center>
      <v-flex class="text-center">
        <blockquote class="font-weight-medium">
          &#8220;{{ chosenQuote.quote }}&#8221;
          <footer>
            <small>
              <em>&mdash; {{ chosenQuote.from }}</em>
            </small>
          </footer>
        </blockquote>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      quotes: [
        {
          from: 'John Johnson',
          quote: 'First, solve the problem. Then, write the code.'
        },
        {
          from: 'Lucius Seneca',
          quote: 'Luck is what happens when preparatation meets opportunity.'
        },
        {
          from: 'Lucius Seneca',
          quote: 'Difficulties strenghten the mind, as labor does the body.'
        },
        {
          from: 'Harold Abelson',
          quote: 'Programs must be written for people to read, and only incidentally for machines to execute.'
        },
        {
          from: 'Uncle Bob',
          quote: 'Truth can only be found in one place: the code.'
        },
        {
          from: 'John Steinbeck',
          quote: 'What good is the warmth of summer, without the cold of winter to give it sweetness.'
        }
      ]
    }
  },
  computed: {
    chosenQuote () {
      return this.quotes[Math.floor(Math.random() * this.quotes.length)]
    }
  }
}
</script>
