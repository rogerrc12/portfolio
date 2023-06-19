<script>
  import Icon from "@iconify/svelte";
  import ContactForm from "./ContactForm.svelte";
  import Container from "./Container.svelte";
  import SubTitle from "./SubTitle.svelte";
  import Title from "./Title.svelte"
</script>

<Container>
  <Title>Contáctame</Title>
  <div class="contact-wrapper">
  <header class="header">
    <SubTitle class="title">Salúdame!</SubTitle>
    <p>Siempre estoy dispuesto a participar en proyectos y apoyar desde mi conocimiento  personas y empresas.</p>
    <div class="item">
      <div class="icon-wrapper">
        <Icon icon="bi:phone" class="contact-icon" />
      </div>
      <div>
        <h4 class="item-title">Llámame</h4>
        <a href="tel:+51930463531">+(51) 930 463 531</a>
      </div>
    </div>
    <div class="item">
      <div class="icon-wrapper">
        <Icon icon="ic:outline-mail" class="contact-icon" />
      </div>
      <div>
        <h4 class="item-title">Enviame un mail</h4>
        <a href="mailto:+rogerreng.c@gmail.com">rogerreng.c@gmail.com</a>
      </div>
    </div>
  </header>
  <article>
    <div class="form-wrapper">
      <ContactForm />
    </div>
  </article>
</div>
</Container>

<style>
  .contact-wrapper {
    display: flex;
    flex-direction: column;
    margin-top: 2rem;
  }

  .header :global(.title) {
    margin-bottom: 45px;
  }

  .header p {
    margin-top: 0;
    margin-bottom: 30px;
  }
  
  .item {
    display: flex;
    align-items: center;
    margin-bottom: 2.6rem;
  }

  .icon-wrapper {
    background-color: var(--primary100);
    padding: 1rem;
    border-radius: 50%;
    margin-right: 1rem;
  }

  :global(.contact-icon) {
    font-size: 34px;
    color: var(--secondary)
  }
  .item-title {
    font-size: 20px;
    margin: 0 0 6px;
    text-transform: capitalize;
  }

  .item a {
    color: #fff;
    text-decoration: none;
    font-size: 16px;
  }

  .form-wrapper {
    margin-top: 2rem;
    width: 100%
  }

  @media screen and (min-width: 978px) {
    .contact-wrapper {
      flex-direction: row;
      align-items: center;
    }

    .header {
      min-width: 50%;
      padding: 0 2rem;
    }
  }
</style>