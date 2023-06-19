<script>
	import Button from "./Button.svelte";
  import ProfileImg from "$lib/images/profile-2.jpeg"
	import Container from "./Container.svelte";
  import SpanishCV from "$lib/docs/cv-spanish.pdf"

  const handleDownloadCV = () => {
    // fetch("/docs/cv-spanish.pdf")
    // .then(res => res.blob())
    // .then(console.log)
    // .catch(console.log)

    let hidden_a = document.createElement("a");
    hidden_a.setAttribute("href", SpanishCV)
    hidden_a.setAttribute("download", "")
    document.body.appendChild(hidden_a)
    hidden_a.click()
  }

</script>

<div class="bg-box">
<Container>
  <div class="about-container">
  <div class="profile-wrapper">
    <img src={ProfileImg} alt="myself">
  </div>
  <article class="section">
    <header class="title-wrapper">
        <h2 class="title">Roger Rengifo</h2>
        <h5 class="subtitle">Soy Especialista en desarrollo <strong>frontend, mobile y fullstack</strong> por más de 5 años</h5>
    </header>
    <h3 class="section-title">Acerca de mi</h3>
    <p>He generado experiencia en diversos proyectos dentro de los sectores de finanzas, comida, medicina y seguros. Mi ha sido crear como Tech-Lead y frontend developer una fintech importante en Peru llamada Instakash SAC, manejando un equipo de 4 personas. Me gusta trabajar mi código de manera concisa y ordenada para facil mantenimiento y actualización. Soy una persona siempre abierta a trabajar con equipos y amoldarme a las caracteristicas y funciones de la empresa.</p>
    <Button clickHandler={handleDownloadCV}>Descargar CV</Button>
  </article>
</div>
</Container>
<div class="left-box" />
</div>

<style>
  .bg-box {
    position: relative;
    margin: 6rem 0;
  }

  .about-container {
    z-index: 1;
    position: relative;
  }

  .title {
    font-size: 2rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 10px;
  }

  .subtitle {
    font-size: 1.2rem;
    font-weight: 400;
    margin-top: 0;
    line-height: 1.6;
  }

  .profile-wrapper {
    max-width: 400px;
  }
  
  .profile-wrapper img {
    width: 100%;
  }

  .section-title {
    color: var(--secondary);
    text-transform: uppercase;
    margin-bottom: 30px;
  }

  .section-title::after {
    content: "";
    display: block;
    width: 15%;
    height: 2px;
    position: relative;
    top: 10px;
    background-color: var(--secondary);
  }

  article p {
    margin-bottom: 40px;
  }

  .left-box {
    display: none;
  }

  @media screen and (min-width: 978px) {
    .about-container {
      display: flex;
      align-items: center;
      gap: 3rem;
      padding: 1rem 0;
    }

    .profile-wrapper {
      min-width: 400px;
      width: 100%;
    }

    .left-box {
      width: 35%;
      max-width: 700px;
      background-color: var(--secondary);
      height: 100%;
      position: absolute;
      left: 0;
      top: 0;
      display: block;
      z-index: 0;
    }
  }
</style>