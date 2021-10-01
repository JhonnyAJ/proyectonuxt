<script>
  export default {
    async asyncData({ $content, params }) {
      const ciudades = await $content('ciudades').fetch()
      return {
        ciudades
      }
    }
  }
</script>

<template>
  <div class="container">
   <HeaderView />
   <h3 style="margin-top: 15px">Ciudades</h3>
     <p>Investiga sobre las ciudades que albergan estos edificios</p>

<div class="row">
<div class="card" style="width: 18rem; margin: 10px" v-for="ciudad of ciudades" :key="ciudad.slug">
  <div class="card-body">
    <h5 class="card-title">{{ciudad.name}}</h5>
    <NuxtLink :to="{ name: 'ciudades-slug', params: { slug: ciudad.slug } }">Ver informacion</NuxtLink>
  </div>
</div>
</div>

   <FooterView />
 </div>
</template>