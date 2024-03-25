<script>
  export default {
    props:{
      id: Number,
      frontImage: String,
      backImage: String,
      brand: String,
      name: String,
      price: String,
      isInFavorites: Boolean,
      badges: Array,
    },

    mounted() {
      console.log();
    },

  }
</script>

<template>
  <div :id="id" class="card">
    <div class="photo">
      <img class="photo-2" :src="frontImage" alt="">
      <img class="photo-1" :src="backImage" alt="">
      <!-- like -->
      <div class="heart" :class="{'liked': isInFavorites}">
        <i class="fa-solid fa-heart"></i>
      </div>
      <!-- /like -->
      <!-- sconto e eco -->
      <div class="details">
        <h4 
        v-for="(badge, index) in badges"
        :key="index"
          :class="badge.type"
        >
          {{badge.value}}</h4
        >
        
      </div>
      <!-- /sconto e eco -->
    </div>
    
    <div class="info">
      <h3>{{ brand }}</h3>
      <h2>{{ name }}</h2>
      <strong class="sale">{{ price }}</strong> <!-- creare funzione che restituisca "price / 100 * product.badge.value" -->
      <span class="price">{{ price }}</span>
    </div>
  
  </div>

  
</template>

<style lang="scss" scoped>
.card{
  width: calc(( 100% - 40px ) / 3);
  div.photo {
    position: relative;
    .photo-2 {
      width: 100%;
      display: block;
      }
    .photo-1 {
      width: 100%;
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      opacity: 0;
      &:hover{
        opacity: 1;
      }
    }
    .heart{
      position: absolute;
      right: 0;
      top: 10px;
      i {
        padding: 12px;
        display: inline-block;
        font-size: 24px;
        background-color: white;
        text-align: center;
        /* &:hover{
          color: red;
        } */
      }
    }
    .liked {
      color: red;
    }
    .details{
      position: absolute;
      bottom: 40px;
      left: 0;
      color: white;
      display: inline-block;
      .discount{
        background-color: red;
        display: inline-block;
        padding: 5px;
      }
      .tag{
        background-color: #008000;
        display: inline-block;
        padding: 5px;
      }
    }
  }
  

  .info{
    margin-top: 10px;
    width: 100%;
    position: static;
    .sale{
      color: red;
    }
    .price{
      text-decoration: line-through;
      font-size: 14px;
    }
  }

}
</style>