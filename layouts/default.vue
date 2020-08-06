<template>
  <div class="container">
    <AppHeader />
    <Nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader';

export default {
  components: {
    AppHeader
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    background:  #f4f4f4;
  }

  a {
    color: #666;
    text-decoration: none;
  }

  ul {
    list-style: none;
  }

  .container {
    max-width: 800px;
    margin: 2 rem auto;
    overflow: hidder;
    padding: 1rem 2rem;
    background: #fff;
  }

  button {
   display:inline-block;
   padding:0.35em 1.2em;
   border:0.1em solid #FFFFFF;
   margin:0 0.3em 0.3em 0;
   border-radius:0.12em;
   box-sizing: border-box;
   text-decoration:none;
   font-family:'Roboto',sans-serif;
   font-weight:300;
   color:#FFFFFF;
   text-align:center;
   transition: all 0.2s;
  }

</style>
