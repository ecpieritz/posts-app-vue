<template>
  <div id="app">
    <Header />
    <div class="container">
      <Cards />
    </div>
  </div>
</template>

<script>
import Header from './components/Header'
import Cards from './components/Cards'

export default {
  name: 'App',
  components: {
    Header, Cards
  }
}
</script>

<style>
:root {
  --light-blue: #4a7399;
  --blue: #1d4468;
  --dark-blue: #09233b;
  --white: #ffffff;
}

body,
html {
  font-family: 'Montserrat', sans-serif;
  background-color: var(--blue);
}
</style>
