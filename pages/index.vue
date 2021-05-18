<template>
  <div>
    <div class="container mt-4 mb-4">
     <div class="row">
       <div class="col-md-12">
        Portfolio action and balances. <br><br>
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('aggro')">Aggressive</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('moderate')">Moderate</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" href="#" @click="navigate('safe')">Safe</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-3" v-show="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
         <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                ACCOUNT 1 – AGGRO 1, THINK OR SWIM (Starting: $200,000)
              </button>
            </h2>
            <div id="collapseOne" class="accordion-collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Hyper Volatile. Options only. No limit on # of trades.<br><br>
                  Feed<br>
                  <hr class="my-1">May 17th, '21. Volitility and overtrading.  <span class="badge bg-warning">Reset</span><br>
                  <ul class="mt-2">
                    <li>Held on to calls over the weekend, and returned to a morning market dip. <span class="badge badge-info">Surprise!</span> [<a href="https://www.marketwatch.com/story/dow-poised-to-start-week-under-pressure-11621251248?mod=home-page">Reference via. @marketwatch</a>] </li>
                    <li><mark>With minor gains leading to overall loss, the bigger mishap today was simply overtrading. Hindsight, the only way to have won would have been to take a short (~10-20 min) scalp and then being wholly done there.</mark> <span class="badge bg-primary">Learnings</span></li>
                    <li>One account blown. Other with significant losses, though still salvageable. 40k => 10k; 100k => 60k.</li>
                  </ul>
                  May 14th, '21. Picked up late morning calls, matching flow of market. <span class="badge bg-success">Gain</span><br>
                  <ul class="mt-2">
                    <li>Inclined for a moment to buy puts just to go against the market, but decided it needless. [<a href="https://tradespy.tumblr.com/post/651217360539320320/following-the-trend-gains-on-calls-36k-48k">Reference</a>] </li>
                    <li>Overall, the decision today was a simple one, and proved profitable.</li>
                    <li><mark>Getting somewhat easier to feel what SPY might do, and controlling reactions to unpredicticality of what is/has actually happened.</mark> <span class="badge bg-primary">Learnings</span></li>
                    <li><mark>Also getting better (less anxious), and more confident about making day trades, and then sitting through the decision afterwards.</mark> <span class="badge bg-primary">Learnings</span></li>
                    <li>Question now: SPY is lower than ATH, how soon will it return, and will it break out again? Forecast for the coming week?</li>
                  </ul>
                  May 13th, '21. Took loss betting on continued puts before being stomped out. <span class="badge bg-danger">Loss</span><br>
                  <ul class="mt-2">
                    <li>Market making a quick comeback from 2-day down trend. <span class="badge badge-info">Surprise!</span></li>
                    <li>Tech, QQQ still weaker.</li>
                  </ul>

                  <div class="container-view-more d-block overflow-hidden" ref="showMoreContainer" :style="{ height: showMoreHeightDynammic + 'px' }" v-show="showViewMore">
                    
                    May 12th, '21. Up-hits on puts, less on calls. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset x2</span><br>
                    <ul class="mt-2">
                      <li>Holds on puts for the day put me over the top @ 432K => 500k+. [<a href="https://tradespy.tumblr.com/post/651003398878052352/432k-501k-120k-48k-currently">Reference</a>]</li>
                      <li>Holds on calls put me below 50% in auxiliary account @ 120k => 48k. Resetting both.</li>
                      <li><mark>Going forward, rather than purposefully trying to bomb an account as I did with previous calls, I can plan to strategically play both accounts. The effort might be more excruciating and challenging, but I would think from it – I could gain more experience.</mark> <span class="badge bg-primary">Learnings</span></li>
                    </ul>
                    May 11th, '21. Major gains on "yolo'd" puts, and less some on reversal calls. <span class="badge bg-success">Gain</span><br>
                    <ul class="mt-2">
                      <li>Puts from previous day extended into this morning, bringing account to 500k+ at one point. Because I hadn't planned on getting this far this soon, I am currently sitting at 432k. Will consider this now as worthy to reset, with the drawback that I failed to <i>pull-out</i> at peak.</li>
                      <li>Secondary account is still considerably over start, but now struggling to find the proper direction; momentum. [<a href="https://tradespy.tumblr.com/post/650903506198331392/account-1-115k-145k-on-late-morning-calls">Reference</a>]</li>
                      <li><mark>Trading in and out of the day takes more effort than taking striking a longer position and sitting. From current history, trading in and out also shows evidence of bringing less returns.</mark> <span class="badge bg-primary">Learnings</span></li>
                    </ul>
                    May 10th, '21. Extending plays. <span class="badge badge-info">Hold</span> <span class="badge badge-light">Anxious!</span> <br>
                    <ul class="mt-2">
                      <li>Pushing sized calls and "yolo" puts on designated accounts. There shouldn't be much more to the top, right..? </li>
                    </ul>
                    May 7th, '21. Gains on following through with calls; loss on puts. <span class="badge bg-success">Gain</span> <span class="badge bg-danger">Loss</span> <span class="badge bg-warning">Reset</span><br>
                    <ul class="mt-2">
                      <li>Account 1A: 100k => 175k. Account 1B: 100k => 20k.</li>
                      <li>Stuck with near OTM calls to make some small gains on first account. <a href="https://tradespy.tumblr.com/image/650455008880607232" target="_blank">[Reference]</a> </li>
                      <li>Was expecting serious continuation of downward trend, but the otherwise became apparent for the second account. <span class="badge badge-info">Surprise!</span></li>
                      <li><mark>Found out its a bit hard to actually forcefully take an account to 0, without having calls expire to worthless.</mark> <span class="badge bg-primary">Learnings</span></li>
                      <li>Resetting 1B account 20k due to low balance. May think about resetting 1A account if it reaches 200k.</li>
                    </ul>
                    May 6th, '21. Gains on SPY puts, etc others. <span class="badge bg-success">Gain</span><br>
                    <ul class="mt-2">
                      <li>Considerable gains on early morning puts before being stomped out. <a href="https://tradespy.tumblr.com/image/650455008880607232" target="_blank">[Reference]</a> </li>
                      <li>Wasn't expecting the sharp reversal aftwards, which opened opportunity for which I was not prepared.</li>
                      <li>Unfortunately, above trades are specified non-SPY – deviating from primary mission. Eek.</li>
                      <li><mark>Trading SPY takes true patience when going both ways, in case: downwards and upwards movement.</mark> <span class="badge bg-primary">Learnings</span></li>
                      <li>Currently, sitting with <i>no positions</i>.</li>
                    </ul>
                    May 5th, '21. Account blown. Reset 2. <span class="badge bg-warning">Reset x2</span><br>
                    <ul class="mt-2">
                      <li>Blown by messing around with &#60;3 DTE calls and puts.  <a href="https://tradespy.tumblr.com/image/650365708821299200" target="_blank">[Reference]</a> </li>
                      <li>Reset one account with 100k of 2 DTE SPY calls, and the other with 100k 2 DTE SPY puts. Pure coin flip. Holding till Friday. <a href="https://tradespy.tumblr.com/image/650371363175006208" target="_blank">[Reference]</a></li>
                      <li>&#60;3 DTE are basically shots in the dark. Might try again a few more rounds. <span class="badge bg-primary">Learnings</span></li>
                      <li><mark><i>"Paper handing"</i> and not following through on a plan seems worse than just sticking to one.</mark> <span class="badge bg-primary">Learnings</span></li>
                    </ul>
                    April 30, '21. Substantial gain to overall lost. <span class="badge bg-danger">Loss</span><br>
                    <ul class="mt-2">
                      <li>Getting ready for reset 2. [<a href="https://tradespy.tumblr.com/post/650195604078788608/200k-235k-59k-time-period-1-week" target="_blank">Reference</a>] </li>
                      <li>$200k => $230k => $60k. SPY puts and then calls. </li>
                      <li>Maybe also MVIS (not SPY!) puts.</li>
                      <li>&#60;3 DTE's</li>
                    </ul>
                    Jan. '21. Major gain. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset</span><br>
                    <ul class="mt-2">
                      <li>$100k to $800k going all-in on PLUG (not SPY!) calls. </li>
                      <li>Reset account after admitting total fluke.</li>
                    </ul>
                  </div>

                  <div class="position-relative">
                    <img src="wht_fade.svg" class="w-100 position-absolute wht-fade" alt="" style="bottom: 0;" :style="{ opacity: showViewMore ? 100 : 0 }">
                  </div>
                  <button type="button" @click="toggleViewMore()" class="btn btn-primary btn-lg btn-block">View more...</button>

                  <br>

                  No. of resets: 6 <br><br>
                  Sitting Strategy<br>
                  <hr class="my-1">
                  <ul>
                    <li>Riding the wave. Currently strategy is a pure <i><u>paper-trading</u></i> strategy which involves making a short future prediction, and then buying (or <i>yolo'ing</i>) along such path. Where the prediction proves wrong (with SPY turns against prediction), this strategy will part with either all near ending puts/calls and go to follow the current momentum. </li>
                    <li>The most difficult part of strategy will be days where direction is weak, and there is none to do but guess in which way securities will go. <del>In case, we will have the option to split accounts to track both downwards && upwards movements, or choose to take both into a single direction.</del> Overall and in such case, we will utilize <mark><i>pure and simple guess work</i></mark>. 🤔</li>
                    <li>Yolo'ed options not held for more than 2-3 days at most, before making decision to reset. Room for refinement. </li>
                  </ul>
                  Goals<br>
                  <hr class="my-1">
                  <ul>
                    <li>With strategic effort, aggressively beat the average yearly returns for SPY of +13.25%/year.</li>
                    <li>With strategic effort, double (2x) or more the original value of one account.</li>
                    <li>Process: Trade => Reset => Refine.</li>
                  </ul>
                  Notes<br>
                  <hr class="my-1">
                  <ul>
                    <li>This is the aggressive, free range account, of which I could plan to eventually "master" at any conceivable level. <del>What I can hope to do here is leverage the different capabilities open to me and use them as an advantage for when the market can move as anyone could expect.</del> The main instrument being options.</li>
                    <li>2x Think or Swim paper trading account, starting with $100,000 each.</li>
                    <li>To-do: normalize a SPY strategy for consistent upside.</li>
                    <li><del>Also, and currently: How many times can I blow an account?</del></li>
                  </ul>
              </div>
            </div>
          </div>
          
        </div>
       </div>
     </div>
   </div>

   <div class="container mt-4 mb-3" v-show="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12">
        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                ACCOUNT 2 – MODERATE 1 (${{ numberWithCommas(((spyCurr * 238) + 221.82).toFixed(2), ) }}/$100,000, 0 RESETS)
              </button>
            </h2>
            <div id="collapseThree" class="accordion-collapse show" aria-labelledby="headingThree" data-parent="#accordionExample">
              <div class="accordion-body">
                Full stocks, along with 3x leverage ETFs where inclined. 3-5 trades/month.<br><br>
                Feed<br>
                <hr class="my-1">
                May 11th, '21. Foward action plan.
                <ul>
                  <li>Planning to sell when SPY price breaks below 50 day, 3-month SMA. [<a href="https://www.barchart.com/etfs-funds/quotes/SPY/technical-chart?plot=CANDLE&volume=total&data=DO&density=ML&pricesOn=1&asPctChange=0&logscale=0&indicators=SMA(50)&sym=SPY&grid=1&height=500&studyheight=100">Reference</a>] </li>
                </ul>
                May 10th, '21. Buy stocks.
                <ul>
                  <li>Eliminating cash positions, and going full stocks. Making to further align with 50/200 day SMA strategy.</li>
                  <li>Buy 58 Shares @ $421.21.</li>
                </ul>
                May 5th, '21. Waiting, watching. <span class="badge bg-info">Hold</span>
                <ul>
                  <li>SPY still high. Looking for better pseudo-entry.</li>
                </ul>
                April 29th, '21. Establish position. 
                <ul>
                  <li>Buy 180 shares SPY at $418.60.</li>
                </ul>
                Holdings: <br>
                <ul>
                  <li>AVG: 238 Shares @ $419.24.</li>
                  <li>58 Shares @ $421.21 ($24,430.18). </li>
                  <li>180 Shares @ $418.60 ($75,348.00). </li>
                </ul>
                Cash: $221.82 <br><br>
                No. of resets: 0 <br><br>
                Strategy<br>
                <hr class="my-1">
                <ul>
                  <li>Utilize an ad-hoc 50/200 day SMA strategy. In when over SMA, out when under. [<a href="/strategies">See Strategies</a>]</li>
                </ul>
                Goals<br>
                <hr class="my-1">
                <ul>
                  <li>With moderate effort, comfortably beat the average yearly returns for SPY of +13.25%/year.</li>
                </ul>
                Notes<br>
                <hr class="my-1">
                <ul>
                  <li>This is a moderately risk account. While I am not limited to any number of trade throughout the day/week/year, I am still only trading SPY. </li>
                  <li>I am hoping to take advantage of market momentum, in case by being in the market when its hot, and being out of it when its not.</li>
                  <li>Access to SPY leverage (3x inverse/bull) where I can feel necessary.</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
       </div>
     </div>
   </div>


   <div class="container mt-4 mb-3" v-show="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingFour">
              <button class="accordion-button collapse show" type="button" data-toggle="collapse" data-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                ACCOUNT 3 – SAFE 1 (${{ numberWithCommas(((spyCurr * 238) + 373.20).toFixed(2)) }}/$100,000)
              </button>
            </h2>
            <div id="collapseFour" class="accordion-collapse show" aria-labelledby="headingFour" data-parent="#accordionExample">
              <div class="accordion-body">
                Full stocks. Hyper conservative. Control group. Avg. trades: 3-5/year, max.<br><br>
                Feed<br>
                <hr class="my-1">
                <ul>
                  <li>Buy 238 shares SPY at $418.60, on 042921. <span class="badge bg-info">Hold</span></li>
                </ul>
                Holdings: <br>
                <ul>
                  <li>233 Shares @ $418.60 ($99,626.80) Cash: $373.20 </li>
                </ul>
                No. of resets: NA <br><br>
                Goals<br>
                <hr class="my-1">
                <ul>
                  <li>With minimal effort, comfortably mirror the average yearly returns for SPY of +13.25%/year.</li>
                </ul>
                Status<br>
                <hr class="my-1">
                <ul>
                  <li>Holding with no immediate plans to sell.</li>
                </ul>
                Notes<br>
                <hr class="my-1">
                <ul>
                  <li>This is the control group used as a reference point for other accounts that may be tolerable of more risk.</li>
                  <li> The only instances I would hope to make a trade in this account is during cases of imminent disaster, and world catastrophe. </li>
                  <li>In being a long-term buy and hold account, I will hope to see about starting different accounts of the same type throughout unspecified times in the year.</li>
                </ul>
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
    setShowMoreHeight: function () {
      this.showMoreHeightStatic = this.$refs.showMoreContainer.clientHeight
    },
    toggleViewMore: function () {
      if (this.showViewMore === false) {
        this.showMoreHeightDynammic = 0
      } else {
        this.showMoreHeightDynammic = this.showMoreHeightStatic
      }

      this.showViewMore = !this.showViewMore
    },
    numberWithCommas: function (x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    },
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
  },
  data () {
    return {
      showMoreHeightStatic: 0,
      showMoreHeightDynammic: null,
      showViewMore: true, 
      tabs: [
        {
          name: 'aggro',
          isActive: true
        },
        {
          name: 'moderate',
          isActive: false
        },
        {
          name: 'safe',
          isActive: false
        }
      ],
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

    this.showMoreHeightStatic = this.$refs.showMoreContainer.clientHeight
    this.showMoreHeightDynammic = 0

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
.view-more:hover {
  cursor: pointer;
}

.container-view-more, .wht-fade  {
  transition: all .5s ease-in-out;
}

img {
  pointer-events: none
}

mark {
  margin-left: -4px;
}
</style>
