<template>
  <section id="content">
    <h2 class="subheader">Peliculas</h2>

    <!--Listado articulos-->
    <div id="articles">
      
        <div v-for="pelicula in peliculas" v-bind:key="pelicula.title">
            <Pelicula :pelicula="pelicula"></Pelicula>
        </div>
        <h2>hola</h2>
    </div>
  </section>
</template>

<script>
import Pelicula from './Pelicula';

export default {
    name: 'Peliculas',
    components: {
        Pelicula
    },
    data(){
        return{
            peliculas: [
                {title: 'Batman vs Superman', year: 2017, image: "http://www.zgrados.com/wp-content/uploads/2017/08/Batman-V-Superman-1-800x445.jpg"},
                {title: 'Gran Torina', year: 2015, image: "https://2.bp.blogspot.com/-DR3U5R4aMY8/UQUgq14L7WI/AAAAAAAAAV0/e4eQkGO66Yw/s1600/descarga.jpg"},
                {title: 'El señor de los anillos', year: 2003, image: "https://i2.wp.com/elanillounico.com/wp-content/uploads/2020/01/Pases-trilogia-extendida-El-Se%C3%B1or-de-los-Anillos-Barcelona-copia.jpg?fit=660%2C660&ssl=1"},
                
            ]
        }

    }

}
</script>