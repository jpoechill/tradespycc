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
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('totalResets')">Total Resets</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" aria-current="page" href="#" @click="navigate('badResets')">Bad Resets</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[3].isActive }" href="#" @click="navigate('goodResets')">Good Resets</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-show="tabs[0].isActive">
     <div class="row">
        <div class="col-md-12">
          <iframe src="https://financhill.com/widget/charts/SPY?defaultOverlays=SMA50%2CSMA200&periodGrouping=daily&defaultSeries=candlesticks" width="100%" height="500" frameborder="0" scrolling="no" style="margin:0 auto;border: 0;" seamless></iframe>
          <!-- <img src="/chart_03.svg" class="w-100" alt=""> -->
          <br><br>

        <table class="table table-bordered">
          <thead>
            <tr>
              <th scope="col"></th>
              <th scope="col">Price</th>
              <th scope="col">Day's Gain/Loss Amount</th>
              <th scope="col">Day's Gain/Loss Percent</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">1 Day Ago</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
            <tr>
              <th scope="row">2 Days Ago</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
            <tr>
              <th scope="row">3 Days Ago</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </tbody>
        </table>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-show="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <img src="/chart_01.svg" class="w-100" alt="">
        <br><br>

        <table class="table table-bordered">
          <thead>
            <tr>
              <th scope="col"></th>
              <th scope="col">Bad Resets (Accounts Blown)</th>
              <th scope="col">Good Resets (Goals Reach – 200%+)</th>
              <th scope="col">Week Total</th>
              <th scope="col">Grand Total</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">May</th>
              <td>4</td>
              <td>1</td>
              <td>5</td>
              <td>6</td>
            </tr>
            <tr>
              <th scope="row">Before May</th>
              <td>0</td>
              <td>1</td>
              <td>0</td>
              <td>1</td>
            </tr>
          </tbody>
        </table>

       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-show="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        <img src="/chart_02.svg" class="w-100" alt="">
       <br><br>

        <table class="table table-bordered">
          <thead>
            <tr>
              <th scope="col"></th>
              <th scope="col">Bad Resets (Accounts Blown)</th>
              <th scope="col">Good Resets (Goals Reach – 200%+)</th>
              <th scope="col">Week Total</th>
              <th scope="col">Grand Total</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">Week 3</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
              <td>9</td>
            </tr>
            <tr>
              <th scope="row">Week 2</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
              <td>6</td>
            </tr>
            <tr>
              <th scope="row">Week 1</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
              <td>3</td>
            </tr>
          </tbody>
        </table>

       </div>
     </div>
   </div>



   <div class="container mt-4 mb-4" v-show="tabs[3].isActive">
     <div class="row">
       <div class="col-md-12">
        <img src="/chart_02.svg" class="w-100" alt="">
       <br><br>

        <table class="table table-bordered">
          <thead>
            <tr>
              <th scope="col"></th>
              <th scope="col">Bad Resets (Accounts Blown)</th>
              <th scope="col">Good Resets (Goals Reach – 200%+)</th>
              <th scope="col">Week Total</th>
              <th scope="col">Grand Total</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">Week 3</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
              <td>9</td>
            </tr>
            <tr>
              <th scope="row">Week 2</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
              <td>6</td>
            </tr>
            <tr>
              <th scope="row">Week 1</th>
              <td>1</td>
              <td>2</td>
              <td>3</td>
              <td>3</td>
            </tr>
          </tbody>
        </table>

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
          name: 'totalResets',
          isActive: false
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
