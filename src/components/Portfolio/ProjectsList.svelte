<script>
	import Container from "./Container.svelte";

  export let items = []
</script>


  <Container>
    {#each items as item}
    <div class="item">
      <div class="item-content">
        <h4>{item.title}</h4>
      <a href={item.link} rel="noreferrer" target="_blank">Ver proyecto</a>
      </div>
      <div class="item-image">
        <img src={item.image} alt={item.title} />
      </div>
    </div>
    {/each}
  </Container>

<style>
  .item {
    position: relative;
  }

  .item-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: absolute;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, .3);
    transition: all 450ms ease-out;
    opacity: 0;
  }

  .item-content h4 {
    font-size: 20px;
    line-height: 22px;
    font-weight: 600;
    margin: 0;
    margin-bottom: 10px;
  }

  .item-content a {
    color: #fff;
    text-decoration: none;
    letter-spacing: .6px;
  }

  .item:hover .item-content {
    opacity: 1;
    transform: scale(.95);
  }

  .item-image {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden
  }

  .item-image img {
    min-width: 100%;
    min-height: 100%
  }
</style>