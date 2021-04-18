<script>
  import PageLayout from "../components/PageLayout.svelte";
  import ProductList from "../components/ProductList.svelte";
  import CaptationLayout from "../components/CaptationLayout.svelte";
</script>

<PageLayout>
  <CaptationLayout />
  <ProductList on:click />
</PageLayout>
