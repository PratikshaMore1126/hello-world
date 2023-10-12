<script>
  let number = 1; // Initialize the number
  function incrementNumber() {
    number++;
  }
</script>

<main>
  <table>
    <!-- <caption>Table Caption</caption>
    <thead>
      <tr>
        <th>Number 1</th><th>Number 2</th><th>Number 3</th><th>Number 4</th>
        <th>Number 5</th><th>Number 6</th><th>Number 7</th><th>Number 8</th>
        <th>Number 9</th><th>Number 10</th>
      </tr>
    </thead> -->
    <tbody>
      <tr>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}>
          {#if number == 1}
            {number}
          {:else if number == 2}
            {number}
          {:else if number > 2}2
          {/if}</td
        >
        <!-- <td>2</td> --><td>3</td><td>4</td><td>5</td> <td>6</td><td>7</td
        ><td>8</td><!-- <td>9</td> -->
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}>
          {#if number == 9}
            {number}
          {:else if number == 10}
            {number}
          {:else if number > 10}10
          {/if}</td
        >
      </tr>
      <tr>
        <!-- <td>1</td><td>2</td> --><td>3</td><td>4</td> <td>5</td><td>6</td
        ><td>7</td><td>8</td>
        <!-- <td>9</td><td>10</td> -->
      </tr>
      <tr>
        <td>1</td><td>2</td>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}>
          {#if number == 3}
            {number}
          {:else if number == 4}
            {number}
          {:else if number > 4}4
          {/if}</td
        >
        <!-- <td>4</td> -->
        <td>5</td><td>6</td>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}>
          {#if number == 7}
            {number}
          {:else if number == 8}
            {number}
          {:else if number > 8}8
          {/if}</td
        >
        <!-- <td>8</td> -->
        <td>9</td><td>10</td>
      </tr>
      <tr>
        <td>1</td><td>2</td><!-- <td>3</td><td>4</td> -->
        <td>5</td><td>6</td><!-- <td>7</td> <td>8</td> -->
        <td>9</td><td>10</td>
      </tr>
      <tr>
        <td>1</td><td>2</td><td>3</td><td>4</td>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}>
          {#if number == 5}
            {number}
          {:else if number == 6}
            {number}
          {:else if number > 6}6
          {/if}</td
        >
        <!-- <td>6</td> -->
        <td>7</td><td>8</td><td>9</td><td>10</td>
      </tr>
      <tr>
        <td>1</td><td>2</td> <td>3</td><td>4</td>
        <!-- <td>5</td> <td>6</td> -->
        <td>7</td><td>8</td><td>9</td><td>10</td>
      </tr>
      <tr>
        <td>1</td> <td>2</td>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}
          >{#if number == 3}
            {number}
          {:else if number == 4}
            {number}
          {:else if number > 4}4
          {/if}</td
        >
        <!-- <td>4</td> -->
        <td>5</td> <td>6</td>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}
          >{#if number == 7}
            {number}
          {:else if number == 8}
            {number}
          {:else if number > 8}8
          {/if}</td
        >
        <!-- <td>8</td> -->
        <td>9</td><td>10</td>
      </tr>
      <tr>
        <td>1</td><td>2</td><!-- <td>3</td> <td>4</td> -->
        <td>5</td><td>6</td><!-- <td>7</td> <td>8</td> -->
        <td>9</td><td>10</td>
      </tr>
      <tr>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}
          >{#if number == 1}
            {number}
          {:else if number == 2}
            {number}
          {:else if number > 2}2
          {/if}</td
        ><!-- <td>2</td> -->
        <td>3</td><td>4</td><td>5</td><td>6</td><td>7</td><td>8</td>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td colspan="2" rowspan="2" id="tab" on:click={incrementNumber}
          >{#if number == 9}
            {number}
          {:else if number == 10}
            {number}
          {:else if number > 10}10
          {/if}</td
        ><!-- <td>10</td> -->
      </tr>
      <!-- <tr>
                <td rowspan="2">1</td><td>2</td>
                <td rowspan="2">3</td><td>4</td>
                <td rowspan="2">5</td><td>6</td>
                <td rowspan="2">7</td><td>8</td>
                <td rowspan="2"> 9</td><td>10</td>
            </tr>
            <tr>
                <td>2</td><td>4</td><td>6</td><td>8</td><td>10</td>
            </tr>
            <tr>
                <td colspan="2">1</td><td colspan="2">3</td><td colspan="2">5</td>
                <td colspan="2">7</td><td colspan="2">9</td>
            </tr> -->
      <tr>
        <!-- <td> 1</td> <td> 2 </td> -->
        <td>3</td><td>4</td><td>5</td><td>6</td><td>7</td><td>8</td>
        <!-- <td>9</td> <td>10</td> -->
      </tr>
    </tbody>
  </table>
</main>

<style>
  table {
    /* background-color: #ed1818; */
    height: 500px;
    width: 100%;
    border-radius: 30%;
  }
  /* caption {
    background-color: rgb(39, 203, 39);
    height: 70px;
    text-align: center;
    font-size: 40px;
  } */
  /* th {
    background-color: rgb(169, 165, 199);
  } */

  td {
    text-align: center;
    text-shadow: green;
    font-size: 30px;
    font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
    font-weight: 200;
    font-style: italic;
    color: rgb(39, 28, 15);
    border: 1px solid black;
    border-collapse: collapse;
    padding: 10px;
    text-align: center;
    border-radius: 30%;
    /* background-color: darkmagenta; */
  }
  #tab {
    background-color: rgb(234, 84, 250);
    color: rgb(255, 0, 0);
  }
</style>
