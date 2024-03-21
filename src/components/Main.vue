<script>
  export default {

  }
</script>

<template>
  <main>
    <div class="container">
      <h1>Questo è il <span>Main</span>.</h1>
    </div>
  </main>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.container{
  height: calc(100vh - 70px - 80px);
  display: flex;
  justify-content: center;
  align-items: center;
  span{
    color: $bg-header;
  }
}

</style>