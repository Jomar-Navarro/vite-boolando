<script>
  export default {
    
  }
</script>


<template>
  <main>
    <div class="container d-flex ">

      <!-- Top items -->
      <div class="product">
        <img class="visible" src="/src/assets/img/1.webp" alt="1">
        <img src="/src/assets/img/1b.webp" alt="1b">
        <span class="heart d-flex ">&hearts;</span>
        <span class="discount d-flex">-50%</span>
        <span class="eco d-flex">Sostenibilitá</span>
        <p>Levi's</p>
        <h3>RELAXED FIT TEE UNISEX</h3>
        <span class="prezzo">14,99 &euro;</span>
        <span class="overline">29,99 &euro;</span>
      </div>

      <div class="product">
        <img class="visible" src="/src/assets/img/2.webp" alt="2">
        <img src="/src/assets/img/2b.webp" alt="2b">
        <span class="heart d-flex ">&hearts;</span>
        <span class="discount  d-flex">-30%</span>
        <p>Guess</p>
        <h3>ROSES TEE</h3>
        <span class="prezzo">20,99 &euro;</span>
        <span class="overline">29,99 &euro;</span>
      </div>

      <div class="product">
        <img class="visible" src="/src/assets/img/3.webp" alt="3">
        <img src="/src/assets/img/3b.webp" alt="3b">
        <span class="heart d-flex ">&hearts;</span>
        <span class="discount d-flex">-30%</span>
        <p>Come zucchero filato</p>
        <h3>VOGLIA DI COLORI PASTELLO</h3>
        <span class="prezzo">129,99 &euro;</span>
        <spa class="overline">184,99 &euro;</spa>
      </div>
      <!-- /Top items -->

      <!-- Bottom items -->
      <div class="product">
        <img class="visible" src="/src/assets/img/4.webp" alt="4">
        <img src="/src/assets/img/4b.webp" alt="4b">
        <span class="heart d-flex ">&hearts;</span>
        <span class="discount d-flex">-50%</span>
        <span class="eco d-flex">Sostenibilitá</span>
        <p>Levi's</p>
        <h3>TEE UNISEX</h3>
        <span class="prezzo">14,99 &euro;</span>
        <span class="overline">29,99 &euro;</span>
      </div>

      <div class="product ">
        <img class="visible" src="/src/assets/img/5.webp" alt="5">
        <img src="/src/assets/img/5b.webp" alt="5b">
        <span class="heart d-flex ">&hearts;</span>
        <span class="discount d-flex">-50%</span>
        <span class="eco d-flex">Sostenibilitá</span>
        <p>Maya Deluxe</p>
        <h3>STRIPE BODICE</h3>
        <span class="prezzo">99,99 &euro;</span>
      </div>

      <div class="product">
        <img class="visible" src="/src/assets/img/6.webp" alt="6">
        <img src="/src/assets/img/6b.webp" alt="6b">
        <span class="heart d-flex ">&hearts;</span>
        <span class="eco-last d-flex">Sostenibilitá</span>
        <p>Esprit</p>
        <h3>MAGLIONE - BLACK</h3>
        <span class="prezzo">29,99 &euro;</span>
      </div>

    </div>
  </main>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.container{
  .product{
    margin: 40px auto;
    position: relative;
    display: inline-block;
    img{
        cursor: pointer;
        width: 465px;
        height: 670px;
    }
    .heart{
        position: absolute;
        top: 0;
        right: 0;
        align-items: center;
        justify-content: center;
        background-color: white;
        height: 50px;
        width: 50px;
        margin-top: 10px;
        font-size: 2rem;
        &:hover{
          color: red;
        }
      .discount{
        position: absolute;
        bottom: 0;
        left: 0;
        align-items: center;
        justify-content: center;
        text-align: center;
        background-color: white;
        width: 55px;
        height: 25px;
        margin-bottom: 100px;
        background-color: red;
        color: white;
      }
    }
  }

  .product{
    .eco{
        position: absolute;
        bottom: 0;
        left: 0;
        align-items: center;
        justify-content: center;
        text-align: center;
        background-color: white;
        width: 100px;
        height: 25px;
        margin-bottom: 100px;
        margin-left: 60px;
        background-color: green;
        color: white;
    }

    .discount{
        position: absolute;
          bottom: 0;
          left: 0;
          align-items: center;
          justify-content: center;
          text-align: center;
          background-color: white;
          width: 55px;
          height: 25px;
          margin-bottom: 100px;
          background-color: red;
          color: white;
    }

    .eco-last{
        position: absolute;
          bottom: 0;
          left: 0;
          align-items: center;
          justify-content: center;
          text-align: center;
          background-color: white;
          width: 100px;
          height: 25px;
          margin-bottom: 100px;
          background-color: green;
          color: white;
    }
  }

  .visible{
      position: absolute;
      top: 0;
      left: 0;
  }
}

.prezzo{
    color: red;
    font-weight: 800;
}

.overline {
  text-decoration: line-through;
}

.product:hover .visible {
  display: none;
}
</style>