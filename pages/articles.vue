<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Articles found around the web and otherwise that are not particular to a single book, or website. <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('spyArt')">SPY Articles</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('cryptArt')">Crypto Articles</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>How I Day Trade the SPY</strong> (Spicer Matthews) <a href="https://options.cafe/blog/how-i-day-trade-the-spy">Link to article.</a><br>
        This short article is short, but quite in depth. Talks about daytrading calls and puts. A++ for content.
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Coinbase vs. Robinhood</strong> (Investopedia) <a href="https://www.investopedia.com/coinbase-vs-robinhood-5176293">Link to article.</a><br>
        An article comparing Coinbase and Robinhood for trading crypto. In this case, Robinhood wins the argument for the more simple-minded trader, while Coinbase takes it for any "Pro" level individual looking for more features and coin varieties.
        <br>
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
          name: 'spyArt',
          isActive: true
        },
        {
          name: 'cryptArt',
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
 