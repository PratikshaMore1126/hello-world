<script>
  import { getContext } from "svelte";
  export let id;
  export let name = "";
  export let amount = 0;
  let displayAmount = true;

  function toggleAmount() {
    displayAmount = !displayAmount;
  }
  const removeExpense = getContext("remove");
  const setModifiedExpense = getContext("modify");
</script>

<article class="single-expense">
  <div class="expense-info">
    <h2>
      {name}
      <button class="amount-btn" on:click={toggleAmount}> Add </button>
    </h2>
    {#if displayAmount}
      <h4>amount : ${amount}</h4>
    {/if}
  </div>
  <div class="expense-buttons">
    <button
      class="expense-btn edit-btn"
      on:click={() => setModifiedExpense(id)}
    >
      Edit
    </button>
    <button class="expense-btn delete-btn" on:click={() => removeExpense(id)}>
      Delete
    </button>
  </div>
</article>
