<div class="items-container">
  <slot />
</div>

<style>
  .items-container {
    display: grid;
    align-items: center;
    grid-template-columns: repeat(auto-fit, minmax(275px, 1fr));
    gap: 20px;
  }
</style>