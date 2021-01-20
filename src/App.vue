<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <FluidNavigation/>
  <Transitions/>
</template>

<script>
import FluidNavigation from "./components/FluidNavigation.vue";
import Transitions from  "./components/Transitions.vue";
export default {
  name: 'App',
  components: {
    FluidNavigation,
    Transitions
  },
}
</script>

<style scoped>
  img{
    width: 200px;
  }
</style>
