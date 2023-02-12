<script>
  import { page } from "$app/stores";
  import NAVS from "../services/menu";
  import Close from "./Close.svelte";
  import Menu from "./Menu.svelte";

  $: menu = "";

  $: routeId = $page.route.id;
</script>

<header class="header">
  <nav class="navbar" id="nav">
    <img src="/img/gabi.jpg" alt="" />
    <ul>
      {#each NAVS as { href, title }}
        <li>
          <a {href} class:active={routeId === href} {title}>{title}</a>
        </li>
      {/each}
    </ul>
  </nav>

  <nav class="navbar-mobile" id="nav">
    <ul>
      {#each NAVS as { href, title, img }}
        <li>
          <a {href} class:active={routeId === href} {title}>
            <img src={img} alt={title} />
          </a>
          <p>{title}</p>
        </li>
      {/each}
    </ul>
  </nav>
</header>
