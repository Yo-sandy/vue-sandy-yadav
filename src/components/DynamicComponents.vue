<template >
  <div class="container mt-3">
    <div class="row">
      <box-child btnText="Change Font"/>
    </div>
  </div>
</template>

<script>
import  BoxChild from "./BoxChild.vue";
export default {
  components:{
    BoxChild,
  },
  data() {
    return{
      item: {
        title:"my title",
        description:"this is google description",
      },
    };
  },
};
</script>