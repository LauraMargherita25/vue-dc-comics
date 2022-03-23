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
        flex-basis: calc((100% / 6) - .5rem);
        .img_wrapper{
            width: 100%;
            height: 192px;
            img{
                width: 100%;
                object-fit: fill;
            }
        }
    }
</style>
