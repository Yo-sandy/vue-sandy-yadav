<template>
  <div class="m-2">
    <button class="m-2 btn-outline-primary" v-for="n in 5">{{n}}</button>
  </div>
  <div>
    <ul >
      <li v-for="item in items" :key="item.message">
        {{ item.message }}
      </li>
    </ul>
  </div>
  <div>
    <ul>
      <li v-for="(name,value) in history">
        {{value}}: {{name}}
      </li>
    </ul>
  </div>
</template>


<script>
export default {
  data(){
    return {
      items:[
        {message:"foo"},
        {message:"bar"}
      ],
      history:{
        title:"Son of Farmer",
        Author:"Jhon doe",
        publishedAt:"18-1-2019"
      },
    }
  },
};
</script>