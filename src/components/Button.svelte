<script>
  export let type = "button"
  export let clickHandler;
</script>

<button type={type} class={`button ${$$restProps.class}`} on:click|preventDefault={clickHandler} {...$$restProps}>
  <slot />
</button>

<style>
  .button {
    padding: 16px 32px;
    background-color: var(--secondary);
    color: #fff;
    border: none;
    letter-spacing: 1px;
  }
</style>