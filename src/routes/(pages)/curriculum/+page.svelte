<script>
  import Title from "$lib/Title.svelte";
  import EDUCATION from "../../../services/education";
  import JOBS from "../../../services/jobs";
</script>

<Title title="Currículum" />

<div class="curriculum">
  <div class="curriculum_left">
    <div class="curriculum_adress">
      <div class="curriculum_adress--title">
        <span>Gabi</span>
      </div>
      <div class="curriculum_adress--info">
        <p><a href="">gapedev@gmail.com</a></p>
        <p><a href="">www.demomento.com</a></p>
        <p>Palma de Mallorca</p>
      </div>
    </div>
    <div class="curriculum_img">
      <img src="/static/img/gabi.jpg" alt="" />
    </div>
    <div>3</div>
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
    <div>3</div>
  </div>
</div>
