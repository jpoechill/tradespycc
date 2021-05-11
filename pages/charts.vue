<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Relevant data viz. <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('main')">SPY Daily</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" aria-current="page" href="#" @click="navigate('badResets')">Bad Resets</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('goodResets')">Good Resets</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-show="tabs[0].isActive">
     <div class="row">
        <div class="col-md-12">
          <iframe src="https://financhill.com/widget/charts/SPY?defaultOverlays=EMA50&periodGrouping=daily&defaultSeries=candlesticks" width="100%" height="500" frameborder="0" scrolling="no" style="margin:0 auto;border: 0;" seamless></iframe>
          <!-- <img src="/chart_03.svg" class="w-100" alt=""> -->
          <br><br>
          Data
          <hr class="my-1">
          Week 1: 3, Week 2: NA, Week 3: NA, Week 4: NA <br><br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-show="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <img src="/chart_01.svg" class="w-100" alt="">
        <br><br>
        Data
        <hr class="my-1">
        Week 1: 3, Week 2: NA, Week 3: NA, Week 4: NA <br><br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-show="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        <img src="/chart_02.svg" class="w-100" alt="">
       <br><br>
        Data
        <hr class="my-1">
        Week 1: 0, Week 2: NA, Week 3: NA, Week 4: NA <br><br><br>
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
          name: 'main',
          isActive: true
        },
        {
          name: 'badResets',
          isActive: false
        },
        {
          name: 'goodResets',
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
