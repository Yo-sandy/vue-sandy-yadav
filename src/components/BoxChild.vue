<template>
  <div class="col-md-4 mb-2">
    <div class="card" style="width: 18rem">
      <div class="card-body" v-bind="$attrs">
        <h5 class="card-title">{{ title }}</h5>
        <p class="card-text">{{ item.description }}</p>
        <a :href="item.link" class="card-link">{{ item.link_title }}</a><br/>
        <button class="btn-primary" @click="$emit('changeFont', 2)">
          {{ btnText }}
        </button>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  inheritAttrs: true,
  props:  {
    item:{
      type: Object,
      default:{
        title:"my title",
        description:"this is google description",
      },
    },
    btnText:{
      type: String,
      validator: function (value) {
        return ["Change Font"].indexOf(value) !== -1;
      },
    },
  },
  data(){
    return{
      title: this.item?.title,
    };
  },
};
</script>
