<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>acces.a — Diseño sin barreras</title>

  <meta
    name="description"
    content="Una guía visual e interactiva para diseñar experiencias digitales más accesibles."
  >

  <style>
    :root {
      --background: #f5f4f0;
      --surface: #ffffff;
      --text: #111111;
      --muted: #66645f;
      --line: #d8d6cf;
      --accent: #2557ff;
      --accent-soft: #e8edff;

      --max-width: 1180px;
      --radius: 18px;
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      background: var(--background);
      color: var(--text);

      font-family:
        Inter,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;

      font-size: 16px;
      line-height: 1.6;
      letter-spacing: 0;
    }

    a {
      color: inherit;
    }

    a:focus-visible,
    button:focus-visible {
      outline: 3px solid var(--accent);
      outline-offset: 4px;
    }

    .container {
      width: min(
        calc(100% - 48px),
        var(--max-width)
      );

      margin-inline: auto;
    }

    /* HEADER */

    header {
      padding: 32px 0;
      border-bottom: 1px solid var(--line);
    }

    nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .logo {
      font-size: 24px;
      font-weight: 800;
      letter-spacing: -0.05em;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 24px;

      font-size: 14px;
    }

    .nav-links a {
      text-decoration: none;
    }

    .nav-links a:hover {
      text-decoration: underline;
      text-underline-offset: 4px;
    }

    /* HERO */

    .hero {
      min-height: 76vh;

      display: grid;
      align-items: end;

      padding: 90px 0 70px;
    }

    .eyebrow {
      margin-bottom: 24px;

      font-size: 12px;
      font-weight: 700;
      letter-spacing: 0.14em;
      text-transform: uppercase;

      color: var(--muted);
    }

    h1 {
      max-width: 900px;

      margin: 0;

      font-size: clamp(4rem, 11vw, 9rem);
      line-height: 0.86;
      letter-spacing: -0.065em;
      font-weight: 750;
    }

    .hero-copy {
      max-width: 570px;

      margin: 42px 0 0;

      font-size: clamp(1.15rem, 2vw, 1.6rem);
      line-height: 1.25;
      letter-spacing: -0.025em;
    }

    .hero-meta {
      display: flex;
      justify-content: space-between;
      gap: 32px;

      margin-top: 80px;
      padding-top: 20px;

      border-top: 1px solid var(--text);

      font-size: 13px;
    }

    /* SECTIONS */

    section {
      padding: 100px 0;
      border-top: 1px solid var(--line);
    }

    .section-grid {
      display: grid;
      grid-template-columns: 0.8fr 2fr;
      gap: 80px;
    }

    .number {
      font-size: 14px;
      color: var(--muted);
    }

    h2 {
      margin: 0 0 28px;

      font-size: clamp(2.4rem, 5vw, 5rem);
      line-height: 0.95;
      letter-spacing: -0.055em;
    }

    h3 {
      margin: 0 0 12px;

      font-size: 20px;
      line-height: 1.15;
      letter-spacing: -0.025em;
    }

    p {
      max-width: 700px;
      margin: 0 0 20px;
    }

    .lead {
      font-size: 22px;
      line-height: 1.4;
      color: #343330;
    }

    /* PRINCIPLES */

    .principles {
      display: grid;
      grid-template-columns: repeat(4, 1fr);

      margin-top: 60px;

      border-top: 1px solid var(--line);
      border-left: 1px solid var(--line);
    }

    .principle {
      min-height: 260px;

      padding: 28px;

      background: var(--surface);

      border-right: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
    }

    .principle-index {
      display: block;

      margin-bottom: 70px;

      color: var(--muted);
      font-size: 13px;
    }

    /* FEATURES */

    .feature-list {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1px;

      margin-top: 50px;

      background: var(--line);
      border: 1px solid var(--line);
    }

    .feature {
      min-height: 170px;
      padding: 28px;
      background: var(--surface);
    }

    .feature span {
      display: block;

      margin-bottom: 38px;

      color: var(--accent);
      font-size: 13px;
      font-weight: 700;
    }

    /* SPECS */

    .spec-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;

      margin-top: 50px;
    }

    .spec-card {
      padding: 28px;

      background: var(--surface);
      border: 1px solid var(--line);
      border-radius: var(--radius);
    }

    .spec-value {
      display: block;

      margin: 28px 0 6px;

      font-size: 44px;
      line-height: 1;
      letter-spacing: -0.05em;
    }

    /* CODE */

    pre {
      overflow-x: auto;

      margin: 24px 0 0;
      padding: 28px;

      border-radius: var(--radius);

      background: #111;
      color: #f7f7f5;

      font-family:
        "SFMono-Regular",
        Consolas,
        monospace;

      font-size: 14px;
      line-height: 1.65;
    }

    code {
      font-family:
        "SFMono-Regular",
        Consolas,
        monospace;
    }

    /* PROMPTS */

    .prompts {
      display: grid;
      gap: 16px;

      margin-top: 50px;
    }

    .prompt {
      padding: 30px;

      background: var(--surface);
      border: 1px solid var(--line);
      border-radius: var(--radius);
    }

    .prompt-number {
      display: block;

      margin-bottom: 30px;

      color: var(--accent);
      font-size: 13px;
      font-weight: 700;
    }

    /* CTA */

    .portfolio {
      background: #111;
      color: #fff;
    }

    .portfolio .section-grid {
      align-items: end;
    }

    .portfolio p {
      color: #bcbcb8;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;

      min-height: 52px;

      margin-top: 22px;
      padding: 0 24px;

      background: #fff;
      color: #111;

      border-radius: 999px;

      text-decoration: none;
      font-weight: 650;
      letter-spacing: -0.01em;
    }

    .button:hover {
      background: #e8e8e4;
    }

    /* FOOTER */

    footer {
      padding: 38px 0;

      background: #111;
      color: #fff;

      border-top: 1px solid #333;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 30px;

      font-size: 13px;
      color: #bcbcb8;
    }

    /* MOBILE */

    @media (max-width: 800px) {

      .container {
        width: min(
          calc(100% - 40px),
          var(--max-width)
        );
      }

      header {
        padding: 24px 0;
      }

      .nav-links {
        display: none;
      }

      .hero {
        min-height: auto;
        padding: 72px 0 52px;
      }

      h1 {
        font-size: clamp(4rem, 20vw, 6.5rem);
        letter-spacing: -0.055em;
      }

      .hero-copy {
        margin-top: 34px;
      }

      .hero-meta {
        flex-direction: column;
        gap: 8px;

        margin-top: 60px;
      }

      section {
        padding: 72px 0;
      }

      .section-grid {
        grid-template-columns: 1fr;
        gap: 30px;
      }

      .principles,
      .spec-grid {
        grid-template-columns: 1fr;
      }

      .feature-list {
        grid-template-columns: 1fr;
      }

      .principle {
        min-height: auto;
      }

      .principle-index {
        margin-bottom: 42px;
      }

      .footer-inner {
        flex-direction: column;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      html {
        scroll-behavior: auto;
      }

      *,
      *::before,
      *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="container">
    <nav aria-label="Navegación principal">

      <div class="logo">
        acces.a
      </div>

      <div class="nav-links">
        <a href="#proyecto">Proyecto</a>
        <a href="#principios">Principios</a>
        <a href="#specs">Specs</a>
        <a href="#codigo">Código</a>
        <a href="#prompts">Prompts IA</a>
      </div>

    </nav>
  </div>
</header>


<main>

  <!-- HERO -->

  <section class="hero" id="proyecto">
    <div class="container">

      <div class="eyebrow">
        UI/UX · Accesibilidad · Diseño inclusivo
      </div>

      <h1>
        Diseño<br>
        sin barreras.
      </h1>

      <p class="hero-copy">
        Una guía visual e interactiva para diseñar
        experiencias digitales más accesibles.
      </p>

      <div class="hero-meta">
        <span>Macarena Ramdohr</span>
        <span>UI/UX Designer</span>
        <span>2026</span>
      </div>

    </div>
  </section>


  <!-- SOBRE EL PROYECTO -->

  <section>
    <div class="container section-grid">

      <div class="number">
        01 / Proyecto
      </div>

      <div>
        <h2>
          La accesibilidad también se diseña.
        </h2>

        <p class="lead">
          acces.a explora cómo pequeñas decisiones de diseño
          pueden hacer que una interfaz sea más fácil de
          percibir, comprender y utilizar.
        </p>

        <p>
          El proyecto no busca únicamente hablar sobre
          accesibilidad. La propia interfaz funciona como
          demostración.
        </p>

        <p>
          Contraste, tipografía, navegación por teclado,
          estados de foco, áreas táctiles y preferencias
          visuales pueden explorarse directamente desde
          la experiencia.
        </p>
      </div>

    </div>
  </section>


  <!-- PRINCIPIOS -->

  <section id="principios">
    <div class="container">

      <div class="section-grid">

        <div class="number">
          02 / POUR
        </div>

        <div>
          <h2>
            Cuatro principios.
          </h2>

          <p class="lead">
            Una experiencia accesible debe ser perceptible,
            operable, comprensible y robusta.
          </p>
        </div>

      </div>


      <div class="principles">

        <article class="principle">
          <span class="principle-index">01</span>

          <h3>Perceptible</h3>

          <p>
            La información debe poder percibirse
            de diferentes maneras.
          </p>
        </article>


        <article class="principle">
          <span class="principle-index">02</span>

          <h3>Operable</h3>

          <p>
            La interfaz debe funcionar con diferentes
            métodos de interacción.
          </p>
        </article>


        <article class="principle">
          <span class="principle-index">03</span>

          <h3>Comprensible</h3>

          <p>
            El contenido y las interacciones deben
            ser claros y predecibles.
          </p>
        </article>


        <article class="principle">
          <span class="principle-index">04</span>

          <h3>Robusto</h3>

          <p>
            La experiencia debe funcionar con diferentes
            tecnologías de asistencia.
          </p>
        </article>

      </div>

    </div>
  </section>


  <!-- EXPLORA -->

  <section>
    <div class="container section-grid">

      <div class="number">
        03 / Guía
      </div>

      <div>

        <h2>
          ¿Qué puedes explorar?
        </h2>

        <div class="feature-list">

          <div class="feature">
            <span>01</span>
            <h3>Contraste de color</h3>
          </div>

          <div class="feature">
            <span>02</span>
            <h3>Jerarquía tipográfica</h3>
          </div>

          <div class="feature">
            <span>03</span>
            <h3>Navegación por teclado</h3>
          </div>

          <div class="feature">
            <span>04</span>
            <h3>Estados de foco</h3>
          </div>

          <div class="feature">
            <span>05</span>
            <h3>Formularios accesibles</h3>
          </div>

          <div class="feature">
            <span>06</span>
            <h3>Texto alternativo</h3>
          </div>

          <div class="feature">
            <span>07</span>
            <h3>Movimiento reducido</h3>
          </div>

          <div class="feature">
            <span>08</span>
            <h3>HTML semántico</h3>
          </div>

        </div>

      </div>
    </div>
  </section>


  <!-- SPECS -->

  <section id="specs">
    <div class="container">

      <div class="section-grid">

        <div class="number">
          04 / Specs
        </div>

        <div>

          <h2>
            Números que importan.
          </h2>

          <p class="lead">
            Algunas referencias útiles para construir
            interfaces más cómodas y legibles.
          </p>

        </div>
      </div>


      <div class="spec-grid">

        <article class="spec-card">
          <h3>Texto base</h3>
          <span class="spec-value">16px</span>
          <p>
            Un punto de partida cómodo para contenido
            de lectura.
          </p>
        </article>


        <article class="spec-card">
          <h3>Contraste AA</h3>
          <span class="spec-value">4.5:1</span>
          <p>
            Referencia WCAG para texto normal.
          </p>
        </article>


        <article class="spec-card">
          <h3>Touch target</h3>
          <span class="spec-value">44px</span>
          <p>
            Referencia cómoda para controles táctiles.
          </p>
        </article>

      </div>

    </div>
  </section>


  <!-- CODIGO -->

  <section id="codigo">
    <div class="container section-grid">

      <div class="number">
        05 / Código
      </div>

      <div>

        <h2>
          Listo para pegar.
        </h2>

        <p class="lead">
          Algunos patrones pueden incorporarse directamente
          en un proyecto.
        </p>


        <h3>Focus visible</h3>

        <pre><code>:focus-visible {
  outline: 3px solid #2557ff;
  outline-offset: 4px;
}</code></pre>


        <h3 style="margin-top: 50px;">
          Reduced motion
        </h3>

        <pre><code>@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}</code></pre>


        <h3 style="margin-top: 50px;">
          Skip link
        </h3>

        <pre><code>&lt;a href="#contenido" class="skip-link"&gt;
  Saltar al contenido
&lt;/a&gt;</code></pre>

      </div>

    </div>
  </section>


  <!-- PROMPTS -->

  <section id="prompts">
    <div class="container section-grid">

      <div class="number">
        06 / IA
      </div>

      <div>

        <h2>
          Revisa tu proyecto con IA.
        </h2>

        <p class="lead">
          Tres prompts para detectar, corregir y comprobar
          problemas de accesibilidad.
        </p>


        <div class="prompts">

          <article class="prompt">

            <span class="prompt-number">
              PROMPT 01
            </span>

            <h3>
              Auditoría de accesibilidad
            </h3>

            <p>
              Analiza esta interfaz utilizando WCAG 2.2
              como referencia. Identifica problemas de
              contraste, navegación por teclado, foco,
              semántica, formularios, imágenes, tipografía,
              áreas táctiles y movimiento.
            </p>

          </article>


          <article class="prompt">

            <span class="prompt-number">
              PROMPT 02
            </span>

            <h3>
              Corrige mi interfaz
            </h3>

            <p>
              Revisa el siguiente HTML, CSS y JavaScript.
              Corrige los problemas de accesibilidad
              encontrados manteniendo la identidad visual
              y estructura general del proyecto.
            </p>

          </article>


          <article class="prompt">

            <span class="prompt-number">
              PROMPT 03
            </span>

            <h3>
              Genera un plan QA
            </h3>

            <p>
              Crea un plan de pruebas de accesibilidad
              que incluya teclado, lector de pantalla,
              zoom, contraste, móvil, reducción de
              movimiento y diferentes tamaños de viewport.
            </p>

          </article>

        </div>

      </div>
    </div>
  </section>


  <!-- PORTFOLIO -->

  <section class="portfolio">
    <div class="container section-grid">

      <div class="number">
        07 / Designer
      </div>

      <div>

        <h2>
          Diseñado por<br>
          Macarena Ramdohr.
        </h2>

        <p class="lead">
          UI/UX Designer · Digital Designer
        </p>

        <p>
          Diseño interfaces donde identidad visual,
          tecnología y experiencia de usuario puedan
          convivir sin añadir complejidad innecesaria.
        </p>

        <!-- REEMPLAZA # CON TU URL REAL -->
        <a
          class="button"
          href="#"
          target="_blank"
          rel="noopener noreferrer"
        >
          Ver portafolio en Behance →
        </a>

      </div>

    </div>
  </section>

</main>


<footer>
  <div class="container footer-inner">

    <strong>
      acces.a
    </strong>

    <span>
      Diseño sin barreras.
    </span>

    <span>
      Macarena Ramdohr © 2026
    </span>

  </div>
</footer>

</body>
</html>
