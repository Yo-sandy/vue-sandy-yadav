<template>
    <div>
      <h1>Author name:{{ author.name}}</h1>
      <p>Total Books = {{total_books}}</p>
      <button @click="increment">increment</button>
    </div>
</template>
<script>
export default {
  data(){
    return{
      author:{
        name:"kuldeep",
        books:{
          total_books: 5,
        },
      },
    };
  },
  computed:{
    total_books(){
      return this.author.books.total_books;
    },
  },
  methods:{
    increment(){
      this.author.books.total_books++;
    },
  },
};
</script>