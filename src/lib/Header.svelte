<script>
  import { page } from "$app/stores";

  const LINKS = [
    {
      href: "/",
      title: "Home",
    },
    {
      href: "/about",
      title: "Sobre Mí",
    },
    {
      href: "/curriculum",
      title: "Currículum",
    },
    {
      href: "/portfolio",
      title: "Portfolio",
    },
    {
      href: "/proyectos",
      title: "Proyectos",
    },
    {
      href: "/contacto",
      title: "Contacto",
    },
  ];

  $: routeId = $page.route.id;
</script>

<div class="header">
  <div class="header_img">
    <img src="/img/gabi.jpg" alt="Foto de Gabriel Pérez Licerán" />
  </div>
  <div class="header_menu">
    <nav>
      <ul>
        {#each LINKS as { href, title }}
          <li>
            <a {href} class:active={routeId === href} {title}>{title}</a>
          </li>
        {/each}
      </ul>
    </nav>
  </div>
</div>
