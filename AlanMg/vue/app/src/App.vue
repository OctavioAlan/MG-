<template>
  <div id= "app">
    <!-- Navbar -->
    <nav class="navbar navbar-light bg-light d-flex justify-content-start">
      <img src="@/assets/logo1.png"/>   
      <p class="ml-3 mb-0">Visualizacion de Datos</p>
    </nav>
    <div class= "container-fluid">
      <div class= "row">
        <div class= "col-12">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App"
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab&display=swap');
#app {
  .navbar {
    height: 50px;
    background-color: rgb(3, 155, 229) !important;
    img {
      width: 31px !important;
      height: 31px !important;
    }
   p {
     color: white;
     font-family: 'Roboto Slab', serif; 
     font-size: 18px;
    }
  }
}
</style>
