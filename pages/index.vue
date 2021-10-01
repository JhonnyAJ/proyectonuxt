<template>
 <div class="container">
   <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
   <HeaderView />
   <h2 style="margin-top: 15px">Edificios altos y dónde encontrarlos</h2>
	  <p>Impresionáte con nuestro catálogo de edificio</p>
    
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