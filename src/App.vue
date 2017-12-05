<template>
  <div id="app">
    <navbar></navbar>
    <router-view/>
  </div>
</template>

<script>
import Navbar from './components/layout/Navbar'

export default {
  name: 'app',
  components: {
    Navbar
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Merriweather:400,700');
  /* @import url('https://fonts.googleapis.com/css?family=Roboto+Slab:300,400,700'); */
  /* @import url('https://fonts.googleapis.com/css?family=Playfair+Display:400,700'); */
</style>
