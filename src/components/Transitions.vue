<template>
  <div class="m-3">
    <button class="btn btn-outline-danger" @click="show = !show">
      Toggle render
    </button>

    <transition name="slide-fade">
      <div class="container" v-show="show">
          <img src="https://freepngimg.com/thumb/star/2-gray-star-png-image.png" style="width: 400px" >
      </div>
    </transition>
  </div>

</template>

<script>
export default {
  components:{
  },
    data() {
      return {
        show: true
      };
    },
};
</script>


<style>
.slide-fade-enter-active {
  transition: all 0.5s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
</style>