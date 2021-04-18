<script>
  import Footer from "./Footer.svelte";
  import Header from "./Header.svelte";
</script>

<div>
  <Header />
  <main>
    <slot />
  </main>
  <Footer />
</div>

<style>
  div {
    height: 100%;
    width: 100%;
    position: relative;
    overflow: hidden;
  }

  main {
    height: 100%;
    overflow: scroll;
  }
</style>
