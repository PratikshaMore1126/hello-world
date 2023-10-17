<script>
  import { afterUpdate, beforeUpdate, onDestroy, onMount } from "svelte";

  onMount(() => {
    alert("onMount event is called");
  });
  onDestroy(() => {
    alert("onDestroy event is called");
  });
  beforeUpdate(() => {
    alert("before Update event is called");
  });
  afterUpdate(() => {
    alert("after Update event is called");
  });
</script>
