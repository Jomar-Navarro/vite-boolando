<script>
  export default {
    
  }
</script>


<template>
  <header>
    <div class="container d-flex ">
        <nav class="menu d-flex ">
          <ul class="d-flex">
            <li><a href="#"></a>Donna</li>
            <li><a href="#"></a>Uomo</li>
            <li><a href="#"></a>Bambini</li>
          </ul>
        </nav>

        <div class="logo d-flex ">
          <img src="/src/assets/img/boolean-logo.png" alt="logo">
        </div>

        <div class="icons">
          <i class="fa-regular fa-user"></i>
          <i class="fa-regular fa-heart"></i>
          <i class="fa-solid fa-bag-shopping"></i>
        </div>
      </div>
  </header>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

  header{
    position: sticky;
    top: 0;
    z-index: 100;
    justify-content: center;
    background-color: $bg-header-color;
    height: 80px;
    box-shadow: 0px 1px 4px 0px;
    .container{
      justify-content: space-between;
      align-items: center;
      height: 100%; 
      ul li{
        color: white;
        padding: 5px;
        font-size: 1rem;
        font-weight: 800;
      }
    }
  }

  .container{
    .logo{
      img{
        width: 150px;
        height: 40px;
      }
    } 
  }
</style>