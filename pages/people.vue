<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Mostly bios on Youtubers, and other internet personalities related to trading. <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('persons')">Personalities, Youtubers</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('investors')">Investors, Finance Specialists</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('figures')">World Figures</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Chris Sain</strong> (<a href="">YT Channel</a>)<br>
        Regular updates throughout the week. Tickers names are usually insightful, but after time gets repeated over and over. Insightful, overall.<br><br>
        <strong>Humbled Trader</strong> (<a href="https://www.youtube.com/channel/UCcIvNGMBSQWwo1v3n-ZRBCw">YT Channel</a>)<br>
        Humbled Trader is a Youtube personality that streams on a regular basis. Her trade videos are quirky and educational. <br><br>
        <strong>Warrior Trading</strong> (<a href="https://www.youtube.com/channel/UCBayuhgYpKNbhJxfExYkPfA">YT Channel</a>)<br>
        Cameron live-streams on a regular basis and runs his own learning platform. His streams cover his specialized strategy of scalping momentum trades every morning, of which the success of such can be seen throughout.<br><br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>Cathie Wood </strong>(<a href="https://ark-invest.com">ARK Invest Website</a>)<br>
        Cathie Wood runs ARK Invest, which ran with extraordinary returns in 2020. <br><br>
        <strong>Jim Kramer</strong> (<a href="https://www.cnbc.com/mad-money/">CNBC's Mad Money</a>)<br>
        Jim Kramer is a former hedge-fund'er and TV personality. <br><br>
        <strong>Elon Musk</strong> <br>
        The self-proclaimed <i>'Technoking'</i> of Tesla! <br><br>
        <strong>Chamath Palihapitiya</strong> <br>
        Finance person. <br><br>
        <strong>Warren Buffett</strong> <br>
        Investor. <br><br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        <strong>President Biden</strong> <br>
        POTUS. <br><br>
        <strong>Jerome Powell</strong> <br>
        Chairman of the Federal Reserve. <br>
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
          name: 'persons',
          isActive: true
        },
        {
          name: 'investors',
          isActive: false
        },
        {
          name: 'figures',
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
