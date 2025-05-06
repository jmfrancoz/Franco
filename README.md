<!DOCTYPE html>
<html lang="es" x-data="{ tab: 'inicio' }" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>asistIA Legal</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
  <style>
    .fade-in {
      animation: fadeIn 1.5s ease-in-out forwards;
    }
    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body class="bg-gray-900 text-white" x-init="$el.classList.add('fade-in')">

  <!-- PORTADA -->
  <section class="relative bg-cover bg-center h-screen" style="background-image: url('https://unsplash.com/es/fotos/mujer-sosteniendo-la-estatua-de-la-espada-durante-el-dia-DZpc4UY8ZtY');">
    <div class="absolute inset-0 bg-blue bg-opacity-100"></div>
    <div class="relative z-10 flex flex-col items-center justify-center h-full text-center px-6">
      <h1 class="text-5xl md:text-6xl font-extrabold mb-4 text-white">ASISTIA LEGAL</h1>
      <p class="text-lg md:text-2xl max-w-3xl text-gray-200 leading-relaxed mb-8">
        Abogados expertos. IA jurídica instantánea.<br>
        Todo en un solo lugar. Todo para ti.
      </p>
      <nav class="flex flex-col md:flex-row gap-4 text-lg font-semibold">
        <button @click="tab = 'inicio'" class="bg-white text-black px-6 py-3 rounded hover:bg-gray-200">Inicio</button>
        <button @click="tab = 'copilot'" class="bg-white text-black px-6 py-3 rounded hover:bg-gray-200">Copilot Jurídico</button>
        <button @click="tab = 'abogados'" class="bg-white text-black px-6 py-3 rounded hover:bg-gray-200">Buscar Abogados</button>
        <button @click="tab = 'registro'" class="bg-white text-black px-6 py-3 rounded hover:bg-gray-200">Registro</button>
      </nav>
    </div>
  </section>

  <!-- SECCIÓN DE INICIO -->
  <section x-show="tab === 'inicio'" class="p-6 transition-fade">
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-6 mb-10">
      <!-- Misión -->
      <div class="bg-white text-gray-900 p-6 rounded-lg shadow-xl">
        <h3 class="text-xl font-bold mb-2">Misión</h3>
        <p>Democratizar el acceso a la justicia mediante soluciones tecnológicas e innovadoras que conecten personas con expertos jurídicos de manera accesible, rápida y ética.</p>
      </div>
      <!-- Visión -->
      <div class="bg-white text-gray-900 p-6 rounded-lg shadow-xl">
        <h3 class="text-xl font-bold mb-2">Visión</h3>
        <p>Ser la plataforma legal más confiable y utilizada en América Latina, combinando IA y talento humano para garantizar la defensa de los derechos de todos.</p>
      </div>
    </div>

    <!-- Quiénes somos y por qué escogernos -->
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-6">
      <div class="bg-gray-800 p-6 rounded-lg shadow-inner">
        <h3 class="text-xl font-bold mb-2 text-white">¿Quiénes somos?</h3>
        <p class="text-gray-300">Un equipo multidisciplinario de desarrolladores, abogados y emprendedores que trabaja por una justicia más eficiente, digital y cercana a la ciudadanía.</p>
      </div>
      <div class="bg-blue-800 p-6 rounded-lg shadow-inner">
        <h3 class="text-xl font-bold mb-2 text-white">¿Por qué escogernos?</h3>
        <ul class="text-white space-y-2">
          <li>✔ IA entrenada en derecho colombiano</li>
          <li>✔ Abogados verificados con trayectoria</li>
          <li>✔ Asistencia 24/7 desde cualquier lugar</li>
          <li>✔ Sistema de reseñas y comunidad activa</li>
        </ul>
      </div>
    </div>

    <!-- Noticias -->
    <div class="max-w-6xl mx-auto mt-12">
      <h2 class="text-2xl font-bold mb-6">Noticias legales recientes en Colombia</h2>
      <div class="grid md:grid-cols-3 gap-6">
        <template x-for="(noticia, index) in [
          {
            img: 'https://www.eltiempo.com/files/article_main/uploads/2024/01/20/65abb9f44566b.jpeg',
            titulo: 'Corte Constitucional emite fallo sobre derechos digitales',
            descripcion: 'Se reconoce protección especial a los datos personales como derecho fundamental.'
          },
          {
            img: 'https://www.semana.com/resizer/1VVAKrJG6JIM3O3b9L59uT5AT_Y=/1200x0/filters:format(jpg):quality(70)/cloudfront-us-east-1.images.arcpublishing.com/semana/L7XZTYWN7BG7ZP2T4Y35MGITWY.jpg',
            titulo: 'Nuevo código penal juvenil es aprobado',
            descripcion: 'El Congreso redefine sanciones para menores y promueve modelos de reintegración.'
          },
          {
            img: 'https://www.elespectador.com/resizer/KzixTfGpgqD_EFbg64nPdkNkxwU=/arc-anglerfish-arc2-prod-elespectador/public/DTTBP2TGTVGGJAA7ZTVA6QEQAI.jpg',
            titulo: 'Avanza reforma a la justicia en Colombia',
            descripcion: 'Se plantea una nueva estructura para reducir tiempos judiciales y mejorar acceso.'
          }
        ]" :key="index">
          <div class="bg-white text-gray-900 rounded-lg overflow-hidden shadow-lg">
            <img :src="noticia.img" class="w-full h-48 object-cover">
            <div class="p-4">
              <h3 class="font-bold text-lg" x-text="noticia.titulo"></h3>
              <p class="text-sm mt-2" x-text="noticia.descripcion"></p>
            </div>
          </div>
        </template>
      </div>
    </div>
  </section>

</body>
</html>
  <!-- COPILOTO JURÍDICO -->
<!-- COPILOTO JURÍDICO CON GEMINI -->
<section x-show="tab === 'copilot'" class="transition-fade bg-gray-900 text-white py-16">
  <div class="max-w-5xl mx-auto px-6 text-center">
    <h2 class="text-4xl md:text-5xl font-extrabold mb-6">Copiloto Jurídico AsistIA</h2>
    <p class="text-lg text-gray-300 mb-8">
      Describe tu situación legal y recibe orientación instantánea con inteligencia artificial de Google Gemini.
    </p>

    <div x-data="copilotoIA()" class="bg-white rounded-lg shadow-xl p-6 md:p-10 text-gray-900">
      <label for="consulta" class="block text-lg font-semibold mb-2">¿En qué podemos ayudarte hoy?</label>
      <textarea x-model="consulta" id="consulta" rows="5" class="w-full p-4 rounded border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500 resize-none transition" placeholder="Ej. ¿Cómo puedo solicitar una pensión de sobreviviente en Colombia?"></textarea>

      <button @click="consultarGemini" :disabled="cargando || !consulta" class="mt-6 w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded transition">
        <template x-if="!cargando">
          <span>Consultar con Gemini</span>
        </template>
        <template x-if="cargando">
          <span>Consultando...</span>
        </template>
      </button>

      <div x-show="respuesta" class="mt-6 bg-gray-100 p-4 rounded text-left border border-gray-300">
        <h4 class="font-bold text-lg mb-2">Respuesta:</h4>
        <p x-text="respuesta" class="text-gray-800 whitespace-pre-line"></p>
      </div>
    </div>

    <!-- Características adicionales -->
    <div class="mt-12 grid md:grid-cols-3 gap-6">
      <div class="bg-blue-800 bg-opacity-90 p-6 rounded-lg shadow text-left">
        <h3 class="text-xl font-bold mb-2 text-white">Velocidad & Precisión</h3>
        <p class="text-gray-300">Gemini responde en segundos con base en derecho colombiano.</p>
      </div>
      <div class="bg-blue-700 bg-opacity-90 p-6 rounded-lg shadow text-left">
        <h3 class="text-xl font-bold mb-2 text-white">Privacidad</h3>
        <p class="text-gray-300">Tu consulta se trata de forma confidencial y segura.</p>
      </div>
      <div class="bg-blue-600 bg-opacity-90 p-6 rounded-lg shadow text-left">
        <h3 class="text-xl font-bold mb-2 text-white">IA Verificada</h3>
        <p class="text-gray-300">Supervisada por abogados reales para garantizar calidad jurídica.</p>
      </div>
    </div>
  </div>

  <!-- ALPINE SCRIPT -->
  <script>
    function copilotoIA() {
      return {
        consulta: '',
        respuesta: '',
        cargando: false,
        apiKey: 'AIzaSyCVOy7Vt7YGrRm0Bm_UtR3aOwWHcE17lpg', // Clave API de Google Gemini

        async consultarGemini() {
          this.cargando = true;
          this.respuesta = '';

          const endpoint = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${this.apiKey}`;

          const payload = {
            contents: [{
              parts: [{ text: this.consulta }]
            }]
          };

          try {
            const res = await fetch(endpoint, {
              method: 'POST',
              headers: {
                'Content-Type': 'application/json'
              },
              body: JSON.stringify(payload)
            });

            const data = await res.json();
            const output = data.candidates?.[0]?.content?.parts?.[0]?.text;

            this.respuesta = output || 'La IA no pudo generar una respuesta clara. Intenta reformular tu consulta.';
          } catch (error) {
            console.error('Error con la API de Gemini:', error);
            this.respuesta = 'Ocurrió un error al procesar la consulta. Intenta más tarde.';
          }

          this.cargando = false;
        }
      }
    }
  </script>
</section>


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
               { nombre: 'Laura Gómez', especialidad: 'Penal', experiencia: 8, ciudad: 'Bogotá', calificacion: 4.9, reseñas: 12, foto: 'images/abogado1.jpg' },
               { nombre: 'Carlos Méndez', especialidad: 'Laboral', experiencia: 5, ciudad: 'Medellín', calificacion: 4.7, reseñas: 8, foto: 'images/abogado2.jpg' },
               { nombre: 'Ana Ruiz', especialidad: 'Civil', experiencia: 6, ciudad: 'Cali', calificacion: 4.8, reseñas: 10, foto: 'images/abogado3.jpg' },
               { nombre: 'Santiago Pérez', especialidad: 'Familia', experiencia: 4, ciudad: 'Bogotá', calificacion: 4.6, reseñas: 6, foto: 'images/abogado4.jpg' },
               { nombre: 'Paula Moreno', especialidad: 'Penal', experiencia: 3, ciudad: 'Barranquilla', calificacion: 4.5, reseñas: 4, foto: 'images/abogado5.jpg' },
               { nombre: 'Julian Restrepo', especialidad: 'Civil', experiencia: 7, ciudad: 'Medellín', calificacion: 4.7, reseñas: 9, foto: 'images/abogado6.jpg' }
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
            <img x-bind:src="abogado.foto" x-bind:alt="'Foto de ' + abogado.nombre" class="w-full h-48 object-cover rounded mb-3">
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
      <p class="mb-4">¿Eres abogado y quieres ofrecer tus servicios en nuestra plataforma? Completa el siguiente formulario:</p>
      
      <form class="grid md:grid-cols-2 gap-4">
        <div>
          <label class="block mb-1 font-medium">Nombre completo</label>
          <input type="text" class="w-full border rounded p-2" required>
        </div>
        <div>
          <label class="block mb-1 font-medium">Número de tarjeta profesional</label>
          <input type="text" class="w-full border rounded p-2" required>
        </div>
        <div>
          <label class="block mb-1 font-medium">Especialidad principal</label>
          <select class="w-full border rounded p-2" required>
            <option value="">Seleccione...</option>
            <option>Derecho Penal</option>
            <option>Derecho Civil</option>
            <option>Derecho Laboral</option>
            <option>Derecho de Familia</option>
          </select>
        </div>
        <div>
          <label class="block mb-1 font-medium">Años de experiencia</label>
          <input type="number" class="w-full border rounded p-2" min="1" required>
        </div>
        <div>
          <label class="block mb-1 font-medium">Correo electrónico</label>
          <input type="email" class="w-full border rounded p-2" required>
        </div>
        <div>
          <label class="block mb-1 font-medium">Teléfono de contacto</label>
          <input type="tel" class="w-full border rounded p-2" required>
        </div>
        <div class="md:col-span-2">
          <label class="block mb-1 font-medium">Breve descripción profesional</label>
          <textarea class="w-full border rounded p-2" rows="3" required></textarea>
        </div>
        <div class="md:col-span-2">
          <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">Enviar solicitud</button>
        </div>
      </form>
    </div>
  </section>

  <footer class="bg-gray-100 text-center text-sm text-gray-600 p-4 mt-10">
    <p>&copy; 2025 asistIA Legal. Todos los derechos reservados.</p>
    <p class="mt-2">
      <a href="#" class="hover:underline">Términos de servicio</a> | 
      <a href="#" class="hover:underline">Política de privacidad</a> | 
      <a href="#" class="hover:underline">Contáctanos</a>
    </p>
  </footer>
</body>
</html>
