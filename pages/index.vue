<template>
 <div class="container">
   <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
   <HeaderView />
   <h2 style="margin-top: 15px">Computer Science Books</h2>
	  <p>This website offers information about highest buildings.</p>
    <button class="btn btn-primary">Prueba</button>
    <ul>
	  <li> <NuxtLink to="/edificios_index">Buildings information</NuxtLink></li>
	  <li> <NuxtLink to="/arquitectos_index">Architects information</NuxtLink></li>
	  <li> <NuxtLink to="/ciudades_index">Cities information</NuxtLink></li>
	</ul>
   <FooterView />
 </div>
</template>

<script>
export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
};
</script>