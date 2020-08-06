<template>
  <div>
    <nuxt-link to="/jokes">Back To Jokes
    </nuxt-link>
    <br />
    <button v-on:click="getNewJoke">Shuffle</button>
    <h2>{{ joke.joke }}</h2>
    <hr />
    <small>Joke ID: {{ joke.id }}</small>
  </div>
</template>

<script>
import Joke from '../../components/Joke';
import axios from 'axios';

export default {
  components: {
    Joke
  },
  data(){
    return {
      joke: {}
    }
  },
  methods: {
    async getNewJoke() {
      const config = {
        headers: {
          'Accept': 'application/json'
        }
      }

      try {
        const res = await axios.get(`https://icanhazdadjoke.com/`, config);

        this.joke = res.data;
      } catch (err) {
        console.log(err)
      }
    }
  },
  async created() {
    this.getNewJoke();
  },
  head() {
    return {
      title: 'Dad Joke',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes'
        }
      ]
    }
  }
};
</script>
