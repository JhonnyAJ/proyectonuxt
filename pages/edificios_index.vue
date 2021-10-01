<script>
  export default {
    async asyncData({ $content, params }) {
      const edificios = await $content('edificios').fetch()
      return {
        edificios
      }
    }
  }
</script>

<template>
  <div class="container">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
   
   <HeaderView />
   <h3 style="margin-top: 15px">Edificios</h3>
     <p>Esta sección presenta los edificios y sus caracteristicas</p>

     <div class="card" v-for="edificio of edificios" :key="edificio.slug">
       <div class="card-body">
         <NuxtLink :to="{ name: 'edificios-slug', params: { slug: edificio.slug } }">{{edificio.title}}</NuxtLink>
       </div>
     </div>
   <!-- <ul>
     <li v-for="edificio of edificios" :key="edificio.slug">
       <NuxtLink :to="{ name: 'edificios-slug', params: { slug: edificio.slug } }">{{edificio.title}}</NuxtLink>
     </li>
   </ul> -->
   <FooterView />
 </div>
</template>