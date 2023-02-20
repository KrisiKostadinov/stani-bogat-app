<template>
  <wrapper-app>
    This is the children.
  </wrapper-app>
</template>

<script>
import WrapperApp from './components/WrapperApp.vue';

export default {
  name: "App",
  components: {
    "wrapper-app": WrapperApp
  }
}
</script>

<style scoped>
</style>
