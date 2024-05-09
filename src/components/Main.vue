<script>
import ProductCard from './partials/ProductCard.vue';
import products from '../data/db.json';
  export default {
    components:{
      ProductCard,
    },

    data(){
      return{
        products,
      }
    },

    mounted() {
      console.log(/* this.products */);
    },

  }
</script>

<template>
  <main>
    <div class="container">
      <!-- <h1>Questo è il <span>Main</span>.</h1> -->
      <ProductCard
        v-for="product in products.products"
        :key="product.id"
        :id="product.id"
        :frontImage="`src/assets/img/${product.frontImage}`"
        :backImage="`src/assets/img/${product.backImage}`"
        :brand="product.brand"
        :name="product.name"
        :price="product.price"
        :isInFavorites="product.isInFavorites"
        :badges="product.badges"
      />
      
    </div>
  </main>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.container{
  /* height: calc(100vh - 70px - 110px); */
  padding-top: 120px;
  padding-bottom: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 20px;
  /* align-items: center; */
  /* border: 1px dashed black; */
  span{
    color: $bg-header;
  }
}

</style>