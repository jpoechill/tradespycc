<template>
  <div>

   <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Website updates, blog/vlogs, stock purchases, etc. <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('marketObs')">Market Observations</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('tradeUps')">Trade Updates</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('websiteUps')">Website Updates</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
          May 10th, 2021. 
          <ul>
            <li>SPY momentum slowing down. QQQ (tech, growth) taking a hit. Crypto flaky.</li>
          </ul>
          May 7th, 2021. 
          <ul>
            <li>SPY breaking new highs. Really stumped; surprised. Just wow.</li>
            <li>Further dip sentiment, with traders taking long on SPY puts. [<a href="https://www.benzinga.com/etfs/broad-u-s-equity-etfs/21/05/21017410/options-trader-makes-3-78m-bet-the-top-is-nearby-for-spy">Reference via. @benzinga</a>]</li>
          </ul>
          May 5th, 2021. 
          <ul>
            <li>Crypto taking off, QQQ and tech taking more dips. SPY holding... for now.</li>
          </ul>
          May 4th, 2021. 
          <ul>
            <li>Nice hit on SPY and QQQ today. Market keeps hitting new highs, but how long will it last? [<a href="https://www.fool.com/investing/2021/05/04/why-zoom-video-fastly-and-square-stocks-all-fell-s/">Commentary via. @fool</a>]</li>
          </ul>
          May 2nd, 2021. 
          <ul>
            <li>Are we at the top..?</li>
          </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        May 7th, 2021. 
        <ul>
          <li>Realizing there are only so many trades of SPY you can make in a day. Considering opening an account with focus, but not limited to SPY.</li>
        </ul>
        May 2nd, 2021. 
        <ul>
          <li>Add, refine trade content. Add TOS account for tracking. </li>
        </ul>
        April 29th, 2021. 
        <ul>
          <li>Buy SPY from recent ATH for SAFE 1, MODERATE 1 accounts. </li>
        </ul>
        April 27th, 2021. 
        <ul>
          <li>Was trying to find a good platform that would allow me to make multiple paper trading accounts under one platform. Tried a bunch of different things but none ended up working as well as I wished. So now, currently, I'm hoping to continue messing with TD's Think or Swim app, and go forward with looking how to put together my own little game, via. this website somehow.</li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        May 7th, 2021. 
        <ul>
          <li>Update layout, design.</li>
        </ul>
        May 5th, 2021. 
        <ul>
          <li>Add arrow keys for navigation. Add content, and fix up styles/formatting.</li>
        </ul>
        April 30th, 2021. 
        <ul>
          <li>Added charts section (empty), and updated portfolios page with real time SPY price (API). Started reading "Around the World...".</li>
        </ul>
        April 29th, 2021. 
        <ul>
          <li>Refine content, push to web. </li>
        </ul>
        April 28th, 2021. 
        <ul>
          <li>Add content to websites section and other links. </li>
        </ul>
        April 27th, 2021. 
        <ul>
          <li>Mock website layout and begin filling general content. </li>
        </ul>
        April 24th, 2021. 
        <ul>
          <li>Purchase domain name.</li>
        </ul>
       </div>
     </div>
   </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      tabs: [
        {
          name: 'marketObs',
          isActive: true
        },
        {
          name: 'tradeUps',
          isActive: false
        },
        {
          name: 'websiteUps',
          isActive: false
        }
      ]
    }
  },
  methods: {
    navigate (page) {
      let tabs = this.tabs
      for (let index in tabs) {
        if (tabs[index].name === page) {
          tabs[index].isActive = true
        } else {
          tabs[index].isActive = false
        }
      } 
    }
  }
}
</script>

<style>
</style>
