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
   <HeaderView />
   <h3 style="margin-top: 15px">Arquitectos</h3>
     <p>Investiga acerca de los arquitectos y constructoras que diseñan estos edificios</p>

<div class="row">
<div class="card" style="width: 18rem; margin: 10px" v-for="arquitecto of arquitectos" :key="arquitecto.slug">
  <div class="card-body">
    <h5 class="card-title">{{arquitecto.name}}</h5>
    <NuxtLink :to="{ name: 'arquitectos-slug', params: { slug: arquitecto.slug } }">Ver mas...</NuxtLink>
  </div>
</div>
</div>

   <FooterView />
 </div>
</template>