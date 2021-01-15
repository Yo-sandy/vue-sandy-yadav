<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <FluidNavigation/>
  <ListRendring/>
</template>

<script>
import FluidNavigation from "./components/FluidNavigation.vue";
import ListRendring from "./components/ListRendring.vue";
export default {
  name: 'App',
  components: {
    FluidNavigation,
    ListRendring
  }
}
</script>

<style scoped>
  img{
    width: 300px;
  }
</style>
