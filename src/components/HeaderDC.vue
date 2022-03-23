<template>
  <header>

    <div class="container">
      <div class="img_wrapper">
        <img src="@/assets/img/dc-logo.png" alt="">
      </div>

      <ul>
        <li @click="setActiveIndex(index)" v-for="(link, index) in links" :key="index" :class="{active: index == activeIndex}"><a :href="link.href">{{ link.text.toUpperCase() }}</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderDC',
  data () {
    return {
      activeIndex: 1,
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
  },
  methods: {
    setActiveIndex (index) {
      this.activeIndex = index
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables.scss";
header{
  background-color: white;
  .img_wrapper{
    width: 100px;
    height: 100px;
    padding: 1rem;
    img{
      width: 100%;
      object-fit: contain;
    }
  }
  li{
    display: inline-block;
    padding: 0 1rem;
    border-bottom: 5px solid white;
    &.active {
      color: $blue;
      border-bottom: 5px solid $blue;
    }
    a{
      line-height: 100px;
      display: inline-block;
    }
  }
}
.container{
  justify-content: space-between;
}
</style>
