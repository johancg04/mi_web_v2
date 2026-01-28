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

  const contenidoF = 'contenidoF'
</script>

<template>
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
