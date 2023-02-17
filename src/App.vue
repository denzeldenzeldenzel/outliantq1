<template>
  <Nav></Nav>
  <RouterView />
  <Footer></Footer>
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
import Nav from "./components/Nav.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  components: {
    Nav,
    Footer
  }
}
</script>

<style scoped>
</style>
