<template>
  <section id="content">
    <h2 class="subheader">{{ titulo }}</h2>
    <hr/>
    <h1>Este es MI COMPPONENTE</h1>
    <h2>{{ subtitulo }}</h2>
    <hr/>

    <h2>Reactividad</h2>
    <input type="text" v-model="nombre"/>
    Mi nombre es: <strong>{{nombre}}</strong>

    <h2>Directivas condicioneles</h2>
    <input type="number" v-model="edad"/>
    Mi edad es: <strong>{{edad}}</strong>

    <p class="alert-danger-provisional" v-if="edad && edad >= 18 && edad <65">
      ¡¡ ERES MAYOR DE EDAD !!
    </p>

    <p class="alert-purple-provisional" v-else-if="edad && edad >= 65">
      ¡¡ ERES DE AVANZADA EDAD !!
    </p>

    <p class="alert-success-provisional" v-else>
      ¡¡ ERES MENOR DE EDAD !!
    </p>

    <h2>Directivas iterativa</h2>
    <ol>
      <li v-for="pelicula in peliculas" :key="pelicula">{{pelicula}}</li>
    </ol>





<!-- Esto me sirve para ver la data del modelo
    <pre>
      {{$data}}
    </pre>
Esto me sirve para ver la data del modelo-->

  </section>
</template>

<script>
export default {
  name: "MiComponente",
  data() {
    return {
      titulo: "Mi Componente",
      subtitulo: "Soy el subtitulo de mi componente",
      nombre: '',
      edad: 18,
      peliculas: ['Batman vs Superman', 'El señor de los anillos', 'Spiderman', 'Anabelle']
    }
  }
};
</script>
