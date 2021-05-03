<template>
  <div>
    <div class="css-selector" style="position: fixed; width: 12px; height: 12px; left: 0; right: 0;">

    </div>
    <div class="container pt-4">
      <div class="row">
        <div class="col-md-12 text-center">
          <nuxt-link to="/" style="color: #111;"><strong>$TRADESPY.cc</strong> </nuxt-link> <br>
          <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">OTHER RESOURCES (MISC)</nuxt-link>
        </div>
      </div>
    </div>
  
    <Nuxt />

    <div class="container mt-2 mb-2">
      <div class="row">
        <div class="col-md-12 text-center mt-4 mb-4">
          SPY: ${{ spyCurr }} | Unique View Count: 000<br><br>
          <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <nuxt-link to="/">PORTFOLIOS</nuxt-link> | <nuxt-link to="/strategies">STRATEGIES</nuxt-link> | <nuxt-link to="/charts">CHARTS</nuxt-link> | <nuxt-link to="/articles">ARTICLES</nuxt-link>  | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">OTHER RESOURCES (MISC)</nuxt-link>
          <br>
          This website was built solely, and strictly for educational purposes. © 2021
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from 'axios'

export default {
  methods: {
    numberWithCommas: function (x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    }
  },
  data () {
    return {
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
  mounted () {
    let self = this
    // axios.request(self.options).then(function (response) {
    //   console.log(response.data);
    // }).catch(function (error) {
    //   console.error(error);
    // });
    axios.get('https://cloud.iexapis.com/stable/stock/' + 'SPY' + '/quote?token=pk_d8826aae332a4b1287b1d4399e2f860b')
        .then(function (response) { 
            self.spyCurr = response.data.iexRealtimePrice
            console.log(response)
          })
        .catch(function (error) {
          console.log(error);
        })
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
