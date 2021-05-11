<template>
  <div>
    <div style="position: fixed; width: 120px; height: 120px; left: 10px; top: 10px;">
      <img src="/cube.svg" width="34px" alt="">
    </div>

    <div style="z-index: 999; position: fixed; left: 0px; bottom: 6px;">
      <img src="/kitten_trans.gif" width="110px" alt="">
    </div>

    <div style="z-index: 999; position: fixed; right: 14px; top: 14px;">
      <img src="/binary.svg" width="30px" alt="">
    </div>

    <div style="z-index: 999; position: fixed; right: 14px; bottom: 14px;">
      <img src="/heart!.svg" width="30px" alt="">
    </div>

    <div class="bg-white pb-4 border-bottom">

      <div class="container pt-0">
        <div class="row pt-0">
          <!-- <div class="row">
            <small>
            <div class="col-md-12 text-center py-2">
              <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/videos">VIDEOS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">MISC</nuxt-link>
            </div>
            </small>
          </div> -->
        </div>
      </div>

      <!-- <div style="background-color: #f9f9f9;" class="mt-5">
        <div class="container py-2">
          <div class="row">
            <div class="col-md-2 text-left" style="word-spacing: 0px;">
              <nuxt-link to="/" style="color: #111;"><strong>$TRADESPY.cc</strong> </nuxt-link>
            </div>
            <div class="col-md-10 text-right" style="word-spacing: 0px;">
              <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/videos">VIDEOS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">MISC</nuxt-link>
            </div>
          </div>
        </div>
      </div> -->

      <div style="background-color: #f9f9f9;">
        <div class="container py-2">
          <div class="row">
            <div class="col-md-12 text-center" style="word-spacing: 0px;">
              <ul class="nav nav-fill justify-content-center">
                <li class="nav-item" v-for="(tab, index) in tabs" :key="index">
                  <nuxt-link :to="tab.path" class="nav-link text-uppercase" :class="{ ooga: tab.isActive }"> {{ tab.title }}</nuxt-link>
                </li>
              </ul>  
            </div>
          </div>
        </div>
      </div>

          <!-- color: #fff; -->
    <!-- background-color: #2F93FF; -->

      <!-- <div style="background-color: #f9f9f9;">
        <div class="container py-2">
          <div class="row">
            <div class="col-md-12 text-center" style="word-spacing: 0px;">
              <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/videos">VIDEOS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">MISC</nuxt-link>
            </div>
          </div>
        </div>
      </div> -->

      <Nuxt />

    </div>

    <div class="container mt-2">
      <div class="row">
        <div class="col-md-12 text-center mt-3 mb-0">
          <nuxt-link to="/" style="color: #111;"><strong>$TRADESPY.cc</strong> </nuxt-link>
        </div>
        <small>
        <div class="col-md-12 text-center pt-2">
          <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/videos">VIDEOS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">MISC</nuxt-link>
        </div>
        </small>
        <div class="col-md-12 text-center mt-0 mb-1">
          <hr>
          SPY: ${{ spyCurr }} | Unique View Count: 000<br>
        </div>
      </div>
    </div>

    <div style="background-color: #ECFEFF;">
      <div class="container">
        <div class="row">
        </div>
      </div>
    </div>

    <div class="container mb-2">
      <div class="row">
        <div class="col-md-12 text-center mt-1 mb-4">
          This is a SPY research and development PAPER TRADING website, built solely and strictly for educational purposes. © 2021
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from 'axios'
import Vue from 'vue'

export default {
  components: {
    dirs: [
      '~/components',
    ]
  },
  data () {
    return {
      tabs: [
        // {
        //   title: 'About',
        //   path: '/about',
        //   isActive: false,
        // },
        {
          title: 'Feed',
          path: '/feed',
          toolTip: 'Website updates, blog/vlogs, stock purchases, etc.',
          isActive: false
        },
        {
          title: 'Portfolios',
          path: '/',
          toolTip: 'Portfolio action and balances.',
          isActive: false
        },
        // {
        //   title: 'Strategies',
        //   path: '/strategies',
        //   isActive: false
        // },
        {
          title: 'Charts',
          path: '/charts',
          toolTip: 'Relevant data viz.',
          isActive: false
        },
        // {
        //   title: 'Articles',
        //   path: '/articles',
        //   isActive: false
        // },
        // {
        //   title: 'Books',
        //   path: '/books',
        //   isActive: false
        // },
        // {
        //   title: 'Videos',
        //   path: '/videos',
        //   isActive: false
        // },
        // {
        //   title: 'People',
        //   path: '/people',
        //   isActive: false
        // },
        // {
        //   title: 'Misc',
        //   path: '/misc',
        //   isActive: false
        // },
      ],
      paths: [
        // '/about',
        // '/articles',
        // '/books',
        '/feed',
        '/',
        '/charts',
        // '/misc',
        // '/people',
        // '/strategies',
        // '/videos',
        // '/websites',
      ],
      spyCurr: 0,
      options: {
        method: 'GET',
        url: 'https://apidojo-yahoo-finance-v1.p.rapidapi.com/auto-complete',
        params: {q: 'tesla', region: 'US'},
        headers: {
          'x-rapidapi-key': 'f9bba36e39msh6ce036ae6589a82p120958jsn561c2df5a048',
          'x-rapidapi-host': 'apidojo-yahoo-finance-v1.p.rapidapi.com'
        }
      },
      accounts: [
        {
          name: 'account 1',

        }
      ]
    }
  },
  computed: {
    currPath: function () {
      return this.$route.path
    }
  },
  methods: {
    setCurrPageActive: function () {
      const currPath = this.currPath
      const tabs = this.tabs

      for (let index in tabs) {
        if (tabs[index].path === currPath) {
          tabs[index].isActive = true
        } else {
          tabs[index].isActive = false
        }
      } 
    },
    numberWithCommas: function (x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    },
    navigate (direction) {
      // navigate PAGES via LEFT and RIGHT arrow keys
      let currIndex, newIndex

      currIndex = this.paths.indexOf(this.currPath)

      if (direction === 'LEFT') {
        if (currIndex === 0) {
          newIndex = this.paths.length - 1
        } else {
          newIndex = currIndex - 1
        }
      } else if (direction === 'RIGHT') {
        if (currIndex === this.paths.length - 1) {
          newIndex = 0
        } else {
          newIndex = currIndex + 1
        }
      }

      this.$router.push({
        path: this.paths[newIndex]
      })
    },
    getSPYPrice () {
      let self = this
      axios.get('https://cloud.iexapis.com/stable/stock/' + 'SPY' + '/quote?token=pk_d8826aae332a4b1287b1d4399e2f860b')
        .then(function (response) { 
          self.spyCurr = response.data.iexRealtimePrice
          })
        .catch(function (error) {
          console.log(error);
        })
    },
    addEventListeners () {
      let self = this

      window.addEventListener('keydown', (e) => {
        if (e.key == 'ArrowLeft') {
          self.navigate('LEFT')
        }

        if (e.key == 'ArrowRight') {
          self.navigate('RIGHT')
        }
      });
    }
  }, 
  mounted () {
      this.$nextTick(() => {
        // console.log('xxx')
        // console.log($('[data-toggle="tooltip"]').tooltip())
          $('[data-toggle="tooltip"]').tooltip()
      });
    this.setCurrPageActive()
    this.addEventListeners()
    this.getSPYPrice()
  },
  watch:{
    $route (to, from){
        this.setCurrPageActive()
      }
  } 
}
</script>

<style>
</style>


<style>
html {
  scroll-behavior: smooth;
}

body {
  background-color: #E7FEFF;
}

.border-bottom {
  border-bottom: 58px solid rgb(249, 249, 249) !important;
}

.ooga {
  border-bottom: 4px solid #2F93FF;
}

.css-selector {  
  background: linear-gradient(270deg, #0bdb00, #00b9ff, #f9ff00);
    background-size: 600% 600%;

    -webkit-animation: AnimationName 10s ease infinite;
    -moz-animation: AnimationName 10s ease infinite;
    animation: AnimationName 10s ease infinite;
}

@-webkit-keyframes AnimationName {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}
@-moz-keyframes AnimationName {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}
@keyframes AnimationName {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}

/* Tooltip container */
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black; /* If you want dots under the hoverable text */
}

/* Tooltip text */
.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
 
  /* Position the tooltip text - see examples below! */
  position: absolute;
  z-index: 1;
}

/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
  visibility: visible;
}
</style>
