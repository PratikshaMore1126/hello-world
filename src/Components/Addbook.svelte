<script>
//   import Book from "./book.svelte";
  
function addBook() {
  const newBook = {
    title: title,
    pages: pages,
    description: description,
  };
  books = books.concat(newBook);
}
</script>

<button on:click>
  <slot />
<!-- <Button on:click={addBook}>ADD Book</Button> -->
<!--  -->

</button>

<style>
  button {
    font: larger;
    padding: 0.15rem 0.5rem;
    background-color: #1b1a1a;
    border: 1px solid aliceblue;
    cursor: pointer;
    color: white;
  }
</style>
