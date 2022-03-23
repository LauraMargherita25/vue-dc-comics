.<template>
  <div class="card">
      <div class="img_wrapper">
        <img :src="cardImg" :alt="cardText">
      </div>
      <p>{{ cardText }}</p>
  </div>
</template>

<script>
export default {
  name: 'CardComic',
  props: {
    cardImg: String,
    cardText: String
  }
}
</script>

<style scoped lang="scss">
  .card{
    width: calc(100% / 6 - 1rem);
    margin-bottom: 2rem;
    .img_wrapper{
      width: 100%;
      height: 200px;
      margin-bottom: 1rem;
      overflow: hidden;
      img{
        width: 100%;
      }
    }
  }
</style>
