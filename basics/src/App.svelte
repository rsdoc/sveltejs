<script>
  let name = 'world !!! 😁';

  let count = 0;

  $: doubled = count * 2;

  // declaring the statements reactively
  $: console.log('Hello i am doubled value', doubled);

  // grouping multiple statements together
  $: {
    console.log('I am group of statements');
    // alert('count is ' + count);
  }

  // conditional statements
  $: if (count > 10) {
    count = 0;
  }

  function handleClick() {
    // console.log('button is clicked');
    count = count + 1;
  }
</script>

<style>
</style>

<main>
  <h1>hello {name} and count is {count} and doubled is {doubled}</h1>
  <button on:click={handleClick}>Clicked</button>
</main>
