
<template>
  <todo-list v-slot="slotProps">
    <span class="green">{{ slotProps.item }}</span>
  </todo-list>
</template>


<script>
import TodoList from  "./TodoList.vue";
export default {
  components:{
    TodoList,
  },
  data(){
    return{};
  }
}
</script>