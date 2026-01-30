<script setup>
  const titulos = ['Curso', 'Universidad', 'Año', 'Certificado']

  const cursos = [
  {
    nombre: 'Python-Fundamentos de Programacion',
    enlace: 'https://drive.google.com/file/d/15eNXdiS7vP4vg1OZBxFegkiiXsaxlm2W/view?usp=sharing',
    universidad: 'Universidad Nacional de Ingenieria',
    anio: '2023',
    imagen: 'src/imagenes/img1.png'
  },
  {
    nombre: 'Algoritmos y estrutura de datos avanzado',
    enlace: 'https://drive.google.com/file/d/1d7EK-mH89rQIMcWsiH3YiOAdgAR3k8TE/view?usp=sharing',
    universidad: 'Universidad Nacional de Ingenieria',
    anio: '2025',
    imagen: 'src/imagenes/img2.png'
  },
  {
    nombre: 'Algoritmos y estrutura de datos basico',
    enlace: 'https://drive.google.com/file/d/1C4rd3sCCF8ULIT0bdXBLE1XzVH4Ksf9-/view?usp=sharing',
    universidad: 'Universidad Nacional de Ingenieria',
    anio: '2025',
    imagen: 'src/imagenes/img3.png'
  },
  {
    nombre: 'C++ Basico',
    enlace: 'https://drive.google.com/file/d/1m__JAOrBuzCTglMYpsjHP3u9WDD4z83Z/view?usp=sharing',
    universidad: 'Platzi',
    anio: '2024',
    imagen: 'src/imagenes/img4.png'
  },
  {
    nombre: 'Curso definitivo de HTML y CSS',
    enlace: 'https://drive.google.com/file/d/1enprx3kEFu1GdHia7jbgtS4KlV9uE83F/view?usp=sharing',
    universidad: 'Platzi',
    anio: '2024',
    imagen: 'src/imagenes/img5.png'
  },
  {
    nombre: 'Desarrollo Web con Python',
    enlace: 'https://drive.google.com/file/d/1mYDyqWqCBN1cfIjxiWycfbNPC_qjays5/view?usp=sharing',
    universidad: 'Pontificia Universidad Catolica del Peru',
    anio: '2023',
    imagen: 'src/imagenes/img6.png'
  },
  {
    nombre: 'Web Scraping con Python',
    enlace: 'https://drive.google.com/file/d/1e-c1VCjp_Un5CVM-OTIfuc0Z1FtqDBHE/view?usp=sharing',
    universidad: 'Pontificia Universidad Catolica del Peru',
    anio: '2025',
    imagen: 'src/imagenes/img7.png'
  },
  {
    nombre: 'Fundamentos de programacion orientada a objetos',
    enlace: 'https://drive.google.com/drive/u/0/folders/1fgYnsugjmoxAHVYdsEF6ZXSZm0V9M6RP',
    universidad: 'Universidad Nacional de Ingenieria',
    anio: '2025',
    imagen: 'src/imagenes/img8.png'
  },
  {
    nombre: 'Programming for Everybody (Getting Started with Python)',
    enlace: 'https://drive.google.com/file/d/1K8zAxV8ZgzqGbcZgZyl_rx9uDJPKMd-D/view?usp=sharing',
    universidad: 'University of Michigan - Coursera',
    anio: '2025',
    imagen: 'src/imagenes/img9.png'
  }
];
  
  const img_prin = 'src/imagenes/img0.png'

  const redirecciones = ["Inicio", "Sobre mí", "Certificados", "Contacto"]

  const contenidoF = 'contenidoF'

</script>

<template>
  <header>
    <nav class="navbar">
      <div class="header-nav">
        <div class="logo">Portafolio</div>

        <div class="nav-buttons">
          <button v-for="item in redirecciones" class="boton-header">
            {{ item }}
          </button>
        </div>
      </div>
    </nav>
    <hr />
  </header>
  
  <section class="hero">
    <div class="hero-img">
      <img v-if="img_prin" :src="img_prin" alt="Foto perfil" />
    </div>

    <div class="hero-content">
      <h1>Johan Alexis Contreras Granados</h1>
      <h2>Estudiante de Ingeniería | Universidad Peruana de Ciencias Aplicadas</h2>

      <p>
        Como estudiante de Ingeniería de Software en la UPC, mi enfoque está en el
        aprendizaje continuo y el desarrollo de habilidades clave en tecnología.
        A lo largo de mi formación, he obtenido certificaciones en instituciones
        como PUCP, UNI y Platzi.
      </p>

      <div class="hero-buttons">
        <a href="https://www.linkedin.com/in/johan-alexis-contreras-granados-abb06b341/" target="_blank" class="btn linkedin">LinkedIn</a>
        <a href="https://github.com/johancg04" target="_blank" class="btn github">GitHub</a>
        <a href="mailto:j.contreras.granados.04@gmail.com" class="btn email">Email</a>
      </div>
    </div>
  </section>


  <div :class="contenidoF">
    <span>CERTIFICADOS</span>
    <table>
      <thead>
          <tr>
            <th v-for="titulo in titulos">
                <bold>{{ titulo }}</bold>
            </th>
          </tr>
      </thead>
      <tbody>
        <tr v-for="curso in cursos">
          <td>
            <a v-bind:href="curso.enlace" target="_blank">
              {{ curso.nombre }}
            </a>
          </td>
          <td>{{ curso.universidad }}</td>
          <td>{{ curso.anio }}</td>
          <td>
            <img v-if="curso.imagen" :src="curso.imagen" alt="" />
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped>
  /** HEADER **/
  .navbar {
    width: 100%;
    padding: 25px 200px;
  }

  .header-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-size: 1.4rem;
    font-weight: bold;
  }

  .nav-buttons {
    display: flex;
    gap: 12px;
  }

  .boton-header {
    font-size: 15px;
    background: transparent;
    padding: 8px 14px;
    border: white;   
  }

  .boton-header:hover {
    color: #3366ff;
  }

  hr {
    border: none;
    height: 1px;
    background-color: #e5e7eb;
  }
  /**INFORMACION**/
  .hero {
    display: flex;
    align-items: center;
    gap: 60px;
    padding: 80px 200px;
    background: #f8fbff;
  }

  .hero-img img {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    object-fit: cover;
    border: 6px solid white;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  }

  .hero-content h1 {
    font-size: 48px;
    font-weight: 800;
    margin-bottom: 10px;
  }

  .hero-content h2 {
    font-weight: 500;
    font-size: 25px;
    color: #2563eb;
    margin-bottom: 20px;
  }

  .hero-content p {
    max-width: 600px;
    line-height: 1.6;
    color: #334155;
    margin-bottom: 30px;
  }

  .hero-buttons {
    display: flex;
    gap: 15px;
  }

  .btn {
    padding: 12px 20px;
    border-radius: 10px;
    font-weight: 600;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  }

  .linkedin {
    background: #3366ff;
    color: white;
  }

  .github {
    background: #111827;
    color: white;
  }

  .email {
    background: white;
    color: #111827;
    border: 1px solid #d1d5db;
  }


  /** TABLA **/
  .contenidoF {
    margin-top: 30px;
    text-align: center;
    padding: 30px;
  }

  div span {
      font-size: 30px;
      text-decoration: underline;
      font-family: "Monaco";
  }

  table {
      margin: auto;
      margin-top: 30px;
  }

  table th {
      padding: 5px 30px 5px 30px;
      background-color: #3366ff;
      color: white;
      text-align: center;
      border-style: solid;
      border-color: black;
      border-width: 1px;
  }

  table td {
      text-align: center;
      border-style: solid;
      border-width: 1px;
      border-color: black;
      padding: 10px;
      align-items: center;
  }

  td a:link {
      color: black;
      text-decoration: underline;
      text-align: center;
  }

  td a:active {
      color: black;
  }

  td a:visited {
      color: black;
      text-align: center;
  }

  td a:hover {
      text-decoration: underline;
      font-weight: bold;
      color: #3366ff;
      font-size: 15px;
  }

  td img {
      height: 175px;
      cursor: pointer;
  }
</style>
