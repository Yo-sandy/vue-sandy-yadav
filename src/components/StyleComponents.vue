<template >
    <div class="container mt-3">
    <div class="row">
      <h3 :style="{ fontSize: fontSize + 'em'}"> All item</h3>
      <box-component v-for="(item, index) in items" :key="index" :item="item" @change-font="changeFont"/>
    </div>
    </div>
</template>


<script>
import BoxComponent from "./BoxComponent.vue";
export  default {
  components:{
    BoxComponent,
  },
  data(){
    return{
      fontSize: 1,
      items: [
        {
          title:"my title",
          description:"this is google description",
          link_title:"Google",
          link:"https://google.com"
        },
        {
          title:"my title",
          description:"this is fb description",
          link_title:"facebook",
          link:"https://fb.com"
        },
        {
          title:"my title",
          description:"this is yahoo description",
          link_title:"yahoo",
          link:"https://yahoo.com"
        },
        {
          title:"my title",
          description:"this is yahoo description",
          link_title:"djpunjaab",
          link:"https://djpunjaab.com"
        },
      ],
    };
  },
  methods:{
    changeFont($event){
      this.fontSize += $event;
    },
  },
};
</script>