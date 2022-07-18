<template>
  <div id="app">
    <botonFuncion :accion="mostrar" :funcion="mostrarTable"></botonFuncion>
    <botonFuncion :accion="ocultar" :funcion="ocultarTable"></botonFuncion>
    <tablaUno :dato="peliculas" class="container"></tablaUno>
  </div>
</template>

<script>
import tablaUno from './components/tablaUno.vue'
import botonFuncion from './components/botonFuncion.vue'


export default {
  name: 'App',
  components: {
    tablaUno,
    botonFuncion
  },
  data (){
    return {
       peliculas: [{ año: 1997, pelicula: "Terminator", puntaje: 8 },
          { año: 1995, pelicula: "Duro de matar", puntaje: 7 },
          { año: 1990, pelicula: "Chucky", puntaje: 3 },
          { año: 2003, pelicula: "Rapidos y furioso", puntaje: 6 },
          { año: 2008, pelicula: "Los mercenarios", puntaje: 10 },
          { año: 2010, pelicula: "Spider Man ", puntaje: 9 }
          ],
        mostrar : "Mostrar",
        ocultar: "Ocultar",
    }
  },
  methods : {
     mostrarTable(){
        this.peliculas = [{ año: 1997, pelicula: "Terminator", puntaje: 8 },
        { año: 1995, pelicula: "Duro de matar", puntaje: 7 },
        { año: 1990, pelicula: "Chucky", puntaje: 3 },
        { año: 2003, pelicula: "Rapidos y furioso", puntaje: 6 },
        { año: 2008, pelicula: "Los mercenarios", puntaje: 10 },
        { año: 2010, pelicula: "Spider Man ", puntaje: 9 }]
        },
     ocultarTable(){
        this.peliculas= []
        }
  }
}
</script>

<style>

.container {
    margin-top: 30px;

}

body {
    background: linear-gradient(45deg, rgb(1, 1, 155), rgb(1, 18, 114));;
    
}


</style>
