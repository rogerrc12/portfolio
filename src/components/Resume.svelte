<script>
  import Icon from '@iconify/svelte';
	import Education from './Education.svelte';
  import SubTitle from './SubTitle.svelte';
  import { skillsList } from '../data/skills';
	import Experience from './Experience.svelte';
	import Title from './Title.svelte';
	import Container from './Container.svelte';

  // ic:outline-star
</script>

<Container>
  <Title>Resume</Title>
  <div class="skills-container">
  <header class="header">
    <SubTitle>Mis habilidades</SubTitle>
    <p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.</p>
  </header>
  <article class="resume-section">
    <ul class="skills-list">
      {#each skillsList as skill}
        <li class="skill">
          <p>{skill.name}</p>
          <div class="skill-level">
            {#each Array(5).fill(0) as _, index}
              <Icon class="rating-icon" icon={(index >= skill.level && skill.level < 5) ? "ic:outline-star-outline" : "ic:outline-star"} />
            {/each}
          </div>
        </li>
      {/each}
    </ul>
  </article>
</div>
<div class="experience-container">
  <Education />
  <Experience />
</div>
</Container>

<style>
  .skills-container, .experience-container {
    display: flex;
    flex-direction: column;
  }

  .skills-container .header {
    margin-top: 1rem;
  }

  .skills-container .header p {
    margin-top: 0;
  }
  
  .resume-section {
    margin-top: 60px;
    background-color: var(--primary100);
    padding: 1rem 1.5rem;
    margin-bottom: 40px;
  }

  .skills-list {
    padding: 0;
    color: #fff;
  }

  .skill {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .skill p {
    font-size: 16px;
  }

  .skill-level {
    display: flex;
    align-items: center;
  }

  :global(.rating-icon) {
    font-size: 25px;
    color: var(--secondary)
  }

  @media screen and (min-width: 978px) {
    .skills-container, .experience-container {
      flex-direction: row;
      align-items: flex-start;
      gap: 10px;
    }

    .skills-container .header {
      padding: 0 2rem;
    }

    .resume-section {
      min-width: 50%;
    }

    .skills-list {
      padding: 0 2rem;
    }
  }
</style>

