<template>
  <div class="container">
    <div class="row">
      <alert>
        <a href="#" class="alert-link alert-dark">go to this link</a><br/>
        <a href="#" class="alert-link alert-light">go to this link</a><br/>
        <a href="#" class="alert-link">go to this link</a><br/>
        <a href="#" class="alert-link">go to this link</a><br/>
      </alert>
    </div>
  </div>
</template>


<script>
import Alert from "./Alertbox.vue";
export default {
  components:{
    Alert,
  },
  data(){
    return{};
  },
};
</script>