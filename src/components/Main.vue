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
  height: calc(100vh - 70px - 110px);
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px dashed black;
  span{
    color: $bg-header;
  }
}

</style>