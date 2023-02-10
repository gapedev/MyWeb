<script>
  import { page } from "$app/stores";
  import NAVS from "../services/menu";
  import Close from "./Close.svelte";
  import Menu from "./Menu.svelte";

  $: menu = "";

  $: routeId = $page.route.id;
</script>

<header class="header">
  <nav class="navbar container" id="nav">
    <ul>
      <img src="/img/gabi.jpg" alt="" />
      {#each NAVS as { href, title }}
        <li>
          <a {href} class:active={routeId === href} {title}>{title}</a>
        </li>
      {/each}
    </ul>
    <a class="nav_hamburger" href="#nav">
      <Menu />
    </a>
    <a class="nav_close" href="#">
      <Close />
    </a>
  </nav>
</header>
