<template>
  <div class="mb-2">
    <label for="name">Name</label>
    <input
        type="text"
        id="name"
        placeholder="Enter Your Name"
        class="form-control"
        :value="firstname"
        @input="emitValue"
    />
  </div>
</template>


<script>
export default {
  props:["firstname", "firstnameModifiers"],
  methods:{
    emitValue(e){
      let value = e.target.value;
      if (this.firstnameModifiers.capital){
        value = value.charAt(0).toUpperCase() + value.slice(1);
      }
      this.$emit("update:firstname",value);
    },
  },
};
</script>