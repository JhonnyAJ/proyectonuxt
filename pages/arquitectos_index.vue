<script>
  export default {
    async asyncData({ $content, params }) {
      const arquitectos = await $content('arquitectos').fetch()
      return {
        arquitectos
      }
    }
  }
</script>

<template>
  <div class="container">
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

   <HeaderView />
   <h3 style="margin-top: 15px">Arquitectos</h3>
     <p>Investiga acerca de los arquitectos y constructoras que diseñan estos edificios</p>

<div class="row">
<div class="card" style="width: 18rem; margin: 10px" v-for="arquitecto of arquitectos" :key="arquitecto.slug">
  <div class="card-body">
    <h4 class="card-title"><b>{{arquitecto.name}}</b></h4>
    <NuxtLink :to="{ name: 'arquitectos-slug', params: { slug: arquitecto.slug } }">Ver mas...</NuxtLink>
  </div>
</div>
</div>

   <FooterView />
 </div>
</template>