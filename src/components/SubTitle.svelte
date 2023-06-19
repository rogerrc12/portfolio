

<h3 class={`title ${$$restProps.class || ""}`}>
  <slot />
</h3>

<style>
  .title {
    font-size: 1.8rem;
    text-transform: capitalize;
    letter-spacing: 2px;
    margin-bottom: 60px;
  }

  .title:after {
    content: "";
    display: block;
    position: relative;
    top: 15px;
    background-color: #fff;
    height: 2px;
    width: 15%;
  }
</style>