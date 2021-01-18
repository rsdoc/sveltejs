<script>
  import Card from './Card.svelte';
  import Others from './Others.svelte';
  export let name;
  let lastname = 'singh';
  let textAreaData = '';
</script>

<main>
  <h1>Hello {name} <Others {lastname} /></h1>
  <Card>
    <h2 slot="header">Heading from parent</h2>
    <p slot="body">body from parent</p>
    <footer slot="footer">footer from parent</footer>
  </Card>

  <textarea
    style="margin-top: 2rem; margin-left: 2rem; border: 2px solid pink;"
    name="template"
    id="textarea1"
    cols="30"
    rows="10"
    bind:value={textAreaData}
  />
  <div>{textAreaData}</div>
  <div>{@html textAreaData} is not sanitized risk</div>
</main>

<style>
  h1 {
    color: #ff3e00;
    font-size: 4em;
    font-weight: 100;
  }
</style>
