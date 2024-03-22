<script>
  import ProductCard from './ProductCard.vue';
  import products from '../assets/data/db.json';
  export default {
    data(){
      return{
        products: products.products,
      }
    },

    components: {
      ProductCard
    }
  }
</script>


<template>
  <main>
    <div class="container">
      <ProductCard v-for="product in products" :key="product.id"
        :productMainImage="`src/assets/img/${product.frontImage}`"
        :productSecondImage="`src/assets/img/${product.backImage}`" :productDiscount="product.value"
        :productBrand="product.brand" :productName="product.name" :productFullPrice="product.price" />
    </div>
  </main>
</template>


<style lang="scss" scoped>

</style>