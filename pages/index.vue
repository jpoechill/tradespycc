<template>
  <div>
   <div class="container mt-4">
     <div class="row">
       <div class="col-md-12">


<div class="accordion" id="accordionExample">
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingOne">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
        ACCOUNT 1 – AGGRO 1, THINK OR SWIM (Starting: $200,000, 2 RESETS)
      </button>
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        Hyper Volatile. Stock and Options. No limit on # of trades.<br><br>
          Feed: <br>
          May 5th, '21. Account blown. Reset 2. <span class="badge bg-warning">Reset</span><br>
          <ul class="mt-2">
            <li>Blown by messing around with &#60;3 DTE calls and puts.  <a href="https://tradespy.tumblr.com/post/650365708821299200/2-dte-calls-and-puts-account-blown-resetting">[Reference]</a> </li>
            <li>Reset to 100k 2 DTE SPY calls, and 100k 2 DTE SPY puts. Coin flip. Holding till Friday.</li>
            <li>&#60;3 DTE are basically shots in the dark. Might try again a few more rounds. <span class="badge bg-primary">Learnings</span></li>
            <li><i>"Paper handing"</i> and not following through on a plan seems worse than sticking to one. <span class="badge bg-primary">Learning</span></li>
          </ul>
          April 30, '21. Substantial gain to overall lost. <br>
          <ul class="mt-2">
            <li>Getting ready for reset 2. [<a href="https://tradespy.tumblr.com/post/650195604078788608/200k-235k-59k-time-period-1-week" target="_blank">Reference</a>] </li>
            <li>$200k => $230k => $60k. SPY puts and then calls. </li>
            <li>Maybe also MVIS (not SPY!) puts.</li>
            <li>&#60;3 DTE's</li>
          </ul>
          Jan. '21. Major gain. <span class="badge bg-success">Win</span> <span class="badge bg-warning">Reset</span><br>
          <ul class="mt-2">
            <li>$100k to $800k going all-in on PLUG (not SPY!) calls. </li>
            <li>Reset account after admitting total fluke.</li>
          </ul>
          No. of resets: 2 <br><br>
          Goals: <br>
          <ul>
            <li>With strategic effort, aggressively beat the average yearly returns for SPY of +13.25%/year.</li>
            <li>Also: how many times can I blow an account?</li>
          </ul>
          Notes: <br>
          <ul>
            <li>This is the aggressive, free range account, of which I could plan to eventually "master" at any conceivable level. What I can hope to do here is leverage the different capabilities open to me and use them as an advantage for when the market can move as anyone could expect.</li>
            <li>2x Think or Swim paper trading account, starting with $100,000 each.</li>
          </ul>
         <br>
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingThree">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
        ACCOUNT 2 – MODERATE 1 (${{ numberWithCommas((spyCurr * 180) + 24652.00, ) }}/$100,000, 0 RESETS)
      </button>
    </h2>
    <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionExample">
      <div class="accordion-body">
         Full stocks, along with 3x leverage ETFs where inclined. 3-5 trades/month.<br><br>
         Feed: <br>
         May 5th, '21. Waiting, watching.
         <ul>
           <li>SPY still high. Looking for better pseudo-entry.</li>
         </ul>
         April 29th, '21. Establish position. 
         <ul>
           <li>Buy 180 shares SPY at $418.60.</li>
         </ul>
         Holdings: <br>
         180 Shares $418.60 ($75,348). <br><br>
         Cash: $24,652.00 <br><br>
         No. of resets: 0 <br><br>
         Goals: <br>
         With moderate effort, comfortably beat the average yearly returns for SPY of +13.25%/year. TEST<br><br>
         Notes: <br>
         This is a moderately risk account. While I am not limited to any number of trade throughout the day/week/year, I am still only trading SPY. In this account, I am hoping to take advantage of market momentum, in case by being in the market when its hot, and being out of it when its not. Access to SPY leverage (3x inverse/bull) where I can feel necessary.
         <br>
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingFour">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
        ACCOUNT 3 – SAFE 1 (${{ numberWithCommas((spyCurr * 238) + 373.20).slice(0) }}/$100,000)
      </button>
    </h2>
    <div id="collapseFour" class="accordion-collapse collapse" aria-labelledby="headingFour" data-bs-parent="#accordionExample">
      <div class="accordion-body">
         Full stocks. Hyper conservative. Control group. Avg. trades: 3-5/year, max.<br><br>
        Feed: <br>
        Buy 238 shares SPY at $418.60, on 042921. <br><br>
         Holdings: <br>
         233 Shares @ $418.60 ($99,626.80) Cash: $373.20 <br><br>
         No. of resets: NA <br><br>
         Goals: <br>
         With minimal effort, comfortably mirror the average yearly returns for SPY of +13.25%/year.<br><br>
         Status: <br>
         Holding with no immediate plans to sell.<br><br>
         Notes: <br>
         This is the control group used as a reference point for other accounts that may be tolerable of more risk. The only instances I would hope to make a trade in this account is during cases of imminent disaster, and world catastrophe. In being a long-term buy and hold account, I will hope to see about starting different accounts of the same type throughout unspecified times in the year.
         <br>
      </div>
    </div>
  </div>
</div>

       </div>
     </div>
   </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  methods: {
    numberWithCommas: function (x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    }
  },
  data () {
    return {
      spyCurr: 0,
      accounts: [
        {
          name: 'account 1',

        }
      ]
    }
  },
  mounted () {
    let self = this

    axios.get('https://cloud.iexapis.com/stable/stock/' + 'SPY' + '/quote?token=pk_d8826aae332a4b1287b1d4399e2f860b')
        .then(function (response) { 
            self.spyCurr = response.data.iexRealtimePrice
          })
        .catch(function (error) {
          console.log(error);
        })
  }
}
</script>

<style>
</style>
