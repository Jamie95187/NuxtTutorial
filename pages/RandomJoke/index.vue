<template>
  <div>
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
  async created() {
    const config = {
      headers: {
        'Accept': 'application/json'
      }
    }

    try {
      const res = await axios.get("https://icanhazdadjoke.com/", config);

      this.joke = res.data;
    } catch (err) {
      console.log(err)
    }
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
