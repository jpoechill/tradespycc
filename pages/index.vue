<template>
  <div>
   <div class="container mt-4">
     <div class="row">
       <div class="col-md-12">


<div class="accordion" id="accordionExample">
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingOne">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
        ACCOUNT 5 – AGGRO 1, THINK OR SWIM ($200,000/200,000, 1 RESETS)
      </button>
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        Hyper Volatile. Stock and Options. No limit on # of trades.<br><br>
          Feed: <br>
          April 30, '21. $200k => $230k => $60k. SPY puts and then calls. Maybe also MVIS (not SPY!). Getting ready for reset 2. <br>
          Jan. '21. $100k to $800k going all-in on PLUG (not SPY!) calls. Reset account after admitting it was a total fluke.
          <br><br>
          No. of resets: 1 <br><br>
          Goals: <br>
          • With strategic effort, aggressively beat the average yearly returns for SPY of +13.25%/year.<br>
          • How many times can I blow an account?<br><br>
          Notes: <br>
          • 2x Think or Swim paper trading account, starting with $100,000 each. <br>
          • This is the aggressive, free range account, of which I could plan to eventually "master" at any conceivable level. What I can hope to do here is leverage the different capabilities open to me and use them as an advantage for when the market can move as anyone could expect.<!-- <br><br> -->
        <!-- I can expect this account to have to be restarted and reset multiple times. -->
         <br>
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingThree">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
        ACCOUNT 3 – MODERATE 1 (${{ numberWithCommas((spyCurr * 180) + 24652.00, ) }}/$100,000, 0 RESETS)
      </button>
    </h2>
    <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionExample">
      <div class="accordion-body">
         Full stocks, along with 3x leverage ETFs where inclined. 3-5 trades/month.<br><br>
         Buy 180 shares SPY at $418.60, on 042921. <br><br>
         Holdings: <br>
         180 Shares $418.60 ($75,348). <br><br>
         Cash: $24,652.00 <br><br>
         No. of resets: 0 <br><br>
         Status: <br>
         Invested 3/4 of capital. Waiting for SPY to drop to pick up rest.<br><br>
         Goals: <br>
         With moderate effort, comfortably beat the average yearly returns for SPY of +13.25%/year.<br><br>
         Notes: <br>
         This is a moderately risk account. While I am not limited to any number of trade throughout the day/week/year, I am still only trading SPY. In this account, I am hoping to take advantage of market momentum, in case by being in the market when its hot, and being out of it when its not. Access to SPY leverage (3x inverse/bull) where I can feel necessary.
         <br>
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingFour">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
        ACCOUNT 4 – SAFE 1 (${{ numberWithCommas((spyCurr * 238) + 373.20).slice(0) }}/$100,000)
      </button>
    </h2>
    <div id="collapseFour" class="accordion-collapse collapse" aria-labelledby="headingFour" data-bs-parent="#accordionExample">
      <div class="accordion-body">
         Full stocks. Hyper conservative. Control group. Avg. trades: 3-5/year, max.<br><br>
         Buy 238 shares SPY at $418.60, on 042921. <br><br>
         Holdings: <br>
         233 Shares @ $418.60 ($99,626.80) Cash: $373.20 <br>
         No. of resets: NA <br><br>
         Goals: <br>
         With minimal effort, comfortably mirror the average yearly returns for SPY of +13.25%/year.<br><br>
         Status: <br>
         Holding with no plans to sell.<br><br>
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
