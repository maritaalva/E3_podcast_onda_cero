<template>
<section>

  <img id="icard_directo" src="/card_directo.svg" alt="icono compartir">

  <main class="index_page">
         <h2>PODCAST</h2>
      <flickity  class="flickity" ref="flickity" :options="flickityOptions">
     <crr-pep
      v-for="(item, index) in ccardsMob" 
      :key="index" 
      :titulo="item.titulo"
      :categoria="item.categoria"
      :srcp="item.srcp" 
      class="mb-card-carousel-pd"/>
    </flickity>
    <h2>PROGRAMA</h2>
    <flickity  class="flickity" ref="flickity" :options="flickityOptions">
     <crr-pepg
      v-for="(item, indexpg) in ccardsMobpg" 
      :key="indexpg" 
      :titulopg="item.titulopg"
      :categoriapg="item.categoriapg"
      :srcpg="item.srcpg" 
      class="mb-card-carousel-pg"/>
    </flickity>
        <h2>NOTCIAS</h2>

    <div class="card_mb_day_nw">
      <p class="text_day_nw">08<br>06<br>20222<br></p>
      <img src="/card_mb_day_nw.svg" alt="icono compartir">
    </div>
</main>

</section>
</template>

<script>
import Flickity from 'vue-flickity'
import CrrPep from '../components/CrrPep.vue'
import CrrPepg from '../components/CrrPepg.vue'

export default {
  name: 'IndexPage',
  components: {
    Flickity,
    CrrPep,
    CrrPepg
},
  data() {
    return {
      flickityOptions: {
        initialIndex: 4,
        freeScroll: true,
        contain: true,
        prevNextButtons: false,
        pageDots: false
        // any options from Flickity can be used
      },
      ccardsMob: [
        {
          titulo: 'Kinótico',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_1.svg'
        },
        {
          titulo: 'Ella Juegan',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_2.svg'
        },
        {
          
          titulo: 'Salud Financiera',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_3.svg'
        },
        {
          
          titulo: 'En primera línea',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_4.svg'
        },
        { 
          titulo: 'La Parroquia',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_1.svg'
        },
        {
          titulo: 'Cállate Payaso',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_2.svg'
        },
        {
          titulo: 'Onda Ruedo',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_3.svg'
        },
                {
          titulo: 'Annual, 1921',
          categoria: 'PODCAST',
          srcp: '/pattern_mobile_4.svg'
        }
        ],
          ccardsMobpg: [
        {
          titulopg: 'La Brújula',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_1pg.svg'
        },
        {
          titulopg: 'Más de Uno',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_2pg.svg'
        },
        {
          
          titulopg: 'La cultureta',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_3pg.svg'
        },
        {
          
          titulopg: 'Gente Viajera',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_4pg.svg'
        },
        { 
          titulopg: 'Onda agraria',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_1pg.svg'
        },
        {
          titulopg: 'En buenas manos',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_2pg.svg'
        },
        {
          titulopg: 'No son Horas',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_3pg.svg'
        },
                {
          titulopg: 'Porfin no es lunes',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_4pg.svg'
        }
        ],
          ccardsMobnw: [
        {
          dianw: '08 06 2022',
          categorianw: 'NOTCIAS',
          srcnw: '/pattern_mobile_1nw.svg'
        },
        {
          dianw: 'Más de Uno',
          categorianw: 'NOTCIAS',
          srcnw: '/pattern_mobile_2nw.svg'
        },
        {
          
          dianw: 'La cultureta',
          categorianw: 'NOTCIAS',
          srcnw: '/pattern_mobile_3nw.svg'
        },
        {
          
          dianw: 'Gente Viajera',
          categorianw: 'NOTCIAS',
          srcnw: '/pattern_mobile_4nw.svg'
        },
        { 
          dianw: 'Onda agraria',
          categorianw: 'NOTCIAS',
          srcnw: '/pattern_mobile_1nw.svg'
        },
        {
          dianw: 'En buenas manos',
          categorianw: 'NOTCIAS',
          srcpg: '/pattern_mobile_2nw.svg'
        },
        {
          dianw: 'No son Horas',
          categorianw: 'NOTICIAS',
          srcnw: '/pattern_mobile_3nw.svg'
        },
                {
          dianw: 'Porfin no es lunes',
          categorianw: 'NOTCIAS',
          srcnw: '/pattern_mobile_4nw.svg'
        }
        ]
    }
  }
}
</script>
<style lang="postcss" scoped>
.index_page{
  padding-bottom: 5rem;
}

#icard_directo{
  width: 100%;
}
.text_day_nw{
  position: absolute;
  font-size: 31px;
  font-weight: 500;
}
.card_mb_day_nw img{
width: 100%;
}
</style>

