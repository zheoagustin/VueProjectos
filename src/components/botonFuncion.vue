<template>
     <button class="btn btn-primary" type="button" @click="funcion" id="center">{{accion}}</button>
</template>

<script>
export default {
  name: 'botonFuncion',
  props: ['accion','funcion']
}
</script>
<style>

#center {
    width: 50%;
    margin-left: 25%;
    margin-top: 10px;
}
.btn-primary.focus, .btn-primary:focus {
    box-shadow: none!important;
}

</style>


