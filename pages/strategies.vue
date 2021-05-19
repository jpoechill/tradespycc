<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Collected SPY strategies gathered from different sources, along with my own (in due time). <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('myStrats')">My Strategies</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('shortStrats')">Day Trading, Charting Strategies</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('longStrats')">SMA Strategies</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>'Riding the Wave' Strategy</strong> <br>
        Summary: Requires PDT. No holdings overnight. Ability to make gain regardless of market direction (down or up). Trade everyday. Development process.<br><br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Rainmaker Strategy.</strong> <br>
        Description here.<br><br>
        <strong>Heikin Ashi Charts strategy.</strong> <br>
        Description here. <br><br>
        <strong>"A SPY Day-Trading Strategy" by software developer, Matt Trivisonno.</strong> [<a href="http://www.trivisonno.com/trade/spy-strategy">Link to source.</a>] <br>
        A simple SPY day trading strategy with back tested data. Read, but not yet tested myself.<br><br>
        <strong>The 21 Most Popular Trading Strategies Every Serious Trader Should Learn To Succeed</strong> [<a href="https://quantstrategies.academy/2020/05/19/the-21-most-popular-trading-strategies-every-serious-trader-should-learn-to-succeed/?gclid=CjwKCAjwqIiFBhAHEiwANg9szuzWac__0wEf5As7dsNy68UAV0MN5MgWga37mjsJAj73bi9AhwsGTBoCOIoQAvD_BwE">Link to source.</a>] <br>
        A general and deep list of trading strategies, honestly, some I've never heard of. Have not reviewed.
       </div>
     </div>
   </div>

  <div class="container mt-4 mb-4" v-if="tabs[2].isActive">
    <div class="row">
      <div class="col-md-12">
        <strong>A Simple And Timeless Way To Trade The S&P 500 Successfully</strong> (SeekingAlpha, 2013) <a href="https://seekingalpha.com/article/1824492-a-simple-and-timeless-way-to-trade-the-s-and-p-500-successfully">Link to source.</a><br>
        Part 1 of 2, in a series of strategies using a mostly simple method of trading SPY via. following SMAs. <br><br>
        <strong>A Simple And Timeless Way To Trade The S&P 500 Successfully, Part 2 </strong> (SeekingAlpha, 2020) <a href="https://seekingalpha.com/article/4336117-simple-and-timeless-way-to-trade-s-and-p-500-successfully-part-2">Link to source.</a><br>
        Part 2 of 2, in a series of strategies using a mostly simple method of trading SPY via. following SMAs.
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
          name: 'myStrats',
          isActive: true
        },
        {
          name: 'shortStrats',
          isActive: false
        },
        {
          name: 'longStrats',
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
