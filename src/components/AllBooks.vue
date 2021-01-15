<template>
  <div>
    <h1>Author name:{{ author.name}}</h1>
     <ul>
       <li v-for="(book,index) in author.books" :key="index">
         {{book}}
       </li>
     </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      author:{
        name: "jhon",
        books: [
            "php cookbook",
            "js cookbook",
            "python cookbook",
            "kotlin cookbook",
            "css cookbook",
        ],
      },
    };
  },
computed:{
    total_books(){
      return 0;
    },
  },
  methods: {},
};
</script>