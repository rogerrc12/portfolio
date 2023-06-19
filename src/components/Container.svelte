<section class={`section ${$$restProps.class || ""}`}>
  <slot />
</section>

<style>
  .section {
    padding: 3rem 1.5rem;
    margin: 0 auto;
  }

  @media screen and (min-width: 400px) {
    .section {
      max-width: 768px;
    }
  }

  @media screen and (min-width: 978px) {
    .section {
      max-width: 1140px;
    }
  }

  @media screen and (min-width: 1200px) {
    .section {
      max-width: 1320px;
    }
  }
</style>