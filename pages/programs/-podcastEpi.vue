<template>

<main>
  <h1>proframepi</h1>
  <div>{{cmbpd}}</div>
  <section class="cuerpo">
        <article id="mbpd_header">
            <div class="crrpepd">
                <div class="text_card_mbpd">
                    <p>{{cmbpd.categoriapd}}</p>
                    <h3>{{cmbpd.titulopd}}</h3>
                </div>
                <img :src="srcp" :alt="titulo" class="bck_card_mb">
            </div>
            <p>{{cmbpd.descripcion}}</p>
        </article>
        <section class="mbpd_epis">
            <img src="/inputs_programa_episodes.svg" :alt="titulo" class="bck_card_mb">
            <div class="scroll">
                <epis-pdmb
                v-for="(itempd, i) in cmbpd.pdepi" 
                :key="i" 
                :epnum="itempd.epnum" 
                :alt="itempd.tituloep" 
                :tituloep="itempd.tituloep"
                />
            </div>
            <audio-player/>
        </section>
   </section>

</main>

</template>

<script>
export default {
computed: {
        cmbpd() {
            return this.mbpdepicd.find(
                (cdpd) => cdpd.titulopd === this.$route.params.titulopd
            )
        }
    },
    data() {
        return {
            mbpdepicd: [
        {
          titulopd: 'La Brújula',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_1pd.svg',
          pdepi: [
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
          titulopd: 'Más de Uno',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_2pd.svg',
          pdepi: [
              {
            epnum: '',
            tituloep:'',

              }
          ]
        },
        {
          
          titulopd: 'La cultureta',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_3pd.svg',
          pdepi: [
              {
            epnum: '',
            tituloep:'',

              }
          ]
        },
        {
          
          titulopd: 'Gente Viajera',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_4pd.svg',
          pdepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
        { 
          titulopd: 'Onda agraria',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_1pd.svg',
          pdepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
        {
          titulopd: 'En buenas manos',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_2pd.svg',
          pdepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
        {
          titulopd: 'No son Horas',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_3pd.svg',
          pdepi: [
              {
              epnum: '',
              tituloep:'',
              }
          ]
        },
                {
          titulopd: 'Porfin no es lunes',
          categoriapd: 'PROGRAMA',
          srcpd: '/pattern_mobile_4pd.svg',
          pdepi: [
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