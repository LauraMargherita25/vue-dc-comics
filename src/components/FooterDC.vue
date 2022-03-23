<template>
  <footer>
      <div class="footer_top">
          <div class="container">
                <ul>
                    <li v-for="(btn, index) in btns" :key="index">
                        <img :src="'assets/img/buy-' + btn.img" alt="">
                        <a :href="btn.href">{{ btn.text }}</a>
                    </li>
                </ul>
          </div>
      </div>
      <div class="footer_btm">
          <div class="container">
              <div class="footer_btm_l">
                  <ul>
                      <ul v-for="(link,index) in links" :key="index">
                          <h3>{{ link.title }}</h3>
                          <li v-for="(a, index) in link.arrLink" :key="index">
                              <a href="">{{ a }}</a>
                          </li>
                      </ul>
                  </ul>
              </div>
              <div class="footer_btm_r">
                  <img src="../assets/img/dc-logo-bg.png" alt="">
              </div>
          </div>
      </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterDC',
  data () {
    return {
      btns: [
        {
          img: 'comics-digital-comics.png',
          href: '#',
          text: 'digital comics'
        },
        {
          img: '',
          href: '#',
          text: 'dc merchandise'
        },
        {
          img: '',
          href: '#',
          text: 'subscription'
        },
        {
          img: '',
          href: '#',
          text: 'comic shop locator'
        },
        {
          img: '',
          href: '#',
          text: 'dc power visa'
        }
      ],
      links: [
        {
          title: 'dc comics',
          arrLink: [
            'Characters',
            'Comics',
            'Movies',
            'TV',
            'Games',
            'Videos',
            'News'
          ]
        },
        {
          title: 'dc comics',
          arrLink: [
            'Characters',
            'Comics'
          ]
        },
        {
          title: 'dc comics',
          arrLink: [
            'Characters',
            'Comics'
          ]
        },
        {
          title: 'dc comics',
          arrLink: [
            'Characters',
            'Comics'
          ]
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.footer_top{
    background-color: #0282f9;
    color: white;
    .container{
        justify-content: space-evenly;
        li{
            display: inline-block;
            padding: 1rem;
        a{
            display: inline-block;
        }
    }
  }
}
.footer_btm{
    width: 100%;
    height: 300px;
    background-image: url(../assets/img/footer-bg.jpg);
    color: white;
    .footer_btm_l{
        width: 50%;
        padding: 2rem 0;
    }
}
</style>
