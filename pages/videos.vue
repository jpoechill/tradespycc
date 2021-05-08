<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Videos with explanations and ideas on trading SPY.  <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('spyArt')">Videos</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>I Lost Everything | Day Trading SPY Options for Beginners</strong> (NicholasWoolsey) [<a href="https://www.youtube.com/watch?v=EXGQiT2v83M">Link to video</a>]<br>
        Man loses everything trading SPY options. Great courage for sharing the story in the first place. While the creator's videos are well focused on finance and education, the attention on SPY accounts for only a small part of his general channel. Unfortunately, more entertaining that for serious learnings.
        <br><br>       
        <strong>Day Trading Tip | How I Use the SPY as a Day Trader to Make Me Money</strong> (ClayTrader) [<a href="https://www.youtube.com/watch?v=1kD66RMWimo">Link to video</a>]<br>
        Author describes some general concepts, and how SPY is used for reference of direction, when trading OTHER stocks. 
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
