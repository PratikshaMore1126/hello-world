<!-- <script>
import { createEventDispatcher } from "svelte";
const dp = createEventDispatcher();
let bookname = " ";
let bookauther = " ";
let bookprice = " ";
function add(){
    // let name = bookname;
    // let author = bookauther;
    // let price = bookprice;
    dp("add",{
        
    })
}
</script>

<main>


  <div>
    <label for="name">Enter a book name :</label>
    <input type="text" id="name" bind:value={bookname}><br>
    <label for="name">Enter a book auther :</label>
    <input type="text" id="name" bind:value={bookauther}><br>
    <label for="name">Enter a book Price :</label>
    <input type="text" id="name" bind:value={bookprice}><br><br>

    <button on:click={add}> Click here to add</button>
  </div>
  <div id="card">
    <h1>{bookname}</h1>
    <h3>{bookauther}</h3>
    <h3>{bookprice}</h3>
  </div>
  <h1>{name}</h1>


</main>

<style>
    div{
        text-align: center;
        height: 300px;
        width: 500px;
        background-color: rgb(156, 157, 109);
    }
    #card{
        height: 200px;
        width: 200px;
    }
label{
    color: black;
}
</style> -->
<!-- App.svelte --><!-- App.svelte --><!-- App.svelte -->


<script>
    import Book from './Book.svelte';
  
    let books = [
    //   { title: 'Book 1', author: 'Author 1', price: 15.99 },
    //   { title: 'Book 2', author: 'Author 2', price: 12.99 },
    //   { title: 'Book 3', author: 'Author 3', price: 20.99 }
    ];
  
    let newBook = { title: '', author: '', price: '' };
  
    const addBook = () => {
      books = [...books, { ...newBook }];
      newBook = { title: '', author: '', price: '' };
    };
  </script>
  
  <main>
    
    <div class="book-container">
      {#each books as book (book.title)}
        <Book
          title={book.title}
          author={book.author}
          price={book.price}
          key={book.title}
        />
      {/each}
    </div>
  
    <h2 id="add">Add a New Book</h2>
    <div class="add-book-form">
        <label for="name">Enter a book Name :</label>
        <input type="text"  bind:value={newBook.title} /><br>

        <label for="name">Enter a book Author :</label>
        <input type="text"  bind:value={newBook.author} /><br>

        <label for="name">Enter a book Price :</label>
        <input type="number" bind:value={newBook.price} /><br><br>
      <button on:click={addBook}>Add Book</button>
    </div>
  </main>
  
  <style>
    .book-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }
  
    .add-book-form {
        margin-left: 40%;
      max-width: 250px;
      text-align: center;
    }
    #add{
        margin-left: 42%;
        color: red;
    }
  </style>
  