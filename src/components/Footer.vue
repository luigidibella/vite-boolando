<script>
  export default {

  }
</script>

<template>
  <footer>
    <div class="container">
      <div class="info">
        <div class="title">Boolando s.r.l</div>
        <div class="link">
          <ul>
            <li><a href="#">Informazioni legali</a></li>
            <li><a href="#">Informativa sulla privacy</a></li>
            <li><a href="#">Diritti di recesso</a></li>
          </ul>
        </div>
      </div>
      <div class="social">
        <div class="title">Trovaci anche su</div>
        <div class="icon">
          <ul>
            <li><a href="#"><i class="fa-brands fa-square-twitter"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-instagram"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-pinterest"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-youtube"></i></a></li>
          </ul>
        </div>
        
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *; 

footer{
  background-color: $bg-footer;
  .container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 110px;
    color: $primary;

    .title{
      font-weight: bold;
    }

    .social{
      .title{
        font-size: 12px;
      }
    }
    
    ul{
      list-style: none;
      display: flex;
      justify-content: center;
      li{
        padding: 5px 10px 5px 0;
        a{
          color: $primary;
          text-decoration: none;
          font-size: 12px;
          &:hover{
            color: $bg-header;
            text-decoration: underline;
          }
          i{
            font-size: 20px;
          }
          i:hover{
            color: $bg-header;
          }
        }
      }
    }
  }
}

</style>