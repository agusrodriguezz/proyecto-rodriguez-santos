<script>
  let empresas = [
    {
      nombre: "Chevron",
      cantidad: 9,
      dueño: "Privado",
      marketCap: "$320B",
      emisiones: "680 Mt"
    },
    {
      nombre: "BP America",
      cantidad: 10,
      dueño: "Privado",
      marketCap: "$110B",
      emisiones: "760 Mt"
    },
    {
      nombre: "Shell USA",
      cantidad: 11,
      dueño: "Privado",
      marketCap: "$190B",
      emisiones: "810 Mt"
    },
    {
      nombre: "ExxonMobil",
      cantidad: 13,
      dueño: "Privado",
      marketCap: "$410B",
      emisiones: "940 Mt"
    },
    {
      nombre: "Gaz USA",
      cantidad: 14,
      dueño: "Gobierno",
      marketCap: "$75B",
      emisiones: "1020 Mt"
    },
    {
      nombre: "National Energy Corp",
      cantidad: 15,
      dueño: "Gobierno",
      marketCap: "$85B",
      emisiones: "1070 Mt"
    },
    {
      nombre: "Jinneng Energy USA",
      cantidad: 16,
      dueño: "Estatal",
      marketCap: "$60B",
      emisiones: "1120 Mt"
    },
    {
      nombre: "CHN Energy USA",
      cantidad: 20,
      dueño: "Estatal",
      marketCap: "$90B",
      emisiones: "1350 Mt"
    },
    {
      nombre: "Coal USA",
      cantidad: 20,
      dueño: "Gobierno",
      marketCap: "$95B",
      emisiones: "1340 Mt"
    },
    {
      nombre: "Aramco USA",
      cantidad: 24,
      dueño: "Estado",
      marketCap: "$1.9T",
      emisiones: "1480 Mt"
    }
  ];
  let maxHuellas = Math.max(...empresas.map(e => e.cantidad));
</script>

<div class="intro-wrapper">
  <h1 class="headline">Tu huella es irreversible si no actuas ahora</h1>
  <p class="subheadline" style="max-width: 800px; text-align: center; line-height: 1.4; margin: 0 auto;">
    Cada empresa deja una huella, conocerla es el primer paso para cambiarla.
  </p>
</div>

<div class="lines-wrapper">
  {#each empresas as empresa}
    <div class="isotype-line">
      
      <div class="tooltip-wrapper">
        <div class="label-empresa">
          {empresa.nombre}
        </div>
        <div class="tooltip">
          <strong style="color:#163747; font-weight:700;">{empresa.nombre}</strong><br />
          <span style="font-weight:600;">Dueño:</span> {empresa.dueño}<br />
          <span style="font-weight:600;">Market Cap:</span> {empresa.marketCap}<br />
          <span style="font-weight:600;">Emisiones:</span> {empresa.emisiones}
        </div>
      </div>

      <div class="isotype-list">
        {#each Array(maxHuellas + 1) as _, j}
          <div class="isotype-row huella-tooltip-wrapper">
            {#if j < empresa.cantidad}
              <img
                src="./imagenes/pie.svg"
                alt={`pie ${empresa.nombre}-${j + 1}`}
                class="iswotype-icon"
              />
              <div class="huella-tooltip">
                Huella {j + 1}: {2.5 * (j + 1)} millones de toneladas de CO₂
              </div>
            {:else if j === empresa.cantidad}
              <div class="cantidad-pies">
                {empresa.cantidad}
              </div>
            {:else}
              <div class="iswotype-icon" style="opacity: 0; visibility: hidden;"></div>
            {/if}
          </div>
        {/each}
      </div>

    </div>
  {/each}
</div>

<div class="leyenda-piecitos">
  <img src="./imagenes/pie.svg" alt="Huella de carbono" class="icono-piecito-leyenda">
  <span class="texto-leyenda">
    = 2,5 millones de toneladas ≈ emisiones anuales de 500.000 autos
  </span>
</div>

<section class="seccion-huella">
  <h2 class="seccion-huella-titulo">Pero... ¿qué es la huella de carbono?</h2>
  <div class="seccion-huella-video">
    <iframe width="100%" height="340" src="https://www.youtube.com/embed/8q7_aV8eLUE"
      title="¿Qué es la huella de carbono?" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
      encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</section>


<h2 class="graficos-titulo" style="text-align: center;">Veinte años de emisiones creciendo sin freno en Estados Unidos</h2>


<div class="graphics-section section-block" style="margin-bottom: 0px;">
  <div class="graphic-pair" style="max-width: 1200px; margin: 0 auto;">
    <div class="graphic-block">
      <h2 class="graphic-title">Emisiones en 2004</h2>
      <iframe 
        src='https://flo.uri.sh/visualisation/22632358/embed' 
        title='Mapa 2004' 
        class='flourish-embed-iframe' 
        frameborder='0' 
        scrolling='no' 
        style='width: 100%; height: 500px; display: block;'>
      </iframe>
    </div>

    <div class="graphic-block">
      <h2 class="graphic-title">Emisiones en 2024</h2>
      <iframe 
        src='https://flo.uri.sh/visualisation/22632623/embed' 
        title='Mapa 2024' 
        class='flourish-embed-iframe' 
        frameborder='0' 
        scrolling='no' 
        style='width: 100%; height: 500px; display: block;'>
      </iframe>
    </div>
  </div>

  <p class="aclaracion-graficos" style="font-size: 16px; margin-top: 10px; margin-bottom: 0px; text-align: center;">
    * Huellas de carbono por Región Oficial del Censo de EE.UU. – valores expresados en <strong>billones de toneladas de CO₂</strong>.
  </p>
</div>


<div class="graphic-text" style="margin: 10px auto 10px auto;"> 
  <p style="font-size: 22px; max-width: 1200px; margin: 0 auto; line-height: 1.5; text-align: justify;">
    Entre 2004 y 2024, la huella de carbono en EE. UU. aumentó. Pese a acuerdos y evidencia, las emisiones siguen creciendo, reflejando la insuficiencia de políticas, consumo y producción sostenibles.</p>
</div>

<div class="graphics-section" style="margin-top: 80px; width: 100%; text-align: center;">
  <h2 class="graphic-title" style="margin-top: 30px;">
    Una promesa verde convertida en humo
  </h2>

  <div style="width: 100%; max-width: 900px; margin: 20px auto 0; padding: 0;">
    <img src="./imagenes/grafico4.jpg" 
         alt="Gráfico Energía" 
         class="graphic-img" 
         style="width: 100%; height: auto; display: block; margin: 0 auto;">
  </div>

  <p class="aclaracion-graficos" style="font-size: 16px; margin-top: 8px; margin-bottom: 0px; text-align: center;">
    * Evolución de <strong>energía renovable</strong> y <strong>no renovable</strong> en EE.UU. (valores expresados en <strong>billones de toneladas de CO₂</strong>).
  </p>

  <div style="max-width: 1200px; margin: 30px auto 0;">
    <p class="graphic-description" style="font-size: 22px; line-height: 1.5; text-align: justify;">
      Desde 2019, cayó el uso de energías renovables y creció el de no renovables. En 2022, la brecha se duplicó, evidenciando una tendencia crítica y la urgencia de políticas sostenibles.
    </p>
  </div>
</div>


<section class="carbon-awareness">
  <h2 class="carbon-awareness-title">
    ¿Cómo se posiciona tu empresa frente al desafío climático?
  </h2>
  <p class="carbon-awareness-text">
    Medir el impacto ambiental es una acción responsable y apuesta por el futuro.<br>
    Entender tu huella es el primer paso hacia un cambio real.
  </p>
  <a
    class="carbon-awareness-button"
    href="https://www.carbonfootprint.com/calculator.aspx"
    target="_blank"
  >
    Medí tu huella de carbono ahora 🌱
  </a>
</section>

<footer class="footer-verde">
  <div class="footer-contenido">
    <p class="footer-nombres">
      <span>
        Agustín Rodríguez
        <a href="https://www.linkedin.com/in/agust%C3%ADn-rodriguez-7340b1270?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app  " target="_blank">
          <i class="fa-brands fa-linkedin" style="color: white; margin-left: 8px;"></i>
        </a>
        <a href="https://github.com/agusrodriguezz" target="_blank">
          <i class="fa-brands fa-square-github" style="color: white; margin-left: 4px;"></i>
        </a>
      </span>
      &nbsp;&nbsp;&nbsp;
      <span>
        Rafael Santos
        <a href="https://www.linkedin.com/in/rafael-santos-4b4463363/" target="_blank">
          <i class="fa-brands fa-linkedin" style="color: white; margin-left: 8px;"></i>
        </a>
        <a href="https://github.com/xrafasantos" target="_blank">
          <i class="fa-brands fa-square-github" style="color: white; margin-left: 4px;"></i>
        </a>
      </span>
    </p>

    <p class="footer-info">
      Visualización de Datos · Licenciatura en Tecnología Digital ·
      <a href="https://www.utdt.edu" target="_blank" style="color: white; text-decoration: underline;">Di Tella</a>
    </p>

    <p class="footer-final">2025 · Proyecto Huella de Carbono</p>
  </div>
</footer>