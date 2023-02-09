<script>
  import Aside from "$lib/Aside.svelte";
  import Header from "$lib/Header.svelte";
</script>

<div class="body-container">
  <Header />
  <Aside />
  <main class="main">
    <slot />
  </main>
</div>

<style>
  .body-container {
    display: grid;
    grid-template-columns: 0.6fr 2.2fr 0.2fr;
    grid-template-rows: 1fr 0fr 0fr;
    gap: 0px 0px;
    grid-auto-flow: row;
    grid-template-areas:
      "header content aside"
      "header content aside"
      "header content aside";
  }
</style>
