<script setup>
import Header from './components/AppHeader.vue'
import Footer from './components/AppFooter.vue'
</script>

<script>
import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {

}
</style>

<template>
  <Header/>
  <HelloWorld/>
  <Footer/>
</template>
