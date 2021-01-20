<template >
  <div class="container mt-3">
    <div class="row">
      <box-child btnText="Change Font" @click="run('this is first')" style="background-color: #0a53be;color: white"/>
      <box-child btnText="Change Font" @click="run('this is 2nd')"/>
      <select-input @change="checkSelectedOption"/>
      <user-login @login="run('you clicked on longin btn')"/>
    </div>
  </div>
</template>

<script>
import  BoxChild from "./BoxChild.vue";
import SelectInput from "./SelectInput.vue"
import UserLogin from "./UserLogin.vue";
export default {
  components:{
    BoxChild,
    SelectInput,
    UserLogin
  },
  data() {
    return{
      item: {
        title:"my title",
        description:"this is google description",
      },
    };
  },
  methods:{
    run(msg){
      console.log(msg);
    },
    checkSelectedOption(e){
      console.log(e.target.value);
    },
  },
};
</script>