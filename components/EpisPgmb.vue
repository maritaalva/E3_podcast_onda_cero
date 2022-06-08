<template>
    <div class="hcard_pgep">
      <p class="epnum">{{epnum}}</p>
      <p class="pgeptitulo">{{tituloep}}</p>
      <button @click="playpause">
          <boton-play :isPlaying="isPlaying" /></button>
    <img src="/ilike_line.svg" alt="Horario">

    </div>
</template>
<script>
export default{
    props:['epnum','tituloep']
}
</script>
