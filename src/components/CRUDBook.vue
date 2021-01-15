<template>
  <div>
    <div>
      <label for="book">Book Name: </label>
      <input
          type="text"
          placeholder="enter the book name"
          v-model="book_name"
          class="m-2"
      />
    </div>
    <button @click="addBook" class="btn btn-primary">{{ is_update ? "update" :"add"}}</button>
    <h3 v-if="books.length > o" >All Available Books</h3>
    <ul>
      <li v-for="(book,index) in books" :key="index">
        {{book}}
        <span>
          <button @click="edit(index)" class="btn-outline-info m-2">Edit</button>
          <button @click="deletebook(index)" class="btn-outline-danger">Delete</button>
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      is_update: false,
      temp_index:null,
      book_name: "",
      books:[],
    };
  },
  methods: {
    addBook(){
      if (this.is_update){
        this.books[this.temp_index] = this.book_name;
        this.is_update = false;
        this.temp_index = null;
      }else {
        this.books.push(this.book_name);
      }
      this.book_name = "";
    },
    deletebook(index){
      this.books.splice(index, 1);
    },
    edit(index){
      this.book_name = this.books[index];
      this.is_update = true;
      this.temp_index = index;
    },
  },
};
</script>