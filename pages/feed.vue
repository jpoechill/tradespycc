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
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('resourceUps')">Resources Updates</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('tradeUps')">Platform Updates</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[3].isActive }" href="#" @click="navigate('websiteUps')">Website Updates</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
          May 14th, 2021.
          <ul>
            <li>Continued SPY gains. Starting to find success in following the flow of the market.</li>
            <li>Notable movers: XLE, XLF. [<a href="https://seekingalpha.com/news/3696789-sp-500s-weekly-market-breakdown-and-sector-performance">Reference via. @seekingalpha</a>] </li>
            <li>Questions: Have growth stocks been primed for a return? Or is it still too early?</li>
          </ul>
          May 13th, 2021.
          <ul>
            <li>Comeback. <span class="badge bg-success">Reversal</span></li>
          </ul>
          May 12th, 2021.
          <ul>
            <li>Continued down trend. All stocks and equities. Cause: fear of inflation. [<a href="https://finance.yahoo.com/news/stock-market-news-live-updates-may-12-2021-221905341.html">Reference via. @yahoo.com</a>]</li>
            <li>The fall is here. To re-iterate from earlier: how long does this last, and how far will it go? Questions. </li>
          </ul>
          May 11th, 2021. 
          <ul>
            <li>SPY takes another hit. The question now: how long does this last, and how far will it go? <span class="badge bg-danger">Reversal</span></li>
          </ul>
          May 10th, 2021. 
          <ul>
            <li>SPY momentum slowing down. QQQ (tech, growth) taking a hit. Crypto flaky. [<a href="https://www.investing.com/analysis/trading-the-sp-500s-latest-wobble-what-the-faang-stocks-are-telling-us-200579135">Reference via. investing.com</a>]</li>
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
          May 14th, 2021. 
          <ul>
            <li>Best SPY (et others) heat map found so far: [<a href="https://finviz.com/map.ashx">@Finviz Heap Map</a>]</li>
            <li>Best SPY daily chart found so far: [<a href="https://finance.yahoo.com/chart/SPY/#eyJpbnRlcnZhbCI6ImRheSIsInBlcmlvZGljaXR5IjoxLCJ0aW1lVW5pdCI6bnVsbCwiY2FuZGxlV2lkdGgiOjYuOTc2MDQ3OTA0MTkxNjE3LCJmbGlwcGVkIjpmYWxzZSwidm9sdW1lVW5kZXJsYXkiOnRydWUsImFkaiI6dHJ1ZSwiY3Jvc3NoYWlyIjp0cnVlLCJjaGFydFR5cGUiOiJsaW5lIiwiZXh0ZW5kZWQiOmZhbHNlLCJtYXJrZXRTZXNzaW9ucyI6e30sImFnZ3JlZ2F0aW9uVHlwZSI6Im9obGMiLCJjaGFydFNjYWxlIjoibGluZWFyIiwicGFuZWxzIjp7ImNoYXJ0Ijp7InBlcmNlbnQiOjEsImRpc3BsYXkiOiJTUFkiLCJjaGFydE5hbWUiOiJjaGFydCIsImluZGV4IjowLCJ5QXhpcyI6eyJuYW1lIjoiY2hhcnQiLCJwb3NpdGlvbiI6bnVsbH0sInlheGlzTEhTIjpbXSwieWF4aXNSSFMiOlsiY2hhcnQiLCLigIx2b2wgdW5kcuKAjCJdfX0sInNldFNwYW4iOm51bGwsImxpbmVXaWR0aCI6Miwic3RyaXBlZEJhY2tncm91bmQiOnRydWUsImV2ZW50cyI6dHJ1ZSwiY29sb3IiOiIjMDA4MWYyIiwic3RyaXBlZEJhY2tncm91ZCI6dHJ1ZSwiZXZlbnRNYXAiOnsiY29ycG9yYXRlIjpbXSwic2lnRGV2Ijp7fX0sInN5bWJvbHMiOlt7InN5bWJvbCI6IlNQWSIsInN5bWJvbE9iamVjdCI6eyJzeW1ib2wiOiJTUFkiLCJxdW90ZVR5cGUiOiJFVEYiLCJleGNoYW5nZVRpbWVab25lIjoiQW1lcmljYS9OZXdfWW9yayJ9LCJwZXJpb2RpY2l0eSI6MSwiaW50ZXJ2YWwiOiJkYXkiLCJ0aW1lVW5pdCI6bnVsbCwic2V0U3BhbiI6bnVsbH1dLCJjdXN0b21SYW5nZSI6bnVsbCwic3R1ZGllcyI6eyLigIx2b2wgdW5kcuKAjCI6eyJ0eXBlIjoidm9sIHVuZHIiLCJpbnB1dHMiOnsiaWQiOiLigIx2b2wgdW5kcuKAjCIsImRpc3BsYXkiOiLigIx2b2wgdW5kcuKAjCJ9LCJvdXRwdXRzIjp7IlVwIFZvbHVtZSI6IiMwMGIwNjEiLCJEb3duIFZvbHVtZSI6IiNmZjMzM2EifSwicGFuZWwiOiJjaGFydCIsInBhcmFtZXRlcnMiOnsid2lkdGhGYWN0b3IiOjAuNDUsImNoYXJ0TmFtZSI6ImNoYXJ0IiwicGFuZWxOYW1lIjoiY2hhcnQifX0sIuKAjG1h4oCMICg1MCxDLG1hLDApIjp7InR5cGUiOiJtYSIsImlucHV0cyI6eyJQZXJpb2QiOjUwLCJGaWVsZCI6IkNsb3NlIiwiVHlwZSI6InNpbXBsZSIsIk9mZnNldCI6MCwiaWQiOiLigIxtYeKAjCAoNTAsQyxtYSwwKSIsImRpc3BsYXkiOiLigIxtYeKAjCAoNTAsQyxtYSwwKSJ9LCJvdXRwdXRzIjp7Ik1BIjoiI2FkNmVmZiJ9LCJwYW5lbCI6ImNoYXJ0IiwicGFyYW1ldGVycyI6eyJjaGFydE5hbWUiOiJjaGFydCJ9fSwi4oCMbWHigIwgKDIwMCxDLG1hLDApIjp7InR5cGUiOiJtYSIsImlucHV0cyI6eyJQZXJpb2QiOiIyMDAiLCJGaWVsZCI6IkNsb3NlIiwiVHlwZSI6InNpbXBsZSIsIk9mZnNldCI6IjAiLCJpZCI6IuKAjG1h4oCMICgyMDAsQyxtYSwwKSIsImRpc3BsYXkiOiLigIxtYeKAjCAoMjAwLEMsbWEsMCkifSwib3V0cHV0cyI6eyJNQSI6IiNmZjMzM2EifSwicGFuZWwiOiJjaGFydCIsInBhcmFtZXRlcnMiOnsiY2hhcnROYW1lIjoiY2hhcnQifX19LCJyYW5nZSI6bnVsbH0-">@Yahoo SPY Chart</a>]</li>
            <li>"Flash crashe(s)" in recent history, and why we might continue to see more. Also, evidence that recoveries are usually quick. [<a href="https://www.investopedia.com/articles/investing/011116/two-biggest-flash-crashes-2015.asp?utm_campaign=quote-yahoo&utm_source=yahoo&utm_medium=referral">Reference via. Investopedia</a>]</li>
          </ul>
          May 10th, 2021. 
          <ul>
            <li>New article: An interesting article via. r/options re: research and results of trades made by US Senators. Concludes with data that shows there are winners and losers, that not surpisingly the tech (FAANG) is the most popular, and that such politicians do well enough to beat the S&P 500. [<a href="https://www.reddit.com/r/options/comments/n940ze/i_analyzed_9000_trades_made_by_us_senators_in_the/">Reference via. r/options</a>]</li>
            <li>New tools site: Another great SPY reference site, detailing past and current SPY candlestick patterns. Hyper useful. [<a href="https://www.investing.com/etfs/spdr-s-p-500-technical">Reference via. @investing.com</a>]</li>
          </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        May 12th, 2021.
        <ul>            
          <li>Remove stocks from Aggro 1 account, and update to options only.</li>
        </ul>
        May 10th, 2021.
        <ul>            
          <li>Considering whether I should continue planning on trying to utiltize leveraged ETFs, or giving it up and just sticking to options. Such ETFs seem to only add another layer of complexity to things already happening.</li>
          <li>Possibly: One idea could be to dedicate and build an entire to platform for such strategy?</li>
        </ul>
        May 7th, 2021. 
        <ul>
          <li>Realizing there are only so many trades of SPY you can make in a day. Considering opening an account with focus, but not limited to SPY.</li>
        </ul>
        April 27th, 2021. 
        <ul>
          <li>Was trying to find a good platform that would allow me to make multiple paper trading accounts under one platform. Tried a bunch of different things but none ended up working as well as I wished. So now, currently, I'm hoping to continue messing with TD's Think or Swim app, and go forward with looking how to put together my own little game, via. this website somehow.</li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[3].isActive">
     <div class="row">
       <div class="col-md-12">
        May 10th, 2021. 
        <ul>
          <li>Layout update.</li>
        </ul>
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
          name: 'resourceUps',
          isActive: false
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
