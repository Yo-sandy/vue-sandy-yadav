<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <FluidNavigation/>
  <StyleComponents/>
  <SlotComponents/>
  <DynamicComponents/>
</template>

<script>
import FluidNavigation from "./components/FluidNavigation.vue";
import  StyleComponents from "./components/StyleComponents.vue";
import  SlotComponents from "./components/SlotComponents.vue";
import DynamicComponents from "./components/DynamicComponents.vue";
export default {
  name: 'App',
  components: {
    FluidNavigation,
    StyleComponents,
    SlotComponents,
    DynamicComponents
  },
}
</script>

<style scoped>
  img{
    width: 300px;
  }
</style>
