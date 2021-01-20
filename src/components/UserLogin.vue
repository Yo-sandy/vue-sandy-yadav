<template>
  <div class="mb-2">
    <label for="email">User Email</label>
    <input
        type="email"
        placeholder="Enter Your Email"
        id="email"
        class="form-control"
    />
  </div>
  <div class="mb-2">
    <label for="password">Password</label>
    <input
        type="password"
        placeholder="Enter Your Password"
        id="password"
        class="form-control"
        v-bind="$attrs"
    />
  </div>
  <div class="mb-2">
    <button class="btn btn-primary" @click="$emit('login')">Login</button>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  emits: {
    login: function (){
      return false;
    },
  },
};
</script>