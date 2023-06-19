<script>
  let shown = false

  function toggleNav() {
    shown = !shown
  }
</script>

<header class="header">
  <div class="header-wrapper" class:shown={shown}>
    <h1 class="logo">RR</h1>
    <button class="nav-btn" on:click="{toggleNav}">
      <span />
      <span />
      <span />
      <span />
    </button>
    <nav class="navigation">
      <ul>
        <li><a href="!#">Acerca</a></li>
        <li><a href="!#">Experiencia</a></li>
        <li><a href="!#">Portafolio</a></li>
        <li><a href="!#">contacto</a></li>
      </ul>
    </nav>
    <div class="nav-bg" />
  </div>
</header>

<style>
  .header {
    box-shadow: 2px 2px 1px rgba(200, 200, 200, .1);
    height: 9.5vh;
    z-index: 100;
    width: 100%;
    background-color: var(--primary);
    position: -webkit-sticky;
	  position: sticky;
	  top: 0;
  }

  .header-wrapper {
    max-width: 1400px;
    height: 100%;
    margin:  0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    padding: 0 24px;
  }

  .logo {
    font-weight: lighter;
    padding: 8px;
    border: 2px solid #fff;
    font-size: 1.3rem;
  }

  .nav-bg {
    top: 0;
    right: 0;
    position: fixed;
    z-index: 9;
    width: 0;
    height: 0;
    margin: 30px 0 20px 20px;
    background: radial-gradient(circle, var(--secondary), var(--secondary));
    border-radius: 50%;
    transition: 350ms ease;
  }

  .navigation {
    display: none;
    position: fixed;
    right: 20px;
    top: 4.5rem;
    z-index: 10;
  }


  .shown .navigation {
    display: block;
  }

  .shown .nav-bg {
    width: 520px;
    height: 480px;
    transform: translate(55%,-20%);
  }

  .navigation ul {
    list-style-type: none;
    padding: 0;
  }

  .navigation ul li a {
    display: inline-block;
    padding: .75rem 1rem;
    width: 100%;
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.3rem;
  }

  .nav-btn {
    background-color: transparent;
    border: none;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 25px;
    height: 25px;
    position: relative;
    z-index: 11;
    cursor: pointer;
  }

  .nav-btn span {
    height: 2px;
    background-color: #fff;
    width: 100%;
    display: inline-block;
    position: absolute;
    transition: 350ms linear;
  }

  .nav-btn span:first-child {
    top: 2px;
    left: 0;
  }

  .nav-btn span:nth-child(2) {
    top: 8px;
    left: 0;
  }

  .nav-btn span:nth-child(3) {
    top: 15px;
    left: 0;
  }

  .nav-btn span:last-child {
    bottom: 2px;
    left: 0;
  }

  .shown .nav-btn span:nth-child(2), .shown .nav-btn span:nth-child(3) {
    opacity: 0;
  }

  .shown .nav-btn span:first-child {
    transform: rotate(45deg) translateY(15px);
    top: 0;
  }

  .shown .nav-btn span:last-child {
    transform: rotate(-45deg) translateY(-17.5px);
    bottom: 0;
    left: 1px;
  }

  @media screen and (min-width: 978px) {
    .nav-btn, .nav-bg {
      display: none;
    } 

    .navigation {
      display: block;
      position: static;
    }

    .navigation ul {
      display: flex;
      align-items: center;
    }

    .navigation ul li a {
      font-size: 1.05rem;
    }
  }
</style>