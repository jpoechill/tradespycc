<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Mostly bios on Youtubers, and other internet personalities related to trading. <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('persons')">People</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('investors')">Web Links</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
        Personalities, Youtubers<br>
        <hr class="my-1">
        <strong>Chris Sain</strong> (<a href="">YT Channel</a>)<br>
        Regular updates throughout the week. Tickers names are usually insightful, but after time gets repeated over and over. Insightful, overall.<br><br>
        <strong>Humbled Trader</strong> (<a href="https://www.youtube.com/channel/UCcIvNGMBSQWwo1v3n-ZRBCw">YT Channel</a>)<br>
        Humbled Trader is a Youtube personality that streams on a regular basis. Her trade videos are quirky and educational. <br><br>
        <strong>Warrior Trading</strong> (<a href="https://www.youtube.com/channel/UCBayuhgYpKNbhJxfExYkPfA">YT Channel</a>)<br>
        Cameron live-streams on a regular basis and runs his own learning platform. His streams cover his specialized strategy of scalping momentum trades every morning, of which the success of such can be seen throughout.
        <br><br>

        Investors, Finance Specialists<br>
        <hr class="my-1">
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

        World Figures<br>
        <hr class="my-1">
        <strong>President Biden</strong> <br>
        POTUS. <br><br>
        <strong>Jerome Powell</strong> <br>
        Chairman of the Federal Reserve. <br>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-4" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
         Trading, General News:<br>
        <hr class="my-1">
        <a href="https://marketwatch.com" target="_blank">Marketwatch</a>, <a href="https://finance.yahoo.com" target="_blank">Yahoo! Finance</a>, <a href="https://seekingalpha.com" target="_blank">Seeking Alpha</a>, <a href="https://fool.com" target="_blank">Motley Fool</a>, r/WallStreetBets <br>
        <br>
        Coding, Design:<br>
        <hr class="my-1">
         <a href="https://www.youtube.com/watch?v=2P-yW7LQr08&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp">MIT OpenCourseWare</a>, 
        Dynamic Programming, <a href="https://leetcode.com" target="_blank">LeetCode</a>, <a href="https://freecodecamp.com" target="_blank">FreeCodeCamp</a>, <a href="https://geeksforgeeks.org" target="_blank">GeeksForGeeks</a>, 
        Dribbble, Dubberly Design Presentations,
        <a href="https://www.designboom.com/" target="_blank">Designboom</a>
        
        <br><br>
        World News, Gaming:<br>
        <hr class="my-1">
        <a href="https://www.youtube.com/user/NewsyHub" target="_blank">Newsy</a>,
        <a href="https://www.bbc.com/" target="_blank">BBC</a>,
        <a href="https://www.youtube.com/channel/UCZaT_X_mc0BI-djXOlfhqWQ" target="_blank">Vice</a>,
        <a href="https://www.polygon.com/" target="_blank">Polygon</a>,
        <a href="https://www.theverge.com/" target="_blank">The Verge</a>,
        <a href="https://www.polygon.com/" target="_blank">Polygon</a>
        <br><br>

        Other:<br>
        <hr class="my-1">
        LDS Church, <a href="http://www.wingchun-sf.com/oakland.html">East-West Wing Chun</a><br><br>
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
