<div class="card">
  <slot name="header" />
  <slot name="body">
    <p>I am default element if nothing is provided</p>
  </slot>
  <slot name="footer" />
</div>

<style>
  .card {
    border: 1px solid red;
  }
</style>
