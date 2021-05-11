<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Websites that talk about trading spy and other related securities.  <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('chartsTools')">Daily Charts and Tools</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('general')">Trading General, News</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('specific')">Other (SPY Specific)</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Slickcharts</strong> <a href="https://www.investing.com/etfs/spdr-s-p-500-technical" target="_blank">Link to source.</a><br>
        Current SPY charts with technical details and current/emerging chart patterns. <br><br>

        <strong>Slickcharts</strong> <a href="https://www.slickcharts.com/sp500" target="_blank">Link to source.</a><br>
        Simple website that shows list of all companies and recent prices in the S&P500. <br><br>

        <strong>FINVIZ</strong> <a href="https://finviz.com" target="_blank">Link to source.</a><br>
        Charts and numbers; no fluff. <br><br>

        <strong>Barchart</strong> <a href="https://www.barchart.com/" target="_blank">Link to source.</a><br>
        News, tools, and other market data. Great interactive UIs for comparing tickers.<br><br>
  
        <strong>Benzinga Options</strong> <a href="https://www.benzinga.com/markets/options" target="_blank">Link to source.</a><br>
        Unusual options activities by <i>"smart money"</i> managers, via. Benzinja. Updated daily.
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <a href="https://marketwatch.com" target="_blank">Marketwatch</a>, <a href="https://finance.yahoo.com" target="_blank">Yahoo! Finance</a>, <a href="https://seekingalpha.com" target="_blank">Seeking Alpha</a>, <a href="https://fool.com" target="_blank">Motley Fool</a>, r/WallStreetBets <br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>SPX Option Trader</strong> (No Affiliation) <a href="">Link to source.</a><br>
        Tim is a veteran trader, offering insights into trading SPY options and credit spreads. The website is informative, with an overuse of stock images. It seems to be updated regularly with their trading performance. There is a 7 day trial, with plans starting at $200/month. Hoping to explore more, and update here with a review.
        
        <br><br>
        <strong>Day Trade SPY</strong> (No Affiliation) <a href="">Link to source.</a><br>
        Hugh and Alex are traders with a focus on SPY. Their website offers a FAQs and blog. Access to their product starts at $600, with weekly communications for $100/week.
        
        <br><br>
        <strong>S&P 500 Futures Trading Group</strong> (No Affiliation) <a href="">Link to source.</a><br>
        This group trades the S&P 500 E-mini. They are located in Arizona, and apparently works through in-person meetings. Membership pricing is not available.<br><br>
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
          name: 'chartsTools',
          isActive: true
        },
        {
          name: 'general',
          isActive: false
        },
        {
          name: 'specific',
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
