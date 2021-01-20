<template>
  <div class="mb-2">
    <label for="search">Search</label>
    <input
        type="search"
        id="search"
        ref="search"
        class="form-control"
        placeholder="Enter your Query"
        data-abc="this is my data-abc"
    />
  </div>
</template>


<script>
export default {
  data(){
    return {};
  },
  mounted() {
    console.log(this.$refs.search.dataset.abc);
  },
};
</script>