<template>

<main>
  <h1>proframepi</h1>
  <div>{{cmbpg}}</div>
  <section class="cuerpo">
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
            epnum: '2',
            tituloep:'asdfgh',

              },
               {
            epnum: '3',
            tituloep:'asdfffgh',

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
.cuerpo{
    margin-top: 100px;
}
#ficha{
  width: 30%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: sticky;
  h1{
      font-size: 30px;
      font-weight: bold;
      font-family: sans-serif;
  }
  p{
      font-size: 16px;
      margin: 10px 0 30px 0;
  }
}
#epi{
  font-size: 32px;
  font-weight: bold;
  position: fixed;
}
section{
  display: flex;
  flex-direction: row;
  padding: 30px;
  width: 100%;
}
.mbpg_epis{
  width: 90%;
  margin-left: 10%;
}
.scroll{
    margin-top: 60px;
}
section{
    background-color: #f5f5f5;
}

</style>