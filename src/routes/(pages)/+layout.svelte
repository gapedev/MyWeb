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
