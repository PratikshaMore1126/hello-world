<script>
  import { createEventDispatcher } from "svelte";
  const dis = createEventDispatcher();

  function clickDispatch() {
    dis("message", {
      Text: "This is first dispatcher text ",
      Data: "this is from first distaptcher ",
    });
  }
</script>

<main>
  <button on:click={clickDispatch}
    >From second Dispatcher and its Text and Data</button
  >
  <!-- <button on:click={clickDispatch}>From Second Dispatcher and its data</button> -->
</main>

<!-- <style>
  button {
    color: yellow;
    background-color: rgb(103, 10, 10);
    border-radius: 10%;
  }
</style> -->
