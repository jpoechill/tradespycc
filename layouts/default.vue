<template>
  <div>
    <div class="css-selector" style="position: fixed; width: 18px; height: 18px; left: 0; right: 0;">

    </div>
    <div class="container pt-4">
      <div class="row">
        <div class="col-md-12 text-center">
          <nuxt-link to="/" style="color: #111;"><strong>$TRADESPY.cc</strong> </nuxt-link> <br>
          <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/videos">VIDEOS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">OTHER RESOURCES (MISC)</nuxt-link>
        </div>
      </div>
    </div>
  
    <Nuxt />

    <div class="container mt-2 mb-2">
      <div class="row">
        <div class="col-md-12 text-center mt-4 mb-4">
          SPY: ${{ spyCurr }} | Unique View Count: 000<br><br>
          <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/videos">VIDEOS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">OTHER RESOURCES (MISC)</nuxt-link>
          <br>
          This is a SPY research and development PAPER TRADING website, built solely and strictly for educational purposes. © 2021
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from 'axios'

export default {
  data () {
    return {
      paths: [
        '/about',
        '/articles',
        '/books',
        '/charts',
        '/feed',
        '/',
        '/misc',
        '/people',
        '/strategies',
        '/videos',
        '/websites',
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
    this.addEventListeners()
    this.getSPYPrice()
  }
}
</script>

<style>
</style>


<style>
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
</style>
