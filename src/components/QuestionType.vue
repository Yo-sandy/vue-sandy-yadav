<template>
  <div>
    <div>
      <input
          type="text"
          class="m-2"
          placeholder="enter the Question"
          v-model="question"
      />
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      question: "",
    };
  },
  watch:{
    question(newValue,oldValue){
      if(newValue.indexOf("?")> -1){
        alert("you type a question");
      }
    },
  },
  methods: {},
};
</script>