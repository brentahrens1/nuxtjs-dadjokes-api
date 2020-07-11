<template>
  <div class="container">
    <AppHeader />
    <Nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader'
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
    font-size: 1rem;
    line-height: 1.6;
    padding: .5em;
  }

  a:link,  a:visited {
    text-decoration: none;
    color: #000;
  }

  li {
    list-style: none;
  }
</style>
