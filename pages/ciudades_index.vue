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
   <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

   <HeaderView />
   <h3 style="margin-top: 15px">Ciudades</h3>
     <p>Investiga sobre las ciudades que albergan estos edificios</p>

<div class="row">
<div class="card" style="width: 18rem; margin: 10px" v-for="ciudad of ciudades" :key="ciudad.slug">
  <div class="card-body">
    <h4 class="card-title"><b>{{ciudad.name}}</b></h4>
    <NuxtLink :to="{ name: 'ciudades-slug', params: { slug: ciudad.slug } }">Ver informacion</NuxtLink>
  </div>
</div>
</div>

   <FooterView />
 </div>
</template>