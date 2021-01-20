<template>
  <div :class="isFluid ? 'container-fluid' : 'container'">
    <div class="row">
      <slot>
        <div class="col-md-6">
          <h3>this is col md 6</h3>
        </div>
        <div class="col-md-6">
          <h3>this is col md 6</h3>
        </div>
      </slot>
    </div>
  </div>
  <div :class="isFluid ? 'container-fluid' : 'container'">
    <div class="row">
        <div class="col-md-10 bg-warning">
           <slot name="main"></slot>
        </div>
        <div class="col-md-2 bg-danger">
          <slot name="sidebar"></slot>
        </div>
    </div>
  </div>
</template>


<script>
export default {
  props:{
    isFluid:Boolean,
    default: false,
  }
}
</script>