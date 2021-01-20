<template>
  <PIChild1> </PIChild1>
    <button class="btn btn-primary" @click="text = 'my new text'">
      Change text
    </button>
</template>

<script>
import { computed } from "vue";
import PIChild1 from  "./PIChild1.vue";
export default {
  provide(){
    return{
      text:computed(() => this.text),
      listLength: this.list.length,
    };
  },
  components:{
    PIChild1,
  },
  data(){
    return{
      list: ["this","that"],
      text: "this is my text",
    };
  },
};
</script>

