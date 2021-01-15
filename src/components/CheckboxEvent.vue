<template>
  <div>
    <div>
      <input type="checkbox" v-model="isChecked"/>
      <div class="box" :class="{activeclass:isChecked}"></div>
    </div>
  </div>
</template>

<script>
export default {
      data(){
        return{
          isChecked:false,
          mycolor: "pink"
        };
      },
  methods: {},
};
</script>

<style>
.box{
  width: 200px;
  height: 200px;
  background-color: #0a58ca;
}
.activeclass{
  background-color: green !important;
}
</style>