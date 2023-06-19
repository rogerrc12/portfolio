<script>
	import Button from "./Button.svelte";
  import ImgProfile from "$lib/images/img-profile.jpeg"
  import Icon from '@iconify/svelte';
	import Container from "./Container.svelte";
</script>

<Container>
  <article class="banner">
  <header>
    <h3 class="subtitle">Desarrollador profesional</h3>
    <h1 class="title">Roger Rengifo</h1>
    <p class="description">Desarrollador de aplicaciones para web y mobile con más de 5 años de experiencia.</p>
    <div class="btn-wrapper">
      <Button>SOBRE MÍ</Button>
    </div>
  </header>
  <div class="img-wrapper">
    <img src={ImgProfile} alt="My profile" />
  </div>
  <ul class="info-list">
    <li class="info-item">
      <h4>Email</h4>
      <p>rogerreng.c@gmail.com</p>
    </li>
    <li class="info-item">
      <h4>Teléfono</h4>
      <p>+(51) 930 463 531</p>
    </li>
    <li class="info-item">
      <h4>Social media</h4>
      <div class="social-wrapper">
        <a class="icon-box" href="!#">
          <Icon class="social-icon" icon="ph:instagram-logo" />
        </a>
        <a class="icon-box" href="!#">
          <Icon class="social-icon" icon="ri:facebook-box-line" />
        </a>
        <a class="icon-box" href="!#">
          <Icon class="social-icon" icon="ph:linkedin-logo" />
        </a>
      </div>
    </li>
  </ul>
</article>
<div class="right-box" />
</Container>

<style>

  .banner {
    z-index: 1;
    position: relative;
  }

  .title, .subtitle {
    margin: 6px 0;
  }

  .subtitle {
    text-transform:  uppercase;
    letter-spacing: 6px;
    font-size: .9rem;
    line-height: 26px;
  }

  .title {
    margin: 10px 0;
    letter-spacing: 2px;
    font-size: 2.3rem;
  }

  .description {
    line-height: 1.7;
    max-width: 300px;
  }

  .btn-wrapper {
    margin-top: 32px;
  }

  .img-wrapper {
    width: 100%;
    max-width: 500px;
    margin-top: 32px;
  }

  img {
    width: 100%;
    object-fit: contain;
  }

  .info-list {
    list-style-type: none;
    padding: 0;
    margin-top: 20px;
  }

  .info-item {
    margin-bottom: 30px;
  }

  .info-item:last-child {
    margin-bottom: 0;
  }

  .info-item h4 {
    margin-bottom: 0;
    text-transform: uppercase;
    font-weight: 600;
    font-size: 14px;
  }

  .info-item p {
    font-size: 14px;
    margin-top: 10px;
    letter-spacing: 1.4px;
  }

  .social-wrapper {
    display: flex;
    align-items: center;
    margin-top: 10px;
  }

  .icon-box {
    padding: 8px;
    margin-right: 16px;
    border-radius: 50%;
    background-color: #fff;
    display: grid;
    place-items: center;
  }

  :global(.social-icon) {
    font-size: 24px;
    color: var(--secondary);
  }

  .right-box {
    display: none;
  }

  @media screen and (min-width: 978px) {
    .banner {
      display: flex;
      align-items: center;
    }

    .img-wrapper  {
      margin: 0 1.5rem;
    }

    .info-list {
      align-self: flex-end;
      margin-bottom: 0;
    }

    .title {
      font-size: 3rem;
      line-height: 60px;
    }
    .right-box {
      display: block;
      position: absolute;
      width: 50%;
      max-width: 800px;
      height: 85%;
      background-color: var(--secondary);
      right: 0;
      top: 0;
      z-index: 0;
    }
  }

  @media screen and (min-width: 1200px) {
    .img-wrapper  {
      margin-left: 3rem;
    }
  }
</style>