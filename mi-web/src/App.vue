<script setup>
  const titulos = ['Curso', 'Universidad', 'Año', 'Certificado']

  const cursos = [
    {
      nombre: 'Python-Fundamentos de Programacion',
      enlace: 'https://drive.google.com/file/d/15eNXdiS7vP4vg1OZBxFegkiiXsaxlm2W/view?usp=sharing',
      universidad: 'Universidad Nacional de Ingenieria',
      anio: '2023'
    },
    {
      nombre: 'Algoritmos y estrutura de datos avanzado',
      enlace: 'https://drive.google.com/file/d/1d7EK-mH89rQIMcWsiH3YiOAdgAR3k8TE/view?usp=sharing',
      universidad: 'Universidad Nacional de Ingenieria',
      anio: '2025'
    },
    {
      nombre: 'Algoritmos y estrutura de datos básico',
      enlace: 'https://drive.google.com/file/d/1C4rd3sCCF8ULIT0bdXBLE1XzVH4Ksf9-/view?usp=sharing',
      universidad: 'Universidad Nacional de Ingenieria',
      anio: '2025'
    }
  ]

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
