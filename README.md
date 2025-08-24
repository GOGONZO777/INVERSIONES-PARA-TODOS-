<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Inversiones para Todos</title>
  <style>
    body {
      margin: 0; font-family: "Segoe UI", sans-serif;
      background: #f4f6f9; color: #333;
      scroll-behavior: smooth;
    }

    /* 🔹 Menú */
    nav {
      position: fixed;
      top: 0; width: 100%;
      background: #0066cc; color: white;
      display: flex; justify-content: center;
      gap: 2rem; padding: 1rem;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      z-index: 1000;
    }
    nav a {
      color: white; text-decoration: none;
      font-weight: bold; transition: 0.3s;
    }
    nav a:hover { color: #ffcc00; }

    header {
      text-align: center; padding: 6rem 1rem 3rem;
      background: linear-gradient(120deg, #0066cc, #00c6ff);
      color: white;
    }

    header h1 { font-size: 2.8rem; margin: 0; }
    header p { font-size: 1.2rem; }

    section {
      max-width: 1000px; margin: auto;
      padding: 3rem 1rem;
    }
    h2 { color: #0066cc; text-align: center; margin-bottom: 2rem; }

    /* 🔹 Tarjetas */
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }
    .card {
      background: white;
      border-radius: 15px;
      padding: 1.5rem;
      box-shadow: 0 3px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s;
      cursor: pointer;
    }
    .card:hover { transform: translateY(-5px); }
    .card h3 { margin-top: 0; color: #0066cc; }

    /* 🔹 Apartados ocultos */
    .details {
      display: none;
      margin-top: 1.5rem;
      padding: 1.5rem;
      background: #eaf4ff;
      border-left: 5px solid #0066cc;
      border-radius: 10px;
      animation: fadeIn 0.5s ease;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .close-btn {
      margin-top: 1rem;
      display: inline-block;
      padding: 0.5rem 1rem;
      background: #0066cc;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }
    .close-btn:hover {
      background: #ff4444;
    }

    /* 🔹 Consejo Millonario */
    .millonario {
      background: #fff7e6;
      border-left: 6px solid #ff9900;
      padding: 2rem;
      border-radius: 12px;
      box-shadow: 0 3px 12px rgba(0,0,0,0.1);
      margin-bottom: 2rem;
      text-align: center;
      font-size: 1.2rem;
    }
    .millonario h3 {
      color: #e67e00;
      margin-bottom: 1rem;
    }

    footer {
      background: #222; color: white;
      text-align: center; padding: 2rem; margin-top: 3rem;
    }
  </style>
</head>
<body>

  <!-- 🔹 Menú -->
  <nav>
    <a href="#planes">Planes</a>
    <a href="#millonario">Consejo Millonario</a>
    <a href="#consejos">Mejores Consejos</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <!-- 🔹 Encabezado -->
  <header>
    <h1>💰 Inversiones para Todos</h1>
    <p>Aprende a invertir de manera inteligente según tu edad</p>
  </header>

  <!-- 🔹 Planes -->
  <section id="planes">
    <h2>Planes según tu edad</h2>
    <div class="cards">

      <!-- 🔹 10-13 -->
      <div class="card" onclick="toggleDetails('detalle10')">
        <h3>👶 Jóvenes (10-13)</h3>
        <p>Primeros pasos en el ahorro.</p>
        <div id="detalle10" class="details">
          <h4>Consejos para 10-13 años</h4>
          <ul>
            <li>💡 Ahorra parte de tu mesada.</li>
            <li>📚 Lee libros básicos de finanzas.</li>
            <li>🐷 Usa una alcancía o app de ahorro.</li>
            <li>🎯 Meta: ahorrar para algo pequeño.</li>
          </ul>
          <button class="close-btn" onclick="closeDetails(event, 'detalle10')">Cerrar</button>
        </div>
      </div>

      <!-- 🔹 14-20 -->
      <div class="card" onclick="toggleDetails('detalle20')">
        <h3>👩‍💻 Jóvenes (14-20)</h3>
        <p>Empieza con inversiones seguras.</p>
        <div id="detalle20" class="details">
          <h4>Consejos para 14-20 años</h4>
          <ul>
            <li>💵 Abre una cuenta de ahorro estudiantil.</li>
            <li>📱 Usa apps de micro-inversión.</li>
            <li>📈 Aprende de acciones y criptos (con poco dinero).</li>
            <li>🎯 Meta: crear hábito de invertir.</li>
          </ul>
          <button class="close-btn" onclick="closeDetails(event, 'detalle20')">Cerrar</button>
        </div>
      </div>

      <!-- 🔹 21-35 -->
      <div class="card" onclick="toggleDetails('detalle35')">
        <h3>👨‍💼 Adultos jóvenes (21-35)</h3>
        <p>Expande tus oportunidades.</p>
        <div id="detalle35" class="details">
          <h4>Consejos para 21-35 años</h4>
          <ul>
            <li>🏠 Ahorra para tu primera propiedad.</li>
            <li>📊 Invierte en fondos y ETFs.</li>
            <li>🚀 Considera emprendimientos.</li>
            <li>🎯 Meta: construir patrimonio.</li>
          </ul>
          <button class="close-btn" onclick="closeDetails(event, 'detalle35')">Cerrar</button>
        </div>
      </div>

      <!-- 🔹 35+ -->
      <div class="card" onclick="toggleDetails('detalle55')">
        <h3>👴 Adultos 35+</h3>
        <p>Seguridad y estabilidad.</p>
        <div id="detalle55" class="details">
          <h4>Consejos para 35+ años</h4>
          <ul>
            <li>🔒 Plazos fijos y bonos.</li>
            <li>📑 Plan de jubilación.</li>
            <li>🏡 Refuerza con bienes raíces.</li>
            <li>🎯 Meta: tranquilidad económica.</li>
          </ul>
          <button class="close-btn" onclick="closeDetails(event, 'detalle55')">Cerrar</button>
        </div>
      </div>
    </div>
  </section>

  <!-- 🔹 Consejo Millonario -->
  <section id="millonario">
    <div class="millonario">
      <h3>💎 El mejor consejo para ser millonario</h3>
      <p><b>Invierte a largo plazo en activos que generen ingresos pasivos y reinvierte siempre las ganancias.</b>  
      La verdadera riqueza no se construye rápido, se construye con constancia, diversificación y paciencia.  
      Aprovecha el interés compuesto: deja que tu dinero trabaje para ti, todos los días, sin descanso. ⏳</p>
    </div>
  </section>

  <!-- 🔹 Consejos generales -->
  <section id="consejos">
    <h2>📌 Mejores Consejos Generales</h2>
    <div class="details" style="display:block;">
      <p>✔ Diversifica tus inversiones.<br>
      ✔ Invierte a largo plazo.<br>
      ✔ Nunca arriesgues lo que no puedes perder.<br>
      ✔ La educación financiera es tu mejor herramienta.</p>
    </div>
  </section>

  <!-- 🔹 Contacto -->
  <section id="contacto">
    <h2>📞 Contáctanos</h2>
    <p style="text-align:center;">
      ¿Tienes dudas? Escríbenos a:  
      <a href="mailto:kairosignis@gmail.com"><b>kairosignis@gmail.com</b></a>
    </p>
  </section>

  <footer>
    <p>© 2025 Inversiones para Todos - Educación financiera accesible</p>
  </footer>

  <!-- 🔹 Script -->
  <script>
    function toggleDetails(id) {
      const section = document.getElementById(id);
      section.style.display = (section.style.display === "block") ? "none" : "block";
    }
    function closeDetails(event, id) {
      event.stopPropagation(); // evita que se vuelva a abrir al hacer clic
      document.getElementById(id).style.display = "none";
    }
  </script>
</body>
</html>
