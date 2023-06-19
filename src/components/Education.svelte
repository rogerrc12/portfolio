<script>
  import { educationList } from "../data/education"
	import SubTitle from "./SubTitle.svelte";
</script>

<article class="education">
  <SubTitle>Educación</SubTitle>
  <ul class="schools-list">
    {#each educationList as education}
      <li class="school">
        <p class="date">{education.year}</p>
        <h4>{education.school}</h4>
        <small>{education.address}</small>
      </li>
    {/each}
  </ul>
</article>

<style>
  .education {
    box-shadow: rgba(0,0,0,.1);
    padding: 2.2rem;
    background-color: var(--primary100);
    width: 100%;
    margin-bottom: 3rem;
  }

  .schools-list {
    padding: 0;
    list-style-type: none;
  }

  .school {
    padding: 12px 0 40px;
    border-bottom: 1px dashed #fff;
    margin: 12px 0;
  }

  .school:last-child {
    border-bottom: none;
  }

  .school h4 {
    font-size: 16px;
    font-family: 'Jost', 'Open Sans', 'Roboto', sans-serif;
    font-weight: 600;
    margin: 0;
    margin-bottom: 6px;
    letter-spacing: .7px;
    line-height: 1.8;
  }
  
  .date {
    margin-bottom: 8px;
    margin-top: 0;
    font-style: italic;
    font-size: 14px;
  }

  @media screen and (min-width: 978px) {
    .education {
      max-width: 550px;
      margin: 0 2rem 0 0;
    }
  }
</style>