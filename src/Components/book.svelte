<!-- Book.svelte -->
<script>
  export let title;
  export let author;
  export let price;
</script>

<div class="book-card">
  <h1 style="text-align: center;">{title}</h1>
  <h3>Author: {author}</h3>
  <h3>Price: {price}</h3>
</div>

<style>
  .book-card {
    background-color: #dfec24;
    border: 1px solid #e40d0d;
    padding: 20px;
    margin: 10px;
    border-radius: 5px;
    width: 250px;
  }
</style>
