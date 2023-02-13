<script>
  import Images from "../services/image";
</script>

<div class="container-job">
  {#each Images as { img }}
    <div class="ImageJob" style="background-image:url({img})">
      <div class="ImageJob_text">
        <h2>Hola</h2>
        <span>Hola holita</span>
      </div>
    </div>
  {/each}
</div>
