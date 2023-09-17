<script>
  let count = 0;

  $: {
    console.log(`the count is ${count}`);
    console.log(`this will also be logged whenever count changes`);
    if (count >= 15) {
      alert("count is dangerously high!");
      count = 0;
    }
  }
  $: doubled = count * 2;

  const increment = () => {
    count += 1;
  };
</script>

<button class="btn btn-primary" on:click={increment}>
  count is {count}
</button>
<p class="my-3">{count} doubled is {doubled}</p>
{#if count > 10}
  <p class="mb-3">{count} is greater than 10</p>
{:else if count < 5}
  <p class="mb-3">{count} is less than 5</p>
{:else}
  <p>{count} is between 0 and 10</p>
{/if}
