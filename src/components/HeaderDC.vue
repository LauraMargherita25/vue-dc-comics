<template>
  <header>

    <div class="container">

      <img src="@/assets/img/dc-logo.png" alt="">

      <ul>
        <li v-for="(link, index) in links" :key="index"><a :href="link.href">{{ link.text }}</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderDC',
  data () {
    return {
      links: [
        {
          href: '#',
          text: 'characters'
        },
        {
          href: '#',
          text: 'comics'
        },
        {
          href: '#',
          text: 'movies'
        },
        {
          href: '#',
          text: 'tv'
        },
        {
          href: '#',
          text: 'games'
        },
        {
          href: '#',
          text: 'collectibles'
        },
        {
          href: '#',
          text: 'videos'
        },
        {
          href: '#',
          text: 'fans'
        },
        {
          href: '#',
          text: 'news'
        },
        {
          href: '#',
          text: 'shop'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
header{
  background-color: white;
  li{
    display: inline-block;
    padding: 1rem;
    a{
      display: inline-block;
    }
  }
}
.container{
  justify-content: space-between;
}
</style>
