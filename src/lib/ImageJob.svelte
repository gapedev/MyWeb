<script>
  import Images from "../services/image";
</script>

<div class="container-job">
  {#each Images as { img, link }}
    <a href={link} target="_blank noreferrer">
      <div class="ImageJob" style="background-image:url({img})" />
    </a>
  {/each}
</div>
