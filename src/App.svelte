<script>
  import { setContext } from "svelte";

  //component
  import Navbar from "./Navbar.svelte";
  import ExpenseList from "./ExpenseList.svelte";
  import Totals from "./Totals.svelte";
  import ExpenseForm from "./ExpenseForm.svelte";
  //data
  import expensesData from "./expenses";
  // import Abc from "./Abc.svelte";

  //variable
  let expenses = [...expensesData];
  //set editing variables
  let setName = "";
  let setAmount = null;
  let setId = null;
  //reactive
  $: isEditing = setId ? true : false;
  $: total = expenses.reduce((acc, curr) => {
    return (acc += curr.amount);
  }, 0);

  //functions
  function removeExpense(id) {
    expenses = expenses.filter((item) => item.id !== id);
  }
  function clearExpenses() {
    expenses = [];
  }
  function addExpense({ name, amount }) {
    let expense = { id: Math.random() * Date.now(), name, amount };
    expenses = [expense, ...expenses];
  }
  function setModifiedExpense(id) {
    let expense = expenses.find((item) => item.id === id);

    setId = expense.id;
    setName = expense.name;
    setAmount = expense.amount;
  }
  function editExpense({ name, amount }) {
    console.log({ name, amount });
  }
  //context
  setContext("remove", removeExpense);
  setContext("modify", setModifiedExpense);
  //

  // import Example from "./Example.svelte";
  //  Each_block
  // let fruits = ["apple", "orange", "lemon"];
  // import Title from "./Title.svelte";
</script>

<Navbar />

<main class="content">
  <ExpenseForm
    {addExpense}
    name={setName}
    amount={setAmount}
    {isEditing}
    {editExpense}
  />
  <Totals title="total expenses" {total} />
  <!-- example of props drilling (passing a functionas as props is called props drilling) -->
  <ExpenseList {expenses} />
  <button
    type="button"
    class="btn btn-primary btn-block"
    on:click={clearExpenses}
  >
    clear expenses
  </button>
</main>

<!-- <Abc name={"Pratiksha"}/> -->

<!-- <Title title="add expense" />
<Title title="expense list" />
<Title />
<Example />
<span>Hello from app</span> -->

<!-- Each_block -->
<!-- {#each fruits as item }  -->
<!-- <h1>fruit : {item}</h1> .... comment import title -->
<!-- <Title title={item} />
{/each} -->
