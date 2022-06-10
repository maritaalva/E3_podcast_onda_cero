<template>

<main>
  <h1>proframepi</h1>
  <!-- <div>{{cmbpg}}</div> -->
  <section class="cuerpo">
       <NuxtLink to="/reproductor"/>
        <article id="mbpg_header">
            <div class="crrpepg">
                <div class="text_card_mbpg">
                    <p>{{cmbpg.categoriapg}}</p>
                    <h3>{{cmbpg.titulopg}}</h3>
                </div>
                <img :src="srcp" :alt="titulo" class="bck_card_mb">
            </div>
            <p>{{cmbpg.descripcion}}</p>
        </article>
        <section class="mbpg_epis">
            <img src="/inputs_programa_episodes.svg" :alt="titulo" class="bck_card_mb">
            <div class="scroll">
                <epis-pgmb
                v-for="(itempg, i) in cmbpg.pgepi" 
                :key="i" 
                :epnum="itempg.epnum" 
                :alt="itempg.tituloep" 
                :tituloep="itempg.tituloep"
                />
            </div>
        </section>
   </section>

</main>

</template>

<script>
export default {
computed: {
        cmbpg() {
            return this.mbpgepicd.find(
                (cdpg) => cdpg.titulopg === this.$route.params.titulopg
            )
        }
    },
    data() {
        return {
            mbpgepicd: [
        {
          titulopg: 'La Brújula',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_1pg.svg',
          pgepi: [
              {
            epnum: '9/06/2022',
            tituloep:'la columna de julia',

              },
               {
            epnum: '10/06/2022',
            tituloep:'entrevistas de julia ',

              },
               {
            epnum: '11/06/2022',
            tituloep:'la columna de julia',

              },
               {
            epnum: '12/06/2022',
            tituloep:'entrevistas de julia',

              }
          ]
        },
        {
          titulopg: 'Más de Uno',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_2pg.svg',
          pgepi: [
              {
            epnum: '',
            tituloep:'',

              }
          ]
        },
        {
          
          titulopg: 'La cultureta',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_3pg.svg',
          pgepi: [
              {
            epnum: '',
            tituloep:'',

              }
          ]
        },
        {
          
          titulopg: 'Gente Viajera',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_4pg.svg',
          pgepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
        { 
          titulopg: 'Onda agraria',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_1pg.svg',
          pgepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
        {
          titulopg: 'En buenas manos',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_2pg.svg',
          pgepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
        {
          titulopg: 'No son Horas',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_3pg.svg',
          pgepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
                {
          titulopg: 'Porfin no es lunes',
          categoriapg: 'PROGRAMA',
          srcpg: '/pattern_mobile_4pg.svg',
          pgepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        }],
        }
    }
}
</script>

<style lang="postcss" scoped>


</style>