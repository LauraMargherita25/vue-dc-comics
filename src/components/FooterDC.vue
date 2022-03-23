<template>
  <footer>
    <div class="footer_top">
      <div class="container">
          <ul>
            <li v-for="(btn, index) in btns" :key="index">
              <img :src=" '../assets/img/' + btn.icon" alt="">
              <a :href="btn.href">{{ btn.text.toUpperCase() }}</a>
            </li>
          </ul>
      </div>
    </div>
    <div class="footer_mid">
      <div class="container">
        <div class="footer_mid_l">
          <!-- <ul>
            <ul v-for="(link,index) in links" :key="index">
              <h3>{{ link.title.toUpperCase() }}</h3>
              <li v-for="(a, index) in link.arrLink" :key="index">
                <a href="">{{ a }}</a>
              </li>
            </ul>
          </ul> -->
        </div>
        <div class="footer_mid_r">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="footer_btn">
      <div class="sign-up_btn">
        <p>sign-up now!</p>
      </div>
      <div class="social">
        <p>follow us</p>
        <img src="../assets/img/footer-facebook.png" alt="">
        <img src="../assets/img/footer-twitter.png" alt="">
        <img src="../assets/img/footer-youtube.png" alt="">
        <img src="../assets/img/footer-pinterest.png" alt="">
        <img src="../assets/img/footer-periscope.png" alt="">
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
      ]
      // links: [
      //   {
      //     title: 'dc comics',
      //     arrLink: [
      //       'Characters',
      //       'Comics',
      //       'Movies',
      //       'TV',
      //       'Games',
      //       'Videos',
      //       'News'
      //     ]
      //   },
      //   {
      //     title: 'dc comics',
      //     arrLink: [
      //       'Characters',
      //       'Comics'
      //     ]
      //   },
      //   {
      //     title: 'dc comics',
      //     arrLink: [
      //       'Characters',
      //       'Comics'
      //     ]
      //   },
      //   {
      //     title: 'dc comics',
      //     arrLink: [
      //       'Characters',
      //       'Comics'
      //     ]
      //   }
      // ]
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables.scss";
footer{
  background-image: url(../assets/img/footer-bg.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  .footer_top{
      padding: 2rem;
      background-color: $blue;
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
  .footer_mid{
    height: 300px;
    color: white;
    .footer_mid_l{
      width: 50%;
    }
    .footer_mid_r{
      width: 50%;
      height: 300px;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      img{
        height: 150%;
      }
    }
  }
  .footer_btn{
    padding: 2rem;
    background-color: $gray;
    color: white;
    text-transform: uppercase;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .sign-up_btn{
      padding: 1rem;
      border: 2px solid $blue;
      cursor: pointer;
    }
    .social{
      display: flex;
      align-items: center;
      p{
        padding: 1rem;
        color: $blue;
        font-size: 20px;
        font-weight: 600;
      }
      img{
        padding: .5rem;
        cursor: pointer;
      }
    }
  }
}
</style>
