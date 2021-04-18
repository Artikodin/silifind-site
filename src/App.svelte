<script>
  import Home from "./pages/Home.svelte";
  import Product from "./pages/Product.svelte";

  let component = "Home";
</script>

<div>
  {#if component === "Home"}
    <Home on:click={() => (component = "Product")} />
  {:else if component === "Product"}
    <Product />
  {/if}
</div>

<style>
  div {
    height: 100%;
  }
</style>
