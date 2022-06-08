<template>
   <NuxtLink to="/podcastEpi">
   <article :style="{ backgroundImage: `url({{srcp}})`}">
        <img :src="srcp" :alt="titulo">
       <!-- :style="{ backgroundImage: `url({{srcp}})`}" -->
        <p>{{categoria}}</p>
        <h3>{{titulo}}</h3>
    </article></NuxtLink>
</template>

<script>
export default{
    props: ['titulo','srcp', 'categoria' ]
}
</script>

<style lang="postcss" scoped>
</style>