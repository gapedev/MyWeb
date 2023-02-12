<script>
  import Aside from "$lib/Aside.svelte";
  import Header from "$lib/Header.svelte";
</script>

<div class="container">
  <div class="container_header">
    <Header />
  </div>
  <div class="container_content">
    <main>
      <slot />
    </main>
  </div>
  <div class="container_aside">
    <Aside />
  </div>
</div>
