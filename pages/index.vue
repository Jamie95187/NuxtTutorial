<template>
  <div>
      <h2>
        Welcome to the best jokes page
      </h2>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: 'Welcome to Dad Jokes',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'Best place for corny dad jokes'
          }
        ]
      };
    }
  };
</script>
