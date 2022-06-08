<template>
   <NuxtLink :to="{name: 'programs-programEpi', params: {titulopg: titulopg}}">
   <article class="crrpepg">
       <!-- :style="{ backgroundImage: `url({{srcp}})`}" -->
       <div class="text_card_mbpg">
        <p>{{categoriapg}}</p>
        <h3>{{titulopg}}</h3>
        </div>
        <img :src="srcpg" :alt="titulopg" class="bck_card_mbpg">

    </article></NuxtLink>
</template>

<script>
export default{
    props: ['titulopg','srcpg', 'categoriapg' ]
}
</script>
<style lang="postcss" scoped>
.crrpepg{
        margin: 0 1rem 0;

}
.text_card_mbpg{
    position: absolute;
    z-index: 888;
}
.bck_card_mbpg{
    z-index: 1;
height: 162px;    
width: 162px;    

}
</style>