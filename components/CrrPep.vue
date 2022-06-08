<template>
   <NuxtLink to="/podcastEpi">
   <article class="crrpep">
       <!-- :style="`backgroundImage: url(${srcp})`" -->
       <!-- :style="{ backgroundImage: `url({{srcp}})`}" -->
       <div class="text_card_mb">
        <p>{{categoria}}</p>
        <h3>{{titulo}}</h3>
        </div>
        <img :src="srcp" :alt="titulo" class="bck_card_mb">

    </article></NuxtLink>
</template>

<script>
export default{
    props: ['titulo','srcp', 'categoria' ]
}
</script>
<style lang="postcss" scoped>
.crrpep{
        margin: 0 1rem 0;

}
.text_card_mb{
    position: absolute;
    
}
.bck_card_mb{
    z-index: 1;
height: 162px;    
width: 162px;    

}
</style>