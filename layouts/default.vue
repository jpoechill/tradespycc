<template>
  <div>
    <div style="position: fixed; z-index: 2; left: 10px; top: 13px;">
      <img src="/art.png" width="38px" alt="">
    </div>

    <!-- <div style="z-index: 999; position: fixed; left: 0px; bottom: 6px;">
      <img src="/kitten_trans.gif" width="110px" alt="">
    </div>

    <div class="rotate" style="z-index: 999; position: fixed; left: 12px; bottom: 50%;">
      <img src="/edna.png" width="58px" alt="">
    </div>

    <div class="rotate" style="z-index: 999; position: fixed; right: 12px; bottom: 50%;">
      <img src="/peele.png" width="58px" alt="">
    </div>


    <div style="z-index: 999; position: fixed; right: 18px; top: 22px;">
      <img src="/binary.svg" width="32px" alt="">
    </div>

    <div style="z-index: 999; position: fixed; right: 50%; bottom: 12px;">
      <img src="/dog.png" width="52px" alt="">
    </div>

    <div style="z-index: 999; position: fixed; right: 14px; bottom: 14px;">
      <img src="/heart!.svg" width="30px" alt="">
    </div> -->

    <div class="pb-1" style="background-color: rgb(222 222 255);">

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

      <div style="background-color: #f9f9f9; position: fixed; width: 100%; z-index: 1;" class="border-top">
        <div class="container py-2">
          <div class="col-md-12 mt-3 mb-0 ms-0 ps-0">
          <small>
          <nuxt-link to="/feed" style="font-size: 14px; color: #111;" class="me-2"><strong>$TRADESPY.cc</strong> </nuxt-link>
          <!-- <nuxt-link to="/" style="color: #111;"><img src="/logo.svg" width="175px" class="mb-1" alt="tradeSPY.cc Logo"></nuxt-link> -->
          
          </small>
          </div>
          <!-- <div class="row">
            <div class="col-md-12 text-center" style="word-spacing: 0px;">
              <ul class="nav nav-fill justify-content-center">
                <li class="nav-item" style="z-index: 1;" v-for="(tab, index) in tabs" :key="index">
                  <nuxt-link :to="tab.path" class="nav-link text-uppercase" :class="{ ooga: tab.isActive }"> {{ tab.title }}</nuxt-link>
                </li>
              </ul>  
            </div>
          </div> -->
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

      <div style="margin-top: 67px;">
        <Nuxt/>
      </div>

    </div>

    <!-- <div class="container bg-dark"> -->
      <!-- <div class="row px-0 mx-0" style="background-color: #f9f9f9;">
        <img src="wave.svg"  class="pt-4 pb-3 mx-0 px-0 w-100" alt="">
      </div> -->
    <!-- </div> -->

    <div class="container mt-2">
      <div class="row">
        <div class="col-md-12 mt-0 mb-0">
          <!-- <nuxt-link to="/" style="font-size: 14px; color: #111;"><strong>$TRADESPY.cc</strong> </nuxt-link> -->
          <!-- <nuxt-link to="/" style="color: #111;"><img src="/logo.svg" width="175px" class="mb-1" alt="tradeSPY.cc Logo"></nuxt-link> -->
        </div>
        <small>
        <div class="col-md-12 ms-0 text-left ps-1 pt-1">
          <!-- <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIO</nuxt-link> |  <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/resources">RESOURCES</nuxt-link> -->
        </div>
        </small>
        <div class="col-md-12 mt-0 mb-5 text-white">
          <!-- <hr> -->
          <!-- <small> -->
            <!-- <nuxt-link to="/about">About</nuxt-link> | Feed | <nuxt-link to="/charts">Charts</nuxt-link> | <nuxt-link to="/strategies">Strategies</nuxt-link> | <nuxt-link to="/resources">Resources</nuxt-link> | <nuxt-link to="/resources">Updates</nuxt-link><br> -->
            Research days/week: 1/5 | PT days/week: 1/5 | SPY: <a href="https://finance.yahoo.com/chart/SPY#eyJpbnRlcnZhbCI6MSwicGVyaW9kaWNpdHkiOjEsInRpbWVVbml0IjoibWludXRlIiwiY2FuZGxlV2lkdGgiOjE2LjgxMTU5NDIwMjg5ODU1LCJmbGlwcGVkIjpmYWxzZSwidm9sdW1lVW5kZXJsYXkiOnRydWUsImFkaiI6dHJ1ZSwiY3Jvc3NoYWlyIjp0cnVlLCJjaGFydFR5cGUiOiJjYW5kbGUiLCJleHRlbmRlZCI6ZmFsc2UsIm1hcmtldFNlc3Npb25zIjp7fSwiYWdncmVnYXRpb25UeXBlIjoib2hsYyIsImNoYXJ0U2NhbGUiOiJsaW5lYXIiLCJwYW5lbHMiOnsiY2hhcnQiOnsicGVyY2VudCI6MSwiZGlzcGxheSI6IlNQWSIsImNoYXJ0TmFtZSI6ImNoYXJ0IiwiaW5kZXgiOjAsInlBeGlzIjp7Im5hbWUiOiJjaGFydCIsInBvc2l0aW9uIjpudWxsfSwieWF4aXNMSFMiOltdLCJ5YXhpc1JIUyI6WyJjaGFydCIsIuKAjHZvbCB1bmRy4oCMIl19fSwibGluZVdpZHRoIjoyLCJzdHJpcGVkQmFja2dyb3VuZCI6dHJ1ZSwiZXZlbnRzIjp0cnVlLCJjb2xvciI6IiMwMDgxZjIiLCJzdHJpcGVkQmFja2dyb3VkIjp0cnVlLCJldmVudE1hcCI6eyJjb3Jwb3JhdGUiOltdLCJzaWdEZXYiOnt9fSwic3ltYm9scyI6W3sic3ltYm9sIjoiU1BZIiwic3ltYm9sT2JqZWN0Ijp7InN5bWJvbCI6IlNQWSIsInF1b3RlVHlwZSI6IkVURiIsImV4Y2hhbmdlVGltZVpvbmUiOiJBbWVyaWNhL05ld19Zb3JrIn0sInBlcmlvZGljaXR5IjoxLCJpbnRlcnZhbCI6MSwidGltZVVuaXQiOiJtaW51dGUiLCJzZXRTcGFuIjpudWxsfV0sImN1c3RvbVJhbmdlIjpudWxsLCJzdHVkaWVzIjp7IuKAjHZvbCB1bmRy4oCMIjp7InR5cGUiOiJ2b2wgdW5kciIsImlucHV0cyI6eyJpZCI6IuKAjHZvbCB1bmRy4oCMIiwiZGlzcGxheSI6IuKAjHZvbCB1bmRy4oCMIn0sIm91dHB1dHMiOnsiVXAgVm9sdW1lIjoiIzAwYjA2MSIsIkRvd24gVm9sdW1lIjoiI2ZmMzMzYSJ9LCJwYW5lbCI6ImNoYXJ0IiwicGFyYW1ldGVycyI6eyJ3aWR0aEZhY3RvciI6MC40NSwiY2hhcnROYW1lIjoiY2hhcnQiLCJwYW5lbE5hbWUiOiJjaGFydCJ9fSwi4oCMbWHigIwgKDUwLEMsbWEsMCkiOnsidHlwZSI6Im1hIiwiaW5wdXRzIjp7IlBlcmlvZCI6NTAsIkZpZWxkIjoiQ2xvc2UiLCJUeXBlIjoic2ltcGxlIiwiT2Zmc2V0IjowLCJpZCI6IuKAjG1h4oCMICg1MCxDLG1hLDApIiwiZGlzcGxheSI6IuKAjG1h4oCMICg1MCxDLG1hLDApIn0sIm91dHB1dHMiOnsiTUEiOiIjYWQ2ZWZmIn0sInBhbmVsIjoiY2hhcnQiLCJwYXJhbWV0ZXJzIjp7ImNoYXJ0TmFtZSI6ImNoYXJ0IiwicGFuZWxOYW1lIjoiY2hhcnQifX0sIuKAjG1h4oCMICgyMDAsQyxtYSwwKSI6eyJ0eXBlIjoibWEiLCJpbnB1dHMiOnsiUGVyaW9kIjoiMjAwIiwiRmllbGQiOiJDbG9zZSIsIlR5cGUiOiJzaW1wbGUiLCJPZmZzZXQiOiIwIiwiaWQiOiLigIxtYeKAjCAoMjAwLEMsbWEsMCkiLCJkaXNwbGF5Ijoi4oCMbWHigIwgKDIwMCxDLG1hLDApIn0sIm91dHB1dHMiOnsiTUEiOiIjZmYzMzNhIn0sInBhbmVsIjoiY2hhcnQiLCJwYXJhbWV0ZXJzIjp7ImNoYXJ0TmFtZSI6ImNoYXJ0IiwicGFuZWxOYW1lIjoiY2hhcnQifX19LCJzZXRTcGFuIjpudWxsLCJyYW5nZSI6bnVsbH0-">${{ spyCurr }} </a> | Scalptheory | Leetcode<br>
            A SPY research and development <del>PAPER TRADING</del> website. Built for educational purposes. © 2021
          <!-- </small> -->
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
      counter: '',
      tabs: [
        // {
        //   title: 'About',
        //   path: '/about',
        //   isActive: false,
        // },
        {
          title: '→ Feed',
          path: '/feed',
          toolTip: 'Website updates, blog/vlogs, stock purchases, etc.',
          isActive: false
        },
        // {
        //   // title: '→ Portfolio',
        //   // path: '/',
        //   // toolTip: 'Portfolio action and balances.',
        //   // isActive: false
        // },
        // {
        //   title: 'Strategies',
        //   path: '/strategies',
        //   isActive: false
        // },
        // {
        //   title: '→ Charts',
        //   path: '/charts',
        //   toolTip: 'Relevant data viz.',
        //   isActive: false
        // },
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
      spyCurr: "#",
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
    getCounter: function () {
      let self = this

      axios.get('https://jsonstorage.net/api/items/0de26d0c-0065-49d4-8990-98bf6c0f237c')
        .then(function (response) { 
          self.counter = response.data.counter
          self.updateCounter()

          })
        .catch(function (error) {
          console.log(error);
        })
    },
    updateCounter: function () {
      let self = this

      axios
        .put(
            "https://jsonstorage.net/api/items/0de26d0c-0065-49d4-8990-98bf6c0f237c", 
            {"counter": self.counter + 1},
            { headers: {
                "Content-Type": "application/json; charset=utf-8",
                "Data-Type": "json"
              }
            }
        )
        .catch(e => console.log(e));
    },
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

      console.log('SPY PRICE')

      axios.get('https://cloud.iexapis.com/stable/stock/' + 'SPY' + '/quote?token=pk_d8826aae332a4b1287b1d4399e2f860b')
        .then(function (response) { 
          console.log(response.data.latestPrice)
          self.spyCurr = response.data.latestPrice
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
    this.getCounter()
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
  font-size: 14px;
}

body {
  background-color: #FF6CBA;
}

.border-bottom {
  border-bottom: 58px solid rgb(249, 249, 249) !important;
}

.border-top {
  border-top: 8px solid yellow !important;
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

/* Rotate on hover */

.rotate {
  transition: transform .7s ease-in-out;
}

.rotate:hover {
  transform: rotate(360deg);
}
</style>
