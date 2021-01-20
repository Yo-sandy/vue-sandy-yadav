<template>
  <ul>
    <li v-for="(item,index) in  item" :key="index">
      <slot :item="item"></slot>
    </li>
  </ul>
</template>


<script>
export default {
  data(){
    return{
      item:["feed a cat","buy milk"],
    };
  },
};
</script>