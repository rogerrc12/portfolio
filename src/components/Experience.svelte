<script>
	import SubTitle from "./SubTitle.svelte";
  import { experienceList } from "../data/experience"

</script>
<article>
  <SubTitle>Experiencia</SubTitle>
  <ul class="experience-list">
    {#each experienceList as experience}
      <li class="experience-item">
        <div class="date-wrapper">
          <span class="date">{experience.year}</span>
          <h4 class="company">{experience.company}</h4>
        </div>
        <div class="desc-wrapper">
          <h5 class="job-tiitle">{experience.title}</h5>
          <p>{experience.description}</p>
        </div>
      </li>
    {/each}
  </ul>
</article>

<style>
  article {
    padding: 2rem;
    background-color: var(--primary100);
  }

  .experience-list {
    padding: 0;
  }

  .experience-item {
    margin-top: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
  }

  .date-wrapper {
    padding-right: 16px;
    width: 100%;
    max-width: 150px;
  }

  .desc-wrapper {
    padding-left: 32px;
    border-left: 1px dashed #fff; 
  }

  .date {
    font-size: 14px;
    font-style: italic;
  }

  .company {
    margin-top: 10px;
    font-weight: 700;
    font-size: 14px;
    letter-spacing: .6px;
  }

  .job-tiitle {
    font-size: 19px;
    letter-spacing: .6px;
    margin-bottom: 8px;
    margin-top: 0;
  }

  .desc-wrapper p {
    font-size: 14px;
    margin-bottom: 0;
    white-space: pre-line;
  }
</style>