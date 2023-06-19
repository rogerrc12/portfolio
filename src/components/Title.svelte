<h2 class={`title ${$$restProps.class} ""}`}>
  <slot />
</h2>

<style>
  .title {
    text-transform: uppercase;
    font-size: 2.2rem;
    text-align: center;
    letter-spacing: 4px;
    line-height: 42px;
    margin-bottom: 50px;
  }

  .title::after {
    content: "";
    position: relative;
    top: 15px;
    display: block;
    width: 15%;
    margin: 0 auto;
    height: 2px;
    background-color: #fff;
  }

  @media screen and (min-width: 978px) {
    .title {
      font-size: 3rem;
      margin-bottom: 30px;
    }
  }
</style>