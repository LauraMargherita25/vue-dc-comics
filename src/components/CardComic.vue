.<template>
  <div class="card">
      <img :src="cardImg" :alt="cardText">
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

<style>

</style>
