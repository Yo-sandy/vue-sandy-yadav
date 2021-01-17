<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <FluidNavigation/>
  <FormInputBindings/>
</template>

<script>
import FluidNavigation from "./components/FluidNavigation.vue";
import FormInputBindings from "./components/FormInputBindings.vue";
export default {
  name: 'App',
  components: {
    FluidNavigation,
    FormInputBindings
  }
}
</script>

<style scoped>
  img{
    width: 300px;
  }
</style>
