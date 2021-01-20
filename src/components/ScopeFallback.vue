<template>
  <ContainerScopeFallback></ContainerScopeFallback>
  <ContainerScopeFallback></ContainerScopeFallback>
  <ContainerScopeFallback></ContainerScopeFallback>
  <ContainerScopeFallback></ContainerScopeFallback>
  <ContainerScopeFallback>
      <div class="col-md-4">
        <h3>this is col md 4</h3>
      </div>
    <div class="col-md-4">
      <h3>this is col md 4</h3>
    </div>
    <div class="col-md-4">
      <h3>this is col md 4</h3>
    </div>
    <template v-slot:main>
      <h1>this main area</h1>
    </template>
    <template v-slot:sidebar>
      <h1>this is sidebar area</h1>
    </template>
  </ContainerScopeFallback>
</template>

<script>
import ContainerScopeFallback from  "./ContainerScopeFallback.vue";
export  default {
  components:{
    ContainerScopeFallback
  },
  data(){
    return {
      text: "this is text"
    };
  },
};
</script>