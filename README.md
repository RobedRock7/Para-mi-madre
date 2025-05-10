# Para-mi-madre
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Para mamá</title>
    <style>
      body {
        margin: 0;
        background: #f9f4f1;
        font-family: "Georgia", serif;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
      }

      .sobre-contenedor {
        position: relative;
        width: 350px;
        height: 220px;
        perspective: 1000px;
        cursor: pointer;
      }

      .sobre {
        position: relative;
        width: 100%;
        height: 100%;
        background: #fff;
        border: 2px solid #e8cfc2;
        border-radius: 8px;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        transition: box-shadow 0.3s ease;
      }

      .sobre:hover {
        box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
      }

      .solapa {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 60%;
        background: #f8d6cc;
        clip-path: polygon(0 0, 50% 100%, 100% 0);
        transform-origin: top;
        transition: transform 1s ease;
        z-index: 3;
      }

      .mensaje-frente {
        position: absolute;
        bottom: 10px;
        width: 100%;
        text-align: center;
        font-size: 1.2em;
        color: #aa4a44;
        font-style: italic;
        z-index: 2;
        transition: opacity 0.5s ease;
      }

      .sobre.abierto .mensaje-frente {
        opacity: 0;
      }

      .carta {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        height: 100%;
        background: #fff;
        padding: 20px;
        box-sizing: border-box;
        transition: top 1s ease;
        z-index: 1;
        overflow-y: auto;
      }

      .sobre.abierto .solapa {
        transform: rotateX(-180deg);
      }

      .sobre.abierto .carta {
        top: 0;
      }

      .carta h2 {
        text-align: center;
        color: #b24c47;
        margin-top: 0;
      }

      .carta p {
        text-align: justify;
        line-height: 1.6;
        margin-bottom: 12px;
      }

      .firma {
        text-align: right;
        font-style: italic;
        margin-top: 20px;
        color: #b24c47;
      }
    </style>
  </head>
  <body>
    <div class="sobre-contenedor" onclick="abrirSobre()">
      <div class="sobre" id="sobre">
        <div class="solapa"></div>
        <div class="mensaje-frente">Para la mejor madre del mundo 💖</div>
        <div class="carta">
          <h2>Querida Mamá</h2>
          <p>
            Hoy quiero tomarme un momento para agradecerte por todo lo que has
            hecho por mí a lo largo de los años. Tu amor, paciencia y fortaleza
            han sido una guía constante que me ha ayudado a crecer y convertirme
            en la persona que soy hoy. No hay palabras suficientes para expresar
            lo agradecido que estoy por tenerte como mi madre.
          </p>
          <p>
            Recuerdo todos esos días en los que estuviste a mi lado cuando más
            te necesito, incluso cuando estabas cansada o preocupada. Siempre
            tienes el tiempo para escucharme, aconsejarme y darme un abrazo que
            lo curaba todo. Eres mi ejemplo de entrega, de cariño incondicional
            y de valentía ante cualquier dificultad.
          </p>
          <p>
            Gracias por enseñarme y seguir haciéndolo, el valor del respeto, el
            trabajo duro y la empatía. Tus enseñanzas están presentes en cada
            decisión que tomo y en la forma en la que trato a los demás. Eres el
            corazón de nuestra familia y la razón por la que nuestro hogar
            siempre ha sido un lugar de amor y apoyo.
          </p>
          <p>
            Te amo con todo mi corazón, mamá. En este día especial y todos los
            días, quiero que sepas cuánto significas para mí. Espero poder
            devolverte aunque sea una pequeña parte de todo lo que me has dado.
            ¡Feliz Día de las Madres!
          </p>
          <div class="firma">
            Con todo mi cariño,<br />Tu hijo(José Berrospe)
          </div>
        </div>
      </div>
    </div>

    <script>
      function abrirSobre() {
        document.getElementById("sobre").classList.toggle("abierto");
      }
    </script>
  </body>
</html>
