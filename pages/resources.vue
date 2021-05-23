<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Resources found throughout the web covering a range of medium.<br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('articles')">Articles</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('books')">Books</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('eBooks')">E-books</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[3].isActive }" href="#" @click="navigate('video')">Video</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[4].isActive }" href="#" @click="navigate('tools')">Charts and Tools</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[5].isActive }" href="#" @click="navigate('platform')">Paid Platforms</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Mentally and Financially Ready to Flip the Switch? Paper Trading vs. Live Trading Accounts</strong> (John Manley, via. @TDAmeritrade) <a href="https://tickertape.tdameritrade.com/tools/paper-trading-vs-live-trading-accounts-15504">Link to article.</a><br>
        Great article with hints on what it takes to move to live trading. Tip: remain emotionally detached, and if so far successful, your stripes may be well earned!
        <br><br>
        <strong>Transitioning From Demo to Live Day Trading</strong> (Cory Mitchell, via. @theBalance) <a href="https://www.thebalance.com/transitioning-from-demo-to-live-day-trading-1031432">Link to article.</a><br>
        Thoughts on transitioning from paper to live trading. Best quotes: "Day traders need to trade—and know when not to trade", "Being a successful live trader requires completely embracing losing trades", "when trading a live account, start out with the smallest position size possible."
        <br><br>
        <strong>Technical Analysis</strong> (StockCharts.com) <a href="https://school.stockcharts.com/doku.php?id=overview:technical_analysis">Link to article.</a><br>
        General run down for better understanding candles, charts, and TA (technical analysis) – as boring as it sounds.
        <br><br>
        <strong>How I Day Trade the SPY</strong> (Spicer Matthews) <a href="https://options.cafe/blog/how-i-day-trade-the-spy">Link to article.</a><br>
        This short article is short, but quite in depth. Talks about daytrading calls and puts. A++ for content.
        <br><br>
        <strong>Coinbase vs. Robinhood</strong> (Investopedia) <a href="https://www.investopedia.com/coinbase-vs-robinhood-5176293">Link to article.</a><br>
        An article comparing Coinbase and Robinhood for trading crypto. In this case, Robinhood wins the argument for the more simple-minded trader, while Coinbase takes it for any "Pro" level individual looking for more features and coin varieties.  
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Around The World: Day Trading The SPY, Day Trading The SPY; Zero To Hero</strong> <a href="https://www.amazon.com/Around-World-Day-Trading-SPY-ebook/dp/B0732Z744L/">Link to source.</a><br>
        Roughly 80 pages in regards to traveling the world and day trading options in SPY. Although it was generally an easy read, some concept as to how options work may be strange to anyone new to trading. From the description, this text describes a particular "Rainmaker" strategy. In somewhat more detail, this strategy utilizes reading SPY's daily chart (and MACD indicator), to following the trend and taking quick small profits. While the author describes the strategy for which can that be used for any particular portfolio size, I could imagine that trading under PDT could bring some issues. The author makes it clear that losses are to be expected, which is just the reality.
        <br><br>
        Overall, I enjoyed the brevity and conciseness of this text. Best quote: "Trading is a process!" (pg. 58).
        <br><br>
        <strong>Day Trade the S&P 500 Index for Fun and Profit: A Unique Method for Using Heikin Ashi Charts to Day Trade...</strong> <a href="">Link to source.</a><br>
        Another short book – technical, concise and well organized. The strategy here might be the most simple yet, and simply goes into reading daily candles, ignoring any type of indicators. While the text descrives using this strategy to trade future contracts, it is noted that the ETF should work also. Hoping to come back to dig deeper and back test some of its recommendations.
        <br><br>
        <strong>The MEJT System: A New Tool for Day Trading the S&P 500 Index</strong> <a href="https://www.amazon.com/MEJT-System-Tool-Trading-Index/dp/0857190350/">Link to source.</a><br>
        While yet to read, the content in said text appears to be substantial. Also, and apparently, the author hosts his own YT channel where past charts are reviewed daily.
        <br><br>
        <strong>Anatomy of $SPY on First Trading Day of the Month by Kora Reddy (2019)</strong> <a href="">Link to source.</a><br>
        Interested. <br><br><strong>S&P 500 Trading Mastery: A Systematic Trading Plan for Capturing Stock Index Profits</strong> <a href="">Link to source.</a><br>
        No text. <br><br>
        <strong>$SPY High Probability Trading Strategies by Kora Reddy (2019)</strong> <a href="">Link to source.</a><br>
        No text. <br><br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>S&P500 Index Strategy: Scalp the S&P index with profitable and reliable strategy</strong> <a href="">Link to source.</a><br>
        Short text, short strategy. While the 1 year performance chart seemed impressive, the layout and content of the book was weak and lacked any details to examples for a reader to really undstand what was going on. Bargain buy; may come back.
        <br><br>
        <strong>Price-Forecasting Models for iShares Core S&P 500 ETF IVV Stock (Top 100 ETFs By Assets)</strong> <a href="">Link to source.</a><br>
        No text. <br><br>
        <strong>87% Win Trading S&P 500: Foolproof strategy to profit from the stock market</strong> <a href="">Link to source.</a><br>
        No text. <br><br>
        <strong>S&P 500 Playbook: The only trends you need to know to make serious money on the stock market</strong> <a href="">Link to source.</a><br>
        No text. <br><br>
        <strong>S&P 500 Earnings, Valuation, and the Pandemic: A Primer for Investors (Predicting the Markets Topical Study Book 4)</strong> <a href="">Link to source.</a><br>
        No text. <br><br>
       </div>
     </div>
   </div>

    <div class="container mt-4 mb-4" v-if="tabs[3].isActive">
     <div class="row">
       <div class="col-md-12">
        No content.
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[4].isActive">
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

   <div class="container mt-4 mb-4" v-if="tabs[5].isActive">
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
          name: 'articles',
          isActive: true
        },
        {
          name: 'books',
          isActive: false
        },
        {
          name: 'eBooks',
          isActive: false
        },
        {
          name: 'video',
          isActive: false
        },
        {
          name: 'tools',
          isActive: false
        },
        {
          name: 'platform',
          isActive: false
        },
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
