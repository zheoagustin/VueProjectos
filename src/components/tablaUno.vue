<template>
    <table class="table">
            <thead class="thead-dark">
                <tr>
                    <th scope="col">Año</th>
                    <th scope="col">Pelicula</th>
                    <th scope="col">Puntaje</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(item, i) in dato" :key="i" :class='{
                    buena: item.puntaje >=7,
                    promedio: item.puntaje>=4 && item.puntaje <=7 ,
                    mala: item.puntaje<=4}'>
                    <td>
                        {{item.año}}
                    </td>
                    <td>
                        {{item.pelicula}}
                    </td>
                    <td>
                    {{item.puntaje}}
                    </td>
                </tr>
            </tbody>
    </table>
</template>
<script>
export default {
  name: 'tablaUno',
  props: ['dato',]
}
</script>
<style>
.buena {
    background-color: green;
}
.mala {
    background-color: red;
}
.promedio {
    background-color: orange;
}

</style>

