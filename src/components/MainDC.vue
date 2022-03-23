<template>
  <main>
    <div class="jumbo">
      <img src="../assets/img/jumbotron.jpg" alt="">
    </div>
    <div class="container">
      <div class="load-more_btn">
        load more
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'MainDC'
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables.scss";
main{
  background-color: $background_color;
  .jumbo{
    height: 30vh;
    img{
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: top;
    }
  }
  .container{
    justify-content: center;
    padding: 1rem;
    .load-more_btn{
      padding: .5rem 2.5rem;
      text-transform: uppercase;
      color: white;
      background-color: $blue;
    }
  }
}
</style>
