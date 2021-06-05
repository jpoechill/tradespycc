<template>
  <div>

   <div class="container mt-0 mb-2">
     <div class="row">
       <div class="col-md-12">
        <!-- Market observations, news, and website updates. <br><br> -->
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[1].isActive }" href="#" @click="navigate('balances')">Paper Trading</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[3].isActive }" href="#" @click="navigate('strats')">Strategies</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[2].isActive }" aria-current="page" href="#" @click="navigate('charts')">Charts</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[0].isActive }" aria-current="page" href="#" @click="navigate('marketObs')">Market</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[4].isActive }" href="#" @click="navigate('resources')">Resources</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[5].isActive }" href="#" @click="navigate('updates')">Updates</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" :class="{ active: tabs[6].isActive }" href="#" @click="navigate('about')">About</a>
          </li>
        </ul>
       </div>
     </div>
   </div>

   <div class="container mt-0 mb-2" v-if="tabs[0].isActive">
     <div class="row">
       <div class="col-md-12">
          <div class="accordion mb-2" id="accordionExample">
            <div class="accordion-item">
              <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="true" aria-controls="collapseTwo">
                  MARKET OBSERVATIONS 1 – MONTH OF MAY 2021
                </button>
              </h2>
              <div id="collapseTwo" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
                <div class="accordion-body">
                  Jun 2nd, 2021.
                  <ul>
                    <li>Morning rise to afternoon fall. Holding at ~420.</li>
                  </ul>
                  Jun 1st, 2021.
                  <ul>
                    <li>Opened ATH from a long weekend, and carried lower to close. Oscillating still +-420.</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>

        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                MARKET OBSERVATIONS 1 – MONTH OF MAY 2021
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Month's summary: <br>
                While trading at near ATH's, SPY and other equities tooks a hit earlier in the month due to concerns about inflation but was able to bounce back. Currently the lines have been holding long enough that there is expected to be a near-soon strong GAP upwards, or downwards. Short interest has also been especially building.<br><br>
                May 28th, 2021.
                <ul>
                  <li>SPY rocky, but breaking even. Long weekend ahead.</li>
                </ul>
                May 27th, 2021.
                <ul>
                  <li>SPY still inching along. Ready a break out, or even a dip. Somethings brewing, though. [<a href="https://www.marketwatch.com/story/as-the-s-p-500-approaches-its-all-time-high-brace-for-a-violent-move-01622125439?mod=home-page">Reference via. @marketwatch</a>]</li>
                </ul>
                May 26th, 2021.
                <ul>
                  <li>SPY inches along. Personally looking for the day it corrects to go <i>hard</i> on puts... Yikes.</li>
                  <li>SPY short interest, higher than ever its been YTD. [<a href="https://www.bloomberg.com/news/articles/2021-05-25/bets-against-357-billion-s-p-500-etf-jump-to-highest-this-year">Reference via. @bloomberg</a>] </li>
                </ul>

                <div class="container-view-more d-block overflow-hidden" ref="showMoreContainer" :style="{ height: showMoreHeightDynammic + 'px' }" v-show="showViewMore">
                
                  May 25th, 2021.
                  <ul>
                    <li>Some continued downard momentum. Do we hold here, or no?</li>
                  </ul>
                  May 24th, 2021.
                  <ul>
                    <li>Early rise; afternoon high to closing draw down. <span class="badge bg-success">Reversal</span> [<a href="https://finance.yahoo.com/news/stock-market-news-live-updates-may-24-2021-112518586.html">Reference via. @yahooFinance</a>, <a href="https://www.bloomberg.com/news/articles/2021-05-24/asian-stocks-set-to-climb-as-dollar-yields-drop-markets-wrap">Reference via. @bloomberg</a>] </li>
                    <li>Positive day. Things might be looking bright this week?</li>
                  </ul>
                  May 21st, 2021.
                  <ul>
                    <li>Shaky downward day. Concerns re: inflation. <span class="badge bg-danger">Reversal</span> [<a href="https://finance.yahoo.com/news/stock-market-news-live-updates-may-21-2021-221344440.html">Reference via. @yahooFinance</a>] </li>
                    <li>More sharp declines than rises. Where do we go from here?</li>
                  </ul>
                  May 20th, 2021.
                  <ul>
                    <li>Equities opening higher due to peak low jobless claims. <span class="badge bg-success">Reversal</span> [<a href="https://finance.yahoo.com/news/stock-market-news-live-updates-may-20-2021-221318405.html">Reference via. @yahooFinance</a>] </li>
                    <li>SPY still trading below ATH; overall positive sentiments.</li>
                    <li>Tech continuing to make gains.</li>
                  </ul>
                  May 19th, 2021.
                  <ul>
                    <li>Opened down, with a shaky end-of-day rise. Overall cultprit: inflation. [<a href="https://www.marketwatch.com/story/dow-futures-drop-250-points-and-tech-stocks-slump-anew-ahead-of-fed-minutes-11621423385?mod=home-page">Reference via. @marketwatch</a>] </li>
                    <li>Opportunity for SPY to close below opening, leaving questions that this down trend may continue.</li>
                    <li>Possibly more "fits and starts" of a return to back to growth. [<a href="https://finance.yahoo.com/news/stock-market-news-live-updates-may-19-2021-221605666.html">Reference via. yahooFinance</a>]</li>
                  </ul>
                  May 18th, 2021.
                  <ul>
                    <li>Volitility with company earnings and general market draw-down. <span class="badge bg-danger">Reversal</span> [<a href="https://www.marketwatch.com/story/dow-futures-rise-as-home-depot-reports-unprecedented-quarterly-demand-11621337117?mod=home-page">Reference via. @marketwatch</a>] </li>
                    <li>Tech making comebacks. Does this get worse before it gets better?</li>
                  </ul>
                  May 17th, 2021.
                  <ul>
                    <li>Morning draw-down with afternoon rise. [<a href="https://www.marketwatch.com/story/dow-poised-to-start-week-under-pressure-11621251248?mod=home-page">Reference via. @marketwatch</a>] </li>
                    <li>Tricky place to be in seeing that current level is perfectly in between recent lows and highs.</li>
                  </ul>
                  May 14th, 2021.
                  <ul>
                    <li>Continued SPY gains. [<a href="https://seekingalpha.com/news/3696789-sp-500s-weekly-market-breakdown-and-sector-performance">Reference via. @seekingalpha</a>] </li>
                    <li>Questions: Have growth stocks been primed for a return? Or is it still too early?</li>
                  </ul>
                  May 13th, 2021.
                  <ul>
                    <li>Comeback. <span class="badge bg-success">Reversal</span></li>
                  </ul>
                  May 12th, 2021.
                  <ul>
                    <li>Continued down trend. All stocks and equities. Cause: fear of inflation. [<a href="https://finance.yahoo.com/news/stock-market-news-live-updates-may-12-2021-221905341.html">Reference via. @yahoo.com</a>]</li>
                    <li>The fall is here. To re-iterate from earlier: how long does this last, and how far will it go? Questions. </li>
                  </ul>
                  May 11th, 2021. 
                  <ul>
                    <li>SPY takes another hit. The question now: how long does this last, and how far will it go? <span class="badge bg-danger">Reversal</span></li>
                  </ul>
                  May 10th, 2021. 
                  <ul>
                    <li>SPY momentum slowing down. QQQ (tech, growth) taking a hit. Crypto flaky. [<a href="https://www.investing.com/analysis/trading-the-sp-500s-latest-wobble-what-the-faang-stocks-are-telling-us-200579135">Reference via. investing.com</a>]</li>
                  </ul>
                  May 7th, 2021. 
                  <ul>
                    <li>SPY breaking new highs. Really stumped; surprised. Just wow.</li>
                    <li>Further dip sentiment, with traders taking long on SPY puts. [<a href="https://www.benzinga.com/etfs/broad-u-s-equity-etfs/21/05/21017410/options-trader-makes-3-78m-bet-the-top-is-nearby-for-spy">Reference via. @benzinga</a>]</li>
                  </ul>
                  May 5th, 2021. 
                  <ul>
                    <li>Crypto taking off, QQQ and tech taking more dips. SPY holding... for now.</li>
                  </ul>
                  May 4th, 2021. 
                  <ul>
                    <li>Nice hit on SPY and QQQ today. Market keeps hitting new highs, but how long will it last? [<a href="https://www.fool.com/investing/2021/05/04/why-zoom-video-fastly-and-square-stocks-all-fell-s/">Commentary via. @fool</a>]</li>
                  </ul>
                  May 2nd, 2021. 
                  <ul>
                    <li>Are we at the top..?</li>
                  </ul>
                </div>

                <div class="position-relative">
                  <img src="wht_fade.svg" class="w-100 position-absolute wht-fade" alt="" style="bottom: 0;" :style="{ opacity: showViewMore ? 100 : 0 }">
                </div>
                <button type="button" @click="toggleViewMore()" class="btn btn-primary btn-lg btn-block">View more...</button>
            
              </div>
            </div>
          </div>
        </div>
       </div>
     </div>
   </div>



   <div class="container mt-2 mb-2" v-if="tabs[1].isActive">
     <div class="row">
       <div class="col-md-12 ">
          
        <!-- <div class="accordion mb-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingFour">
              <button class="accordion-button collapse show" type="button" data-toggle="collapse" data-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                ACCOUNT 4 – AGRRO 2, EXPERIMENTAL 1
              </button>
            </h2>
            <div id="collapseFour" class="collapse" aria-labelledby="headingFour" data-parent="#accordionExample">
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
        </div> -->


         <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                ACCOUNT 3 – AGGRO 1, THINK OR SWIM (RETIRED)
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Hyper Volatile. Options only. No limit on # of trades.<br><br>
                  Feed<br>
                  <hr class="my-1">
                    
                  May 28th, '21. Gain day. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset x2</span>
                  <ul class="mt-2">
                    <li>Took advantage of ending options to double up in a brief trading session. Ended day early.</li>
                    <li>Reset to 1k, 500 account size.</li>
                    <li>Day's summary:  72.6 => 157k. 12m => 14.6m (yikes, AMC... again!).</li>
                    <li>Trade time: ~1.5hrs.</li>
                  </ul>
                  May 27th, '21. Slow day, but was able to catch some good dips. <span class="badge bg-success">Gain</span> [<a href="https://tradespy.tumblr.com/post/652356585986916352/30k-72k-10m-10m-no-change-trade-time">Reference</a>]
                  <ul class="mt-2">
                    <li>Overall slow day, but was still able to catch some falls (2x) that put me over the top. Finished the day early.</li>
                    <li>More investigations, prep for strategy transition to live trading.</li>
                    <li>Day's summary:  30k => 72k. 10m => 12m (yikes, traded AMC..!).</li>
                    <li>Approximate # of day-trades (round trips): <20 </li>
                    <li>Trade time: ~2hrs.</li>
                  </ul>


                  <div class="container-view-more d-block overflow-hidden" ref="showMoreContainer" :style="{ height: showMoreHeightDynammic + 'px' }" v-show="showViewMore">
                    
                    May 26th, '21. Probably a million trades, but overall, full gains. <span class="badge bg-success">Gain</span> [<a href="https://tradespy.tumblr.com/post/652307358174887936/15k-30k-10m-10m-no-change-min-optimal">Reference</a>]
                    <ul class="mt-2">
                      <li>SPY ended up barely moving, but with this, was still able to accomplish doubling (2x) today's start. This, through many, many trades...</li>
                      <li>Currently, trying to figure out how to adjust to seriously trading less. Also, more serious investigations into transitions into live trading.</li>
                      <li>Would like to somehow continue to be transparent once the shift is made, but keep <i>light and playfullness</i>, as seen currently.</li>
                      <li>Contemplating working with a new goal, to count # amount of trades/day, and hand tallying each one.</li>
                      <li>Day's summary:  15k => 30k. 10m => 10m.</li>
                      <li>Trade time: ~4hrs.</li>
                    </ul>
                    May 25th, '21. Strategy still working well. Overall substantial gain, with reset of smaller account to 15k. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset</span>
                    <ul class="mt-2">
                      <li>Early downward movement today along with larger bid sizes allowed me considerable gains in larger account.</li>
                      <li>Movement in end of day allowed me to boost smaller account by 50%. In a real-world case, would be limited to PDT, so would actually have to be more careful about picks in entering/exits.</li>
                      <li>Some personal issues still with over trading; in such, losing out on fees/commissions.</li>
                      <li>Rather than setting account goals, would like to see myself set ones that are more time based, ie. trade x style for 1 month and review. Could possibly provide greater detail in the after.</li>
                      <li>Day's summary:  10k => 15k. 4m => 10m (fees/commissions to date: 3.2m).</li>
                      <li>Trade time: ~4hrs.</li>
                    </ul>
                    May 24th, '21. Substantial gain, with minor blunder. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset</span>
                    <ul class="mt-2">
                      <li>Focused on major account today. Experimented with 3 DTE options. Although less risky (as can be seen in gain), I am positive that I saved more in overall fees than OTE's plays. Possibly hoping not to reset account until it reaches 10m, or 100m. Continuing hyper-aggressive approach.</li>
                      <li>Loss that eventually recovered today came from being somewhat disoriented+dissatisfied with price action, which ended up with me trying to chase prices rather than playing the chart. </li>
                      <li><mark>Starting to see consistent winning days with more confidence in being able to turn a profitable day regardless of market direction. Hoping to steady the play, with continuing to deepen knowledge through practice and study.</mark> <span class="badge bg-primary">Learnings</span></li>
                      <li><mark>The chart brings truth. Play the chart. Ignore the numbers.</mark>  <span class="badge bg-primary">Learnings</span></li>
                      <li><mark>Don't burn out. Remember to take breaks where imclined and needed. </mark>  <span class="badge bg-primary">Learnings</span></li>
                      <li>Resetting minor account to 10k. Hoping to record time it take to get to 100k.</li>
                      <li>Day's summary: 3m => 4m (fees/commissions to date: 3.2m).</li>
                      <li>Trade time: ~4hrs.</li>
                    </ul>
                    May 21st, '21. Gains, with recovered blunder. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset</span>
                    <ul class="mt-2">
                      <li>More trade time => more gains. Am content, but really do not want to become over zealous. [<a href="https://tradespy.tumblr.com/post/651641411815571456/more-gains-where-paying-attention-115k-133k">Reference</a>]</li>
                      <li>Reset smaller account to research how fees/commissions are factored into option trades. Would like to try hand at 10k account next.</li>
                      <li><mark>Blunder today was taking a put to the bottom, and then purchasing a call before the last price could settle. Loss about all of the day's gain immediately after purchase. Overall, was able to recover – albeit almost frantically.</mark> <span class="badge bg-primary">Learnings</span></li>
                      <li><mark>Need to work on taking more patience, trading less, and being considerate of overall costs (fees/commission) per trade. More research on history of candle-sticks.</mark> <span class="badge bg-primary">Learnings</span></li>
                      <li>Day's summary: 100k => 150k (fees.commissions: 105k!). 1.23m => 3m (fees/commissions: 1.16m).</li>
                      <li>Trade time: ~4hrs.</li>
                    </ul>
                    May 20th, '21. Gains where paying attention. <span class="badge bg-success">Gain</span> <span class="badge bg-warning">Reset</span>
                    <ul class="mt-2">
                      <li>More solid gains where paying attention. [<a href="https://tradespy.tumblr.com/post/651641411815571456/more-gains-where-paying-attention-115k-133k">Reference</a>]</li>
                      <li>Reset second account to 1m balance; overall it did well. Hoping to try a ~10k balance next.</li>
                      <li><mark>Losses on second account when I tried to trade other securities not SPY... The liquidity and spreads just weren't there. :'( </mark>  <span class="badge bg-primary">Learnings</span></li>
                      <li><mark>Hindsight, while I closed the day for myself before 9am (12noon, eastern), I see now that there would have been plenty of opportunity to make even more gains today due some of the strong movement that happened after. I question now, what would be returns if I dedicate a full day to solely trading and focusing with said strategy. Is there a limit to how much can be made in a day, and what factors would challenge and hold me back from doing this, apart from mental endurance?</mark>  <span class="badge bg-primary">Learnings</span> <span class="badge badge-light">Questions?</span> </li>
                      <li>Day's summary: 133k => 141k. 100k => 120k => 106k. 1m => 1.23m.</li>
                      <li>Trade time: <2hrs.</li>
                    </ul>
                    May 19th, '21. More gains where paying attention.<br>
                    <ul class="mt-2">
                      <li>Got in late today but was still able to catch some action – albeit, small gains. [<a href="https://tradespy.tumblr.com/post/651641411815571456/more-gains-where-paying-attention-115k-133k">Reference</a>]</li>
                      <li>Yesterday's puts failed to close in time, which led them to be carried into <i>major and considerable gains</i> the following day.</li>
                      <li><mark>As seen in wins today. am continuing to better accurately catch market flows. Here, hoping to do more with understanding exactly TA, the candles, and general charting knowledge.</mark> <span class="badge bg-primary">Learnings</span></li>
                      <li>Day's summary: 115k => 133k. 48k => 120k. <span class="badge bg-success">Gain</span> </li>
                    </ul>
                    May 18th, '21. Full gains where I was paying attention.<br>
                    <ul class="mt-2">
                      <li>Even with some of the volitility today, I was able to match a majority of the flows for solid gains – all where I was paying attention.  [<a href="https://tradespy.tumblr.com/post/651555796716519424/100k-116k-65k-48k-gains-where-i-was-paying">Reference</a>]</li>
                      <li>Day's summary: 100k => 115k. 60k => 48k. <span class="badge bg-success">Gain</span> <span class="badge bg-danger">Loss</span> </li>
                      <li><mark>Relying less on fundamentals and moving into an area where I'm purely playing the chart. Much hoping to keep with today's consistency in moving forward. </mark> <span class="badge bg-primary">Learnings</span></li>
                    </ul>
                    May 17th, '21. Volitility and overtrading.  <span class="badge bg-warning">Reset</span><br>
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

                  No. of resets: 11 <br><br>
                  Sitting Strategy<br>
                  <hr class="my-1">
                  <ul>
                    <li>[<nuxt-link to="/strategies">See Strategies</nuxt-link>]</li>
                  </ul>
                  Goals<br>
                  <hr class="my-1">
                  <ul> 
                    <li>Where abled, enhance and perfect descriptions and details of current strategy.</li>
                    <li>Transitions to a SPY/day-trading/options-trading research and experimentation site. </li>
                    <li><del>Be accountable, and consciously aware of fees/commissions, and relative tax burdens.</del></li>
                    <li><del>Carefully, and methodically, prove a successful transition to live-trading.</del></li>
                    <li><del>Process: Trade => Reset => Refine.</del></li>
                    <li><del>With strategic effort, aggressively beat the average yearly returns for SPY of +13.25%/year – on a consistent basis.</del></li>
                    <li><del>With strategic effort, double (2x) or more the original value of one account.</del></li>
                    <li><del>Prove discipline and consistency with positive winning days/week.</del></li>
                    <li><del>Record pecentages of weekly returns. After time, review and assess.</del></li>
                    <li><del>Eventually transition strategy into live trading, without rush. Possibly months (even years?) down the line.</del></li>
                  </ul>
                  Notes<br>
                  <hr class="my-1">
                  <ul>
                    <li>2x ThinkorSwim paper-trading accounts. Reset regulary via. personal discretion. </li>
                    <li><del>This is the aggressive, free range account, of which I could plan to eventually "master" at any conceivable level. What I can hope to do here is leverage the different capabilities open to me and use them as an advantage for when the market can move as anyone could expect. The main instrument being options.</del></li>
                    <li><del>2x Think or Swim paper trading account, starting with $100,000 each.</del></li>
                    <li><del>Would eventually like to experiment with different starting balances – 10k, 50k, 250k, 500k, 1m and etc.</del></li>
                    <li><del>Would like to continue building/optimizing/refining platform in months and years on. Somehow would like to keep it <mark><i>light and playful</i></mark></del>.</li>
                    <!-- <li>Would like to continue paper-trading months and years on – or until completely comfortable with identical, successful plays in live-trading.</li> -->
                    <li><del>To-do: normalize a SPY strategy for consistent upside.</del></li>
                    <li><del>Also, and currently: How many times can I blow an account?</del></li>
                  </ul>
              </div>
            </div>
          </div>
         </div>


          <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                ACCOUNT 2 – MODERATE 1 (${{ numberWithCommas(((spyCurr * 238) + 221.82).toFixed(2), ) }}/$100,000, 0 RESETS)
              </button>
            </h2>
            <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordionExample">
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


        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingFour">
              <button class="accordion-button collapse show" type="button" data-toggle="collapse" data-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                ACCOUNT 1 – SAFE 1 (${{ numberWithCommas(((spyCurr * 238) + 373.20).toFixed(2)) }}/$100,000)
              </button>
            </h2>
            <div id="collapseFour" class="collapse" aria-labelledby="headingFour" data-parent="#accordionExample">
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

   <div class="container mt-0 mb-2" v-if="tabs[2].isActive">
     <div class="row">
       <div class="col-md-12">
        
        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                SPY DAILY
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>

        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                CALLS DAILY
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>


        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                PUTS DAILY
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>

       </div>
     </div>
   </div>

   <div class="container mt-0 mb-2" v-if="tabs[3].isActive">
     <div class="row">
       <div class="col-md-12 py-0">
        
        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                STRAT 1
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>

        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                STRAT 2
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>

       </div>
     </div>
   </div>

   <div class="container mt-0 mb-2" v-if="tabs[4].isActive">
     <div class="row">
       <div class="col-md-12">
        
        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Video
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                <a href="https://www.youtube.com/user/smbcapital">SMB Capital on YT</a>
               </div>
            </div>
          </div>
        </div>

        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Articles
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                <a href="">Mentally and Financially Ready to Flip the Switch? Paper Trading vs. Live Trading Accounts (@TDAmeritrade)</a>, 
                <a href="">Transitioning From Demo to Live Day Trading</a>,
                Technical Analysis, 
                How I Day Trade the SPY,
                Coinbase vs. Robinhood
               </div>
            </div>
          </div>
        </div>

        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Websites
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                <a href="">SPX Option Trader</a>,
                <a href="">Day Trade SPY</a>,
                <a href="">S&P 500 Futures Trading Group</a>
               </div>
            </div>
          </div>
        </div>


        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Books
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Around The World: Day Trading The SPY, Day Trading The SPY; Zero To Hero,
                Day Trade the S&P 500 Index for Fun and Profit: A Unique Method for Using Heikin Ashi Charts to Day Trade...,
                The MEJT System: A New Tool for Day Trading the S&P 500 Index,
                Anatomy of $SPY on First Trading Day of the Month,
                S&P 500 Trading Mastery: A Systematic Trading Plan for Capturing Stock Index Profits,
                $SPY High Probability Trading Strategies
               </div>
            </div>
          </div>
        </div>


        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Platforms
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>


        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                People
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Content
               </div>
            </div>
          </div>
        </div>

       </div>
     </div>
   </div>




   <div class="container mt-0 mb-2" v-if="tabs[5].isActive">
     <div class="row">
       <div class="col-md-12 py-0">


        <div class="accordion mb-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne"> 
                Resources Updates 1 – Month of May 2021
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                May 28th, 2021. 
                <ul><li>Paper-trading might not fully mimic real-time trade fills. [<a href="https://www.reddit.com/r/options/comments/apux73/negotiating_with_td_ameritrade/">Reference via. @Reddit</a>]</li> <li>How live fills can compare to paper-trading fills. Answer: much slower. [<a href="https://www.reddit.com/r/Daytrading/comments/c0l4w1/how_do_fills_compare_live_vs_paper_trading/er5oui3/">Reference via. @Reddit</a>] </li></ul>
                May 26th, 2021. 
                <ul><li>More serious investigations into using current strategy IRL. Tradings hundreds of thousands of options prices back and forth may not particularly be practical in a real world setting.</li></ul>
                May 21st, 2021. 
                <ul><li>Ordered/received great book on reading/understanding/comprehending candle-stick patterns.</li></ul>
                May 21st, 2021. 
                <ul><li>To-do: investigate how taxes/fees/commissions works for gain. </li> <li>To-do: consider being conscious of such (taxes/fees/commissions), and amounts difference from gains in trades.</li> <li>While paper-trading can now be considered successful, consider transitions to live-trading, and what might be the challenges and risks from there.</li> <li>possible new goal: Trade 'til the sky falls down.</li></ul>
                May 19th, 2021. 
                <ul><li>What I need: a basic charting and TA guide. [<a href="https://school.stockcharts.com/doku.php?id=overview:technical_analysis">Reference via. StockCharts</a>] </li> <li>Add article on transitioning from paper trading to live trading.</li></ul>
                May 17th, 2021. 
                <ul><li>Add sourced aritcles/content in strategies section. <a href="/strategies" class="">Link to section.</a></li></ul>
                May 15th, 2021. 
                <ul><li>Article re: thoughts on an upcoming market crash. The message brings some caution as to what to future can hold, but in such, with given and current strategy, I can be more ready for the situation in which gains came be made with SPY going in either direction. The trouble may be, as we've seen this week, is correctly marking the reversals in time and catching the overall direction before it goes against us.
                    [<a href="https://www.fool.com/investing/2021/05/15/stock-market-crash-is-coming-3-stocks-i-aim-to-buy/">Reference via. @seekingalpha.com</a>]
                  </li></ul>
                May 14th, 2021. 
                <ul><li>Best SPY (et others) heat map found so far: [<a href="https://finviz.com/map.ashx">@Finviz Heap Map</a>]</li> <li>Best SPY daily chart found so far: [<a href="https://finance.yahoo.com/chart/SPY/#eyJpbnRlcnZhbCI6ImRheSIsInBlcmlvZGljaXR5IjoxLCJ0aW1lVW5pdCI6bnVsbCwiY2FuZGxlV2lkdGgiOjYuOTc2MDQ3OTA0MTkxNjE3LCJmbGlwcGVkIjpmYWxzZSwidm9sdW1lVW5kZXJsYXkiOnRydWUsImFkaiI6dHJ1ZSwiY3Jvc3NoYWlyIjp0cnVlLCJjaGFydFR5cGUiOiJsaW5lIiwiZXh0ZW5kZWQiOmZhbHNlLCJtYXJrZXRTZXNzaW9ucyI6e30sImFnZ3JlZ2F0aW9uVHlwZSI6Im9obGMiLCJjaGFydFNjYWxlIjoibGluZWFyIiwicGFuZWxzIjp7ImNoYXJ0Ijp7InBlcmNlbnQiOjEsImRpc3BsYXkiOiJTUFkiLCJjaGFydE5hbWUiOiJjaGFydCIsImluZGV4IjowLCJ5QXhpcyI6eyJuYW1lIjoiY2hhcnQiLCJwb3NpdGlvbiI6bnVsbH0sInlheGlzTEhTIjpbXSwieWF4aXNSSFMiOlsiY2hhcnQiLCLigIx2b2wgdW5kcuKAjCJdfX0sInNldFNwYW4iOm51bGwsImxpbmVXaWR0aCI6Miwic3RyaXBlZEJhY2tncm91bmQiOnRydWUsImV2ZW50cyI6dHJ1ZSwiY29sb3IiOiIjMDA4MWYyIiwic3RyaXBlZEJhY2tncm91ZCI6dHJ1ZSwiZXZlbnRNYXAiOnsiY29ycG9yYXRlIjpbXSwic2lnRGV2Ijp7fX0sInN5bWJvbHMiOlt7InN5bWJvbCI6IlNQWSIsInN5bWJvbE9iamVjdCI6eyJzeW1ib2wiOiJTUFkiLCJxdW90ZVR5cGUiOiJFVEYiLCJleGNoYW5nZVRpbWVab25lIjoiQW1lcmljYS9OZXdfWW9yayJ9LCJwZXJpb2RpY2l0eSI6MSwiaW50ZXJ2YWwiOiJkYXkiLCJ0aW1lVW5pdCI6bnVsbCwic2V0U3BhbiI6bnVsbH1dLCJjdXN0b21SYW5nZSI6bnVsbCwic3R1ZGllcyI6eyLigIx2b2wgdW5kcuKAjCI6eyJ0eXBlIjoidm9sIHVuZHIiLCJpbnB1dHMiOnsiaWQiOiLigIx2b2wgdW5kcuKAjCIsImRpc3BsYXkiOiLigIx2b2wgdW5kcuKAjCJ9LCJvdXRwdXRzIjp7IlVwIFZvbHVtZSI6IiMwMGIwNjEiLCJEb3duIFZvbHVtZSI6IiNmZjMzM2EifSwicGFuZWwiOiJjaGFydCIsInBhcmFtZXRlcnMiOnsid2lkdGhGYWN0b3IiOjAuNDUsImNoYXJ0TmFtZSI6ImNoYXJ0IiwicGFuZWxOYW1lIjoiY2hhcnQifX0sIuKAjG1h4oCMICg1MCxDLG1hLDApIjp7InR5cGUiOiJtYSIsImlucHV0cyI6eyJQZXJpb2QiOjUwLCJGaWVsZCI6IkNsb3NlIiwiVHlwZSI6InNpbXBsZSIsIk9mZnNldCI6MCwiaWQiOiLigIxtYeKAjCAoNTAsQyxtYSwwKSIsImRpc3BsYXkiOiLigIxtYeKAjCAoNTAsQyxtYSwwKSJ9LCJvdXRwdXRzIjp7Ik1BIjoiI2FkNmVmZiJ9LCJwYW5lbCI6ImNoYXJ0IiwicGFyYW1ldGVycyI6eyJjaGFydE5hbWUiOiJjaGFydCJ9fSwi4oCMbWHigIwgKDIwMCxDLG1hLDApIjp7InR5cGUiOiJtYSIsImlucHV0cyI6eyJQZXJpb2QiOiIyMDAiLCJGaWVsZCI6IkNsb3NlIiwiVHlwZSI6InNpbXBsZSIsIk9mZnNldCI6IjAiLCJpZCI6IuKAjG1h4oCMICgyMDAsQyxtYSwwKSIsImRpc3BsYXkiOiLigIxtYeKAjCAoMjAwLEMsbWEsMCkifSwib3V0cHV0cyI6eyJNQSI6IiNmZjMzM2EifSwicGFuZWwiOiJjaGFydCIsInBhcmFtZXRlcnMiOnsiY2hhcnROYW1lIjoiY2hhcnQifX19LCJyYW5nZSI6bnVsbH0-">@Yahoo SPY Chart</a>]</li> <li>"Flash crashe(s)" in recent history, and why we might continue to see more. Also, evidence that recoveries are usually quick. [<a href="https://www.investopedia.com/articles/investing/011116/two-biggest-flash-crashes-2015.asp?utm_campaign=quote-yahoo&amp;utm_source=yahoo&amp;utm_medium=referral">Reference via. Investopedia</a>]</li></ul>
                May 10th, 2021. 
                <ul><li>New article: An interesting article via. r/options re: research and results of trades made by US Senators. Concludes with data that shows there are winners and losers, that not surpisingly the tech (FAANG) is the most popular, and that such politicians do well enough to beat the S&amp;P 500. [<a href="https://www.reddit.com/r/options/comments/n940ze/i_analyzed_9000_trades_made_by_us_senators_in_the/">Reference via. r/options</a>]</li> <li>New tools site: Another great SPY reference site, detailing past and current SPY candlestick patterns. Hyper useful. [<a href="https://www.investing.com/etfs/spdr-s-p-500-technical">Reference via. @investing.com</a>]
                </li></ul>
              </div>
            </div>
          </div>
        </div>

        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne"> 
                Platform Updates 1 – Month of May 2021
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                May 24th, 2021.
                <ul>    
                  <li>Start refining, updating strategies section.</li>        
                </ul>
                May 22nd, 2021.
                <ul>    
                  <li>Consider updating site to focus solely on options trading; removing moderate/safe sections in portfolios.</li>        
                  <li>Consider addition or transition of website to live-trading. Would like to keep the "playfulness" of paper trading, but some how, would like to pose contents (?) for serious readers.</li>
                  <li>Possibly, in the future, may be able to trade such accounts on a limited number of days in the week, rather than currently, every single day. Market updates, and chart analysis should continue to be exactly the same.</li>
                </ul>
                May 21st, 2021.
                <ul>    
                  <li>Remove targeted, value account goals.</li>        
                  <li>Update goals, moreover, to fight for overall consistency, growth and mental health.</li>
                </ul>
                May 20th, 2021.
                <ul>            
                  <li>Experimented with TOS on desktop – got it to work, but still overall clunky. Settling with yahoo's daily chart and TOS tablet app.</li>
                  <li>Updated tablet settings/ui-preferences to streamline only core functionalities.</li>
                  <li>Hoping to find some time to detail current strategy, and do some research on more TA.</li>
                  <li>Updates to main strategy.</li>
                </ul>
                May 19th, 2021.
                <ul>            
                  <li>Worked with TOS support to enabled real-time data in paper-trading account.</li>
                </ul>
                May 18th, 2021.
                <ul>            
                  <li>Consolidate sections.</li>
                </ul>
                May 15th, 2021.
                <ul>            
                  <li>Add strategies description.</li>
                </ul>
                May 12th, 2021.
                <ul>            
                  <li>Remove stocks from Aggro 1 account, and update to options only.</li>
                </ul>
                May 10th, 2021.
                <ul>            
                  <li>Considering whether I should continue planning on trying to utiltize leveraged ETFs, or giving it up and just sticking to options. Such ETFs seem to only add another layer of complexity to things already happening.</li>
                  <li>Possibly: One idea could be to dedicate and build an entire to platform for such strategy?</li>
                </ul>
                May 7th, 2021. 
                <ul>
                  <li>Realizing there are only so many trades of SPY you can make in a day. Considering opening an account with focus, but not limited to SPY.</li>
                </ul>
                April 27th, 2021. 
                <ul>
                  <li>Was trying to find a good platform that would allow me to make multiple paper trading accounts under one platform. Tried a bunch of different things but none ended up working as well as I wished. So now, currently, I'm hoping to continue messing with TD's Think or Swim app, and go forward with looking how to put together my own little game, via. this website somehow.</li>
                </ul>
              </div>
            </div>
          </div>
        </div>

        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Website updates 1 – Month of May 2021
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                May 21st, 2021. 
                <ul>
                  <li>Add some tackiness.</li>
                </ul>
                May 10th, 2021. 
                <ul>
                  <li>Layout update.</li>
                </ul>
                May 7th, 2021. 
                <ul>
                  <li>Update layout, design.</li>
                </ul>
                May 5th, 2021. 
                <ul>
                  <li>Add arrow keys for navigation. Add content, and fix up styles/formatting.</li>
                </ul>
                April 30th, 2021. 
                <ul>
                  <li>Added charts section (empty), and updated portfolios page with real time SPY price (API). Started reading "Around the World...".</li>
                </ul>
                April 29th, 2021. 
                <ul>
                  <li>Refine content, push to web. </li>
                </ul>
                April 28th, 2021. 
                <ul>
                  <li>Add content to websites section and other links. </li>
                </ul>
                April 27th, 2021. 
                <ul>
                  <li>Mock website layout and begin filling general content. </li>
                </ul>
                April 24th, 2021. 
                <ul>
                  <li>Purchase domain name.</li>
                </ul>
              </div>
            </div>
          </div>
        </div>

      </div>
     </div>
   </div>

   <div class="container mt-0 mb-2" v-if="tabs[6].isActive">
     <div class="row">
       <div class="col-md-12 py-0">


        
        <div class="accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne"> 
                What is this thing?
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                This website, and project, primarily revolves SPY (S&P500 ETF), and observations in tracking its general/daily movements.
               </div>
            </div>
          </div>
        </div>

        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                What platforms am I using? 
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                For the main trading account (AGRRO 1), I am using TD Ameritrade's Think or Swim app, on the iPad. 
                <br><br>
                For all other accounts (MODERATE 1 and SAFE 1), I am trading these almost literally on paper, and through text. Being simple enough in trade actions, little real calculations is involved.
               </div>
            </div>
          </div>
        </div>


        <div class="accordion mt-2" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button text-uppercase" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                Who am I? 
              </button>
            </h2>
            <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordionExample">
              <div class="accordion-body">
                Po Rith (<a href="https://github.com/jpoechill">@jpoechill</a>) is a designer and web developer from Oakland, CA. 
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
export default {
  mounted () {
    this.showMoreHeightStatic = this.$refs.showMoreContainer.clientHeight
    this.showMoreHeightDynammic = 0
  },
  data () {
    return {
      showMoreHeightStatic: 0,
      showMoreHeightDynammic: null,
      showViewMore: true, 
      tabs: [
        {
          name: 'marketObs',
          isActive: true
        },
        {
          name: 'balances',
          isActive: false
        },
        {
          name: 'charts',
          isActive: false
        },
        {
          name: 'strats',
          isActive: false
        },
        {
          name: 'resources',
          isActive: false
        },
        {
          name: 'updates',
          isActive: false
        },
        {
          name: 'about',
          isActive: false
        }
      ]
    }
  },
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
  }
}
</script>

<style>
</style>
