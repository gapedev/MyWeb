<script>
  import Github from "$lib/Github.svelte";
  import Linkedin from "$lib/Linkedin.svelte";
  import Title from "$lib/Title.svelte";
  import EDUCATION from "../../../services/education";
  import JOBS from "../../../services/jobs";
  import Html from "$lib/Html.svelte";
  import Css3 from "$lib/Css3.svelte";
  import Javascript from "$lib/Javascript.svelte";
  import Sass from "$lib/Sass.svelte";
  import Bulma from "$lib/Bulma.svelte";
  import React from "$lib/React.svelte";
  import Svelte from "$lib/Svelte.svelte";
  import Git from "$lib/Git.svelte";
  import Bitbucket from "$lib/Bitbucket.svelte";
  import Azure from "$lib/Azure.svelte";
</script>

<Title title="Currículum" />

<div class="curriculum">
  <div class="curriculum_left">
    <div class="curriculum_adress">
      <div class="curriculum_adress--title">
        <span>Gabi</span>
      </div>
      <div class="curriculum_adress--info">
        <p>
          <a href="mailto:gapedev@gmail.com" target="_blank noreferrer"
            >gapedev@gmail.com</a
          >
        </p>
        <p>
          <a href="https://gapedev.netlify.app/" target="_blank noreferrer"
            >https://gapedev.netlify.app/</a
          >
        </p>
        <p>601 06 87 78</p>
      </div>
    </div>
    <div class="curriculum_img">
      <img src="/img/gabi.jpg" alt="" />
    </div>
    <div class="curriculum_text">
      <h4>Sobre Mí</h4>
      <p>
        +5 años de experiencia en desarrollo web, utlizando distintas
        tecnologías. He ayudado a construir marcas desde 0, y he tenido contacto
        con el cliente, dándole consejo y adaptando la web como él quiere. Por
        supuesto todo en un entorno responsive, y buenas prácticas para su
        posicionamiento.
      </p>
      <h2>Gabriel Pérez Licerán</h2>
      <span>Desarrollador Front-End</span>
    </div>
    <div class="curriculum_rrss">
      <div class="curriculum_item">
        <div class="curriculum_rrss--icon">
          <Github />
        </div>
        <div class="curriculum_rrss--text">
          <p><a href="">https://github.com/gapedev</a></p>
        </div>
      </div>
      <div class="curriculum_item">
        <div class="curriculum_rrss--icon">
          <Linkedin />
        </div>
        <div class="curriculum_rrss--text">
          <p>
            <a href=""
              >https://www.linkedin.com/in/gabriel-p%C3%A9rez-licer%C3%A1n-b0826a14b/</a
            >
          </p>
        </div>
      </div>
      <div class="curriculum_item">
        <div class="curriculum_rrss--icon">
          <img src="img/icons/device-desktop.svg" alt="" />
        </div>
        <div class="curriculum_rrss--text">
          <p>
            <a href="">www.demomento.com</a>
          </p>
        </div>
      </div>
    </div>
  </div>
  <div class="curriculum_right">
    <div class="curriculum_title">
      <div class="curriculum_title--name">Gabi Pérez Licerán</div>
      <div class="curriculum_title--position">Front-End Developer</div>
    </div>
    <div class="curriculum_job">
      <div class="curriculum_job--container">
        <h2>Formación</h2>
        {#each EDUCATION as { date, academy, course }}
          <div class="curriculum_job--education">
            <span>{date}</span>
            <p>{academy}</p>
            <p>{course}</p>
          </div>
        {/each}
      </div>
      <div class="curriculum_job--container">
        <h2>Experiencia</h2>
        {#each JOBS as { date, position, company, text, link }}
          <div class="curriculum_job--jobs">
            <span>{date}</span>
            <p>{position}</p>
            <p>
              Compañía | <a target="_blank norereferr" href={link}>{company}</a>
            </p>
            <span>{text}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="curriculum_stack">
      <h2>Stack Tecnológico</h2>
      <div class="curriculum_icons">
        <div class="curriculum_icons--items">
          <p>Html5</p>
          <Html />
        </div>
        <div class="curriculum_icons--items">
          <p>Css3</p>
          <Css3 />
        </div>
        <div class="curriculum_icons--items">
          <p>Sass</p>
          <Sass />
        </div>
        <div class="curriculum_icons--items">
          <p>Javascript</p>
          <Javascript />
        </div>
        <div class="curriculum_icons--items">
          <p>Bulma</p>
          <Bulma />
        </div>
      </div>
      <div class="curriculum_icons">
        <div class="curriculum_icons--items">
          <p>React</p>
          <React />
        </div>
        <div class="curriculum_icons--items">
          <p>Svelte</p>
          <Svelte />
        </div>
        <div class="curriculum_icons--items">
          <p>Git</p>
          <Git />
        </div>
        <div class="curriculum_icons--items">
          <p>Bitbucket</p>
          <Bitbucket />
        </div>
        <div class="curriculum_icons--items">
          <p>Azure</p>
          <Azure />
        </div>
      </div>
    </div>
  </div>
</div>
