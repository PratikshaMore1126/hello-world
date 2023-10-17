<script>
  import { createEventDispatcher } from "svelte";
  import FirstDispatcher from "./FirstDispatcher.svelte";
  const dispatch = createEventDispatcher();

  function ForwardEvent() {
    dispatch("message", {
      Text: "Lorem ipsum dolor sit amet consectetur adipisicing elit Fugiat dolorum suscipit quo eaque eum, perspiciatis minima nulla corrupti deserunt in,aliquam aperiam nihil praesentium rem laudantium illo. Veritatis, asperiores expedita? ",
      Data: "This is from second  Dispatcher",
    });
  }
</script>

<main>
  <!-- <Dispatcher on:message={ForwardEvent} /> -->
  <FirstDispatcher on:message={ForwardEvent} />
  <!-- <button on:message={ForwardEvent} /> -->
</main>
