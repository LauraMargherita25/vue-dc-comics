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
            <ul>
              <h2>dc comics</h2>
              <li><a href="#">Characters</a></li>
              <li><a href="#">Comics</a></li>
              <li><a href="#">Movies</a></li>
              <li><a href="#">TV</a></li>
              <li><a href="#">Games</a></li>
              <li><a href="#">Videos</a></li>
              <li><a href="#">News</a></li>
            </ul>
            <ul>
              <h2>shop</h2>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
            <ul>
              <h2>dc</h2>
              <li><a href="#">Terms Of Use</a></li>
              <li><a href="#">Privacy policy (New)</a></li>
              <li><a href="#">Ad Choices</a></li>
              <li><a href="#">Advertising</a></li>
              <li><a href="#">Jobs</a></li>
              <li><a href="#">Subscriptions</a></li>
              <li><a href="#">Talent Workshops</a></li>
              <li><a href="#">CPSC Certificates</a></li>
              <li><a href="#">Ratings</a></li>
              <li><a href="#">Shop Help</a></li>
              <li><a href="#">Contact Us</a></li>
            </ul>
            <ul>
              <h2>sites</h2>
              <li><a href="#">DC</a></li>
              <li><a href="#">MAD Magazine</a></li>
              <li><a href="#">DC Kids</a></li>
              <li><a href="#">DC Universe</a></li>
              <li><a href="#">DC Power Visa</a></li>
            </ul>
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
    background-color: $blue;
    color: white;
    ul{
      width: 100%;
      padding: 2rem 0;
      display: flex;
      justify-content: space-evenly;
      li{
        display: inline-block;
        padding: 1rem;
      }
      a{
        display: inline-block;
      }
    }
  }
  .footer_mid{
    height: 300px;
    color: white;
    .footer_mid_l{
      width: 50%;
      display: flex;
      ul{
        margin: 0 1rem;
        h2{
          margin-bottom: 1rem;
          text-transform: uppercase;
        }
        li{
          margin-bottom: .3rem;
          font-size: 13px;
          color: $gray_text;
        }
      }
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
