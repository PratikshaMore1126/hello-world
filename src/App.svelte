<script>
  import FirstComponent from "./Components/FirstComponent.svelte";
  import Dispatcher from "./Components/dispatcher.event.svelte";
  import Table from "./Components/table.svelte";

  // export let name;
  let dat = "Props example";

  function handleMessage(event){
    alert(event.detail.Text)
  };

</script>

<main>
  <FirstComponent />

  <h1>{dat}</h1>
  
  <Table></Table>   <br><br><br>
  
  <Dispatcher on:message={handleMessage}></Dispatcher>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    background-color: rgb(92, 74, 15);
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
