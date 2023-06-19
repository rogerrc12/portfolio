<div class="tab">
  <slot />
</div>

<style>
  .tab {
    display: grid;
    align-items: center;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr))
  }
</style>