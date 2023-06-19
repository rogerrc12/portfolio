<script>
	import ProjectsList from "./Portfolio/ProjectsList.svelte";
	import Tabs from "./Tabs/Tabs.svelte";
import Title from "./Title.svelte";
import { portfolioList } from "../data/portfolio"
	import Container from "./Container.svelte";

const tabsItems = [
  {
    label: "Todos",
    value: 1,
    component: ProjectsList,
    props: { items: portfolioList }
  },
  {
    label: "Proyectos web",
    value: 2,
    component: ProjectsList,
    props: { items: portfolioList.filter(item => item.tags.includes("web")) }
  },
  {
    label: "Proyectos app",
    value: 3,
    component: ProjectsList,
    props: { items: portfolioList.filter(item => item.tags.includes("app")) }
  }
]
</script>

<section class="portfolio-section">
  <Container>
  <Title>Portafolio</Title>
  <article>
    <Tabs items={tabsItems} />
  </article>
</Container>
</section>

<style>
  .portfolio-section {
    padding: 4rem 1.5rem;
  }
</style>