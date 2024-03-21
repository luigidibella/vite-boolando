<script>
  export default {

  }
</script>

<template>
  <header>
    <div class="container">
      <nav>
        <ul>
          <li><a href="#">Donna</a></li>
          <li><a href="#">Uomo</a></li>
          <li><a href="#">Bambini</a></li>
        </ul>
      </nav>
      <div class="logo">
        <img src="../assets/img/boolean-logo.png" alt="logo">
      </div>
      <nav>
        <ul>
          <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
          <li><a href="#"><i class="fa-regular fa-heart"></i></a></li>
          <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *; 

header{
  background-color: $bg-header;
  .container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    ul{
      list-style: none;
      display: flex;
      justify-content: center;
      li{
        padding: 5px;
        a{
          color: $primary;
          text-decoration: none;
          &:hover{
            text-decoration: underline;
          }
          i:hover{
            color: $secondary;
          }
        }
      }
    }
    .logo{
      width: 140px;
      height: 30px;
      margin: 20px;
    }
  }
}

</style>