<template>
  <div class="container">
    <div class="row">
      <name-input v-model:firstname.capital="first_name"/>
      <h3>User First Name Is:{{ first_name }}</h3>
      <user-login @login="run('you clicked on longin btn')"/>
    </div>
  </div>
</template>

<script>
  import UserLogin from "./UserLogin.vue";
  import NameInput from "./NameInput.vue";
  export default {
    components:{
      UserLogin,
      NameInput
    },
    data(){
      return{
        first_name: "",
      };
    },
  };
</script>