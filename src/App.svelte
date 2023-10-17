<script>
  import FirstComponent from "./Components/FirstComponent.svelte";
  import BindingForm from "./Components/bindingForm.svelte";
  import Hooks from "./Components/hooks.svelte";
  // import Dispatcher from "./Components/FirstDispatcher.svelte";
  import Second from "./Components/second.svelte";
  import Table from "./Components/table.svelte";
  // import Addbook from "./Components/Addbook.svelte";
  import Assignment1 from "./Components/Assignment1.svelte";

  // export let name;
  let dat = "Props example";

  function handleMessage(event) {
    alert(event.detail.Text);
  }
  function handleMessage1(event) {
    alert(event.detail.Data);
  }
  let one = false;
  function oneHeader() {
    one = !one;
  }

  // import Book from "./Components/book.svelte";
  // let title = "";
  // let pages = 0;
  // let description = "";
  // function setTitle(event) {
  //   title = event.target.value;
  // }
</script>

<main>
  <button on:click={oneHeader}> Click here to load Header</button>

  {#if one}
    <FirstComponent />
  {/if}

  <h1>{dat}</h1>

  <Table /> <br /><br /><br />

  <Second on:message={handleMessage} />
  <Second on:message={handleMessage1} />

  <!-- <Dispatcher on:message={handleMessage}></Dispatcher> -->
  <!-- <Hooks /> -->
  <BindingForm />
<!-- 
  <section>
    <div>
      <label for="title">Title</label>
      <input type="text" id="title" value={title} on:input={setTitle} />
    </div>
    <div>
      <label for="pages"> pages</label>
      <input type="number" id="price" bind:value={pages} />
    </div>
    <div>
      <label for="description">Description</label>
      <textarea rows="3" id="description" bind:value={description} />
    </div>
  </section> -->
  <!-- <Book bookTitle={title} bookPages={pages} bookDescription={description} />. -->

  <!-- {#if Book.length === 0}
    <p>Add a new book</p>
  {:else}
    {#each Book as book}
      <Book
        bookTitle={book.title}
        bookPages={book.pages}
        bookDescription={book.description}
      />
    {/each}
  {/if} -->

  <!-- <Button on:click={addBook}>ADD Book</Button> -->
  <!-- <Addbook on:click={setTitle} /> -->

  <Assignment1></Assignment1>
</main>

<style>
  main {
    /* text-align: center; */
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    background-color: rgb(179, 177, 173);
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
    text-align: center;
  }
  button {
    color: yellow;
    background-color: rgb(103, 10, 10);
    border-radius: 30%;
  }
  
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
