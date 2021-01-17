<template>
  <div>
    <div>
      <h1>Count:{{count}}</h1>
      <button class="btn btn-primary mx-2" @click="increaseByten">MY BUTTON</button>
    </div>
  </div>
  <button class="btn btn-primary m-2" @click="greeting('Hi',$event)">say hi</button>
  <button class="btn btn-primary m-2" @click="greeting ('hellow',$event)">say hellow</button>
  <button class="btn btn-primary m-2" @click="greeting('bye bye',$event)">say bye bye</button>
</template>

<script>
export default {
  data(){
    return{
      count: -10,
    };
  },
  methods:{
    greeting(message, e) {
      alert(message);
    },
    increaseByten(){
      if(this.count < 0){
        this.count = 0;
      }else {
        this.count++;
      }
    },
  },
};
</script>