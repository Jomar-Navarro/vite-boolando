<script>
  export default {
    data(){
      return {
        
      }
    },
    props: {
      productMainImage: String,
      productSecondImage: String,
      productDiscount: String,
      productBrand: String,
      productName: String,
      productFullPrice: String,
      productbadges: Array,
    }
  }
</script>


<template>

  <!-- Top items -->
  <div class="product">
    <img class="visible" :src="productMainImage" :alt="productMainImage">
    <img :src="productSecondImage" :alt="productSecondImage">
    <span class="heart d-flex ">&hearts;</span>
    <span class="discount d-flex">{{ productDiscount }}</span>
    <span v-for="(badge, index) in productbadges" :key="index" class="eco d-flex">{{ badge.value }}</span>
    <p>{{ productBrand }}</p>
    <h3>{{ productName }}</h3>
    <span class="prezzo">14,99 &euro;</span>
    <span class="overline">{{ productFullPrice }} &euro;</span>
  </div>

</template>


<style lang="scss" scoped>
      .product {
        margin: 40px auto;
        position: relative;
        display: inline-block;
        padding: 0 9px;
        img {
          cursor: pointer;
          width: 465px;
          height: 670px;
        }
  
        .heart {
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
  
          &:hover {
            color: red;
          }
  
          .discount {
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
  
      .product {
        .eco {
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
  
        .discount {
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
  
        .eco-last {
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
  
      .visible {
        position: absolute;
        top: 0;
        left: 0;
      }
  
    .prezzo {
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