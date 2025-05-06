<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>asistIA Legal</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
  <style>
    html {
      scroll-behavior: smooth;
    }
    .transition-fade {
      transition: opacity 0.5s ease-in-out;
    }
  </style>
</head>
<body class="bg-gray-900 text-white" x-data="{ tab: 'inicio', expanded: {} }">
  <header class="bg-black bg-opacity-90 text-white shadow-lg sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-6 py-4 flex flex-col md:flex-row items-center justify-between">
      <div class="flex items-center space-x-4">
        <div class="bg-blue-500 text-white rounded-full p-2">
          <svg class="h-8 w-8" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M8 10h.01M12 10h.01M16 10h.01M9 16h6m2 4H7a2 2 0 01-2-2V6a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V18a2 2 0 01-2 2z"/>
          </svg>
        </div>
        <div>
          <h1 class="text-3xl font-bold">asistIA Legal</h1>
          <p class="text-sm text-gray-300">Orientación jurídica automatizada y confiable</p>
        </div>
      </div>
      <nav class="flex flex-wrap gap-3 mt-4 md:mt-0 text-sm font-medium">
        <button @click="tab = 'inicio'" class="hover:underline">Inicio</button>
        <button @click="tab = 'copilot'" class="hover:underline">Copilot Jurídico</button>
        <button @click="tab = 'abogados'" class="hover:underline">Buscar Abogados</button>
        <button @click="tab = 'registro'" class="hover:underline">Registro de Abogados</button>
      </nav>
    </div>
  </header>

  <!-- INICIO + POR QUÉ ESCOGERNOS -->
  <section x-show="tab === 'inicio'" class="p-6 transition-fade">
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-6">
      <div class="bg-white text-gray-900 p-6 rounded-lg shadow-xl">
        <h2 class="text-2xl font-bold mb-2">Bienvenido a asistIA Legal</h2>
        <p class="mb-4">En asistIA Legal, combinamos la inteligencia artificial con la experiencia humana para ofrecerte asesoría jurídica confiable, instantánea y especializada en Colombia.</p>
        <h3 class="font-bold mt-4 mb-2">Misión</h3>
        <p class="mb-2">Democratizar el acceso a la justicia mediante soluciones tecnológicas e innovadoras que conecten personas con expertos jurídicos de manera accesible, rápida y ética.</p>
        <h3 class="font-bold mb-2">Visión</h3>
        <p class="mb-2">Ser la plataforma legal más confiable y utilizada en América Latina, combinando IA y talento humano para garantizar la defensa de los derechos de todos.</p>
        <h3 class="font-bold mb-2">¿Quiénes somos?</h3>
        <p>Un equipo de desarrolladores, abogados y emprendedores apasionados por transformar la justicia a través de la tecnología, creando herramientas que empoderen a la ciudadanía.</p>
      </div>
      <div class="bg-blue-800 text-white p-6 rounded-lg shadow-inner">
        <h3 class="text-xl font-bold mb-2">¿Por qué escogernos?</h3>
        <ul class="space-y-3">
          <li><strong>✔ Especialización:</strong> IA entrenada en derecho colombiano + abogados expertos reales.</li>
          <li><strong>✔ Velocidad:</strong> Tu respuesta en segundos. No más filas ni esperas telefónicas.</li>
          <li><strong>✔ Confianza:</strong> Todos los profesionales son verificados. La IA es supervisada por juristas.</li>
          <li><strong>✔ Accesibilidad:</strong> Disponible 24/7 desde cualquier lugar y dispositivo.</li>
          <li><strong>✔ Comunidad:</strong> Reseñas reales y transparencia en cada perfil de abogado.</li>
        </ul>
      </div>
    </div>

    <!-- Portal de noticias -->
    <div class="max-w-6xl mx-auto mt-10">
      <h2 class="text-2xl font-bold mb-4">Noticias legales recientes en Colombia</h2>
      <div class="grid md:grid-cols-3 gap-4">
        <div class="bg-white text-gray-900 p-4 rounded-lg shadow">
          <img src="https://www.eltiempo.com/files/article_main/uploads/2024/01/20/65abb9f44566b.jpeg" alt="Noticias legales" class="rounded mb-2">
          <h3 class="font-bold">Corte Constitucional emite fallo histórico sobre derechos digitales</h3>
          <p class="text-sm">La Corte reconoce los datos personales como parte del núcleo esencial del derecho a la intimidad.</p>
        </div>
        <div class="bg-white text-gray-900 p-4 rounded-lg shadow">
          <img src="https://www.semana.com/resizer/1VVAKrJG6JIM3O3b9L59uT5AT_Y=/1200x0/filters:format(jpg):quality(70)/cloudfront-us-east-1.images.arcpublishing.com/semana/L7XZTYWN7BG7ZP2T4Y35MGITWY.jpg" alt="Noticias justicia" class="rounded mb-2">
          <h3 class="font-bold">Nuevo código penal juvenil es aprobado en el Congreso</h3>
          <p class="text-sm">La ley redefine sanciones y promueve la resocialización de menores en conflicto con la ley.</p>
        </div>
        <div class="bg-white text-gray-900 p-4 rounded-lg shadow">
          <img src="https://www.elespectador.com/resizer/KzixTfGpgqD_EFbg64nPdkNkxwU=/arc-anglerfish-arc2-prod-elespectador/public/DTTBP2TGTVGGJAA7ZTVA6QEQAI.jpg" alt="Reforma legal" class="rounded mb-2">
          <h3 class="font-bold">Reforma al sistema judicial avanza en segunda vuelta</h3>
          <p class="text-sm">Se busca mejorar tiempos procesales, aumentar acceso y eficiencia en la administración de justicia.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONSULTORIO JURÍDICO -->
  <section x-show="tab === 'copilot'" class="p-6 transition-fade">
    <div class="bg-white text-gray-900 shadow rounded-lg p-6 max-w-4xl mx-auto">
      <h2 class="text-xl font-bold mb-4">Consultorio Jurídico asistIA Legal</h2>
      <p class="mb-4">Haz tu consulta jurídica directamente con nuestro asistente Gemini entrenado para Colombia:</p>
      <textarea id="pregunta" class="w-full border rounded-lg p-2 mb-4" rows="4" placeholder="Escribe tu consulta jurídica aquí..."></textarea>
      <button onclick="consultarGemini()" class="bg-blue-700 text-white px-4 py-2 rounded hover:bg-blue-800">Consultar</button>
      <div id="respuesta" class="mt-4 text-gray-800 whitespace-pre-line"></div>
    </div>
  </section>

  <script>
    async function consultarGemini() {
      const pregunta = document.getElementById("pregunta").value;
      const respuestaDiv = document.getElementById("respuesta");
      respuestaDiv.textContent = "Consultando con Gemini...";

      try {
        const response = await fetch("https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=AIzaSyCVOy7Vt7YGrRm0Bm_UtR3aOwWHcE17lpg", {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify({
            contents: [{ parts: [{ text: pregunta }], role: "user" }]
          })
        });

        const data = await response.json();
        const respuestaIA = data.candidates?.[0]?.content?.parts?.[0]?.text || "No se pudo obtener una respuesta.";
        respuestaDiv.textContent = respuestaIA;
      } catch (error) {
        respuestaDiv.textContent = "Error al contactar la API: " + error.message;
      }
    }
  </script>

  <!-- LISTADO DE ABOGADOS -->
  <section x-show="tab === 'abogados'" class="p-6 transition-fade">
  <div class="max-w-7xl mx-auto text-white">
    <h2 class="text-3xl font-bold mb-6">Directorio de Abogados</h2>

    <!-- Filtros y búsqueda -->
    <div class="bg-gray-800 p-4 rounded-lg mb-6 grid md:grid-cols-4 gap-4 text-black">
      <input x-model="searchName" placeholder="Buscar por nombre" class="p-2 rounded w-full" type="text">
      <select x-model="filterEspecialidad" class="p-2 rounded w-full">
        <option value="">Todas las especialidades</option>
        <option value="Penal">Derecho Penal</option>
        <option value="Civil">Derecho Civil</option>
        <option value="Laboral">Derecho Laboral</option>
        <option value="Familia">Derecho de Familia</option>
      </select>
      <select x-model="filterExperiencia" class="p-2 rounded w-full">
        <option value="">Años de experiencia</option>
        <option value="1">+1 año</option>
        <option value="3">+3 años</option>
        <option value="5">+5 años</option>
        <option value="10">+10 años</option>
      </select>
      <select x-model="filterCiudad" class="p-2 rounded w-full">
        <option value="">Todas las ciudades</option>
        <option value="Bogotá">Bogotá</option>
        <option value="Medellín">Medellín</option>
        <option value="Cali">Cali</option>
        <option value="Barranquilla">Barranquilla</option>
      </select>
    </div>

    <!-- Listado de abogados -->
    <div class="grid md:grid-cols-3 gap-6"
         x-data="{
           searchName: '',
           filterEspecialidad: '',
           filterExperiencia: '',
           filterCiudad: '',
           abogados: [
             { nombre: 'Laura Gómez', especialidad: 'Penal', experiencia: 8, ciudad: 'Bogotá', calificacion: 4.9, reseñas: 12 },
             { nombre: 'Carlos Méndez', especialidad: 'Laboral', experiencia: 5, ciudad: 'Medellín', calificacion: 4.7, reseñas: 8 },
             { nombre: 'Ana Ruiz', especialidad: 'Civil', experiencia: 6, ciudad: 'Cali', calificacion: 4.8, reseñas: 10 },
             { nombre: 'Santiago Pérez', especialidad: 'Familia', experiencia: 4, ciudad: 'Bogotá', calificacion: 4.6, reseñas: 6 },
             { nombre: 'Paula Moreno', especialidad: 'Penal', experiencia: 3, ciudad: 'Barranquilla', calificacion: 4.5, reseñas: 4 },
             { nombre: 'Julian Restrepo', especialidad: 'Civil', experiencia: 7, ciudad: 'Medellín', calificacion: 4.7, reseñas: 9 },
             { nombre: 'Camila Torres', especialidad: 'Laboral', experiencia: 10, ciudad: 'Bogotá', calificacion: 5.0, reseñas: 14 },
             { nombre: 'Andrés Rodríguez', especialidad: 'Familia', experiencia: 2, ciudad: 'Cali', calificacion: 4.3, reseñas: 3 },
             { nombre: 'Mariana Quintero', especialidad: 'Penal', experiencia: 9, ciudad: 'Bogotá', calificacion: 4.8, reseñas: 11 },
             { nombre: 'Felipe Díaz', especialidad: 'Civil', experiencia: 12, ciudad: 'Medellín', calificacion: 4.9, reseñas: 15 }
           ]
         }"
    >
      <template x-for="abogado in abogados.filter(a => 
        (!searchName || a.nombre.toLowerCase().includes(searchName.toLowerCase())) &&
        (!filterEspecialidad || a.especialidad === filterEspecialidad) &&
        (!filterExperiencia || a.experiencia >= parseInt(filterExperiencia)) &&
        (!filterCiudad || a.ciudad === filterCiudad)
      )" :key="abogado.nombre">
        <div class="bg-white text-gray-900 rounded-lg p-4 shadow-lg hover:shadow-2xl transition">
          <h3 class="text-xl font-bold mb-1" x-text="abogado.nombre"></h3>
          <p class="text-sm text-gray-600" x-text="'Especialidad: ' + abogado.especialidad"></p>
          <p class="text-sm text-gray-600" x-text="'Experiencia: ' + abogado.experiencia + ' años'"></p>
          <p class="text-sm text-gray-600" x-text="'Ciudad: ' + abogado.ciudad"></p>
          <p class="text-sm text-yellow-600 font-bold mt-2" x-text="'⭐ ' + abogado.calificacion + ' (' + abogado.reseñas + ' reseñas)'"></p>
          <button class="mt-3 bg-blue-600 text-white py-1 px-3 rounded hover:bg-blue-700 transition">Ver perfil</button>
        </div>
      </template>
    </div>
  </div>
</section>
  <!-- REGISTRO DE ABOGADOS -->
  <section x-show="tab === 'registro'" class="p-6 transition-fade">
    <div class="max-w-5xl mx-auto bg-white text-gray-900 p-6 rounded-lg shadow-lg">
      <h2 class="text-2xl font-bold mb-4">Registro de Abogados</h2>
      <p class="mb-4">¿Eres abogado y quieres ofrecer tus servicios en nuestra plataforma? Completa el siguiente formulario y nuestro equipo validará tu perfil.</p>
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdK_doAR23lKia09FjztRxr3rZNA6xHfhT2d-gLusvjw3PfOg/viewform?embedded=true" width="900" height="800" frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>
    </div>
  </section>

</body>
</html>

<footer class="bg-gray-100 text-center text-sm text-gray-600 p-4 mt-10">
    <p>&copy; 2025 asistIA Legal. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
