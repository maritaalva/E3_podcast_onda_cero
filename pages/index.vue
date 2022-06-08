<template>
<section>
  <header>
    <!-- <div class="card_mobile_directo">
      <div>
      <div>
      <img src="/circle_green.svg" alt="icono directo">
      <a>EN DIRECTO</a>
      </div>
      <img src="/compartir_line_grey.svg" alt="icono compartir">
      </div>
    </div> -->
  </header>
  <img src="/card_directo.svg" alt="icono compartir">

  <main>
      <flickity  class="flickity" ref="flickity" :options="flickityOptions">
     <crr-pep
      v-for="(item, index) in ccardsMob" 
      :key="index" 
      :titulo="item.titulo"
      :categoria="item.categoria"
      :srcp="item.srcp" 
      class="mb-card-carousel"/>
    </flickity>
</main>
  <MenuMobile/>
  <MenuWeb/>
</section>
</template>

<script>
import Flickity from 'vue-flickity'
import CrrPep from '../components/CrrPep.vue'
export default {
  name: 'IndexPage',
  components: {
    Flickity,
    CrrPep
},
  data() {
    return {
      flickityOptions: {
        initialIndex: 2,
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
    }
  }
}
</script>
<style lang="postcss" scoped>

        </style>

