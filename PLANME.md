# python-datascience-summerproj
ALL INVOLVED ARE WELCOME TO EDIT. MAKE SURE TO DOCUMENT CHANGES WELL


BIGGEST PROBLEMS:
1. Classifying tweets for positive or negativeness towards a currency. note that this can be solved AFTER we
model speculation, but having a solution will increase our model's effectiveness if users posess or percieve
a bias. the market value may be resistent to bear predictions, certain "key players" may be predisposed to 
negativity, and thus be less "heeded" when advising a sell. Or vice versa, but keep in mind the market is 
characterized by extreme optimism on the part of its core users.


Just for the sake of documentation: the general idea here is to combine a bit of CS and a bit of Economics to 
test our ability to model a market. in this case we're going to use cryptocurrency markets under the assumption
that their drivers are almost entirely limited to simple speculation. The following consists of our primary
questions: how can we get usable data on speculation? where can we get ENOUGH of it? how can we model this 
speculation in the market? 
this includes: 

Who are the key influencers of speculation? 

To what degree does "group mentality" exist in the speculation data? 

How does speculation coincide with price fluctuations?

Is the reverse true? is it possible that prices are driving speculation instead?(we as authors percieve a large lack
of understanding of the cryptocurrency market, perhaps success has had has more to do with the overall large gains
in cryptocurrency markets over the last year, and less to do with proper investment decisions).


Finally, we will try to use our gained understanding of the market functioning to predict its fluctuations
in real time, and evaluate for predictive power.



The big questions:
1. What will our speculation data be? (first suggestion is mentionings of currency by name on social media)
  1a. RAW DATA: Twitter will be best, use of hashtags and relatively short text to be processed.
  1b. Raw data from twitter will be processed into a database to be kept as simple as possible. definitely
      we will need a table for tweets, and a table for network nodes (users), then later on we need data
      for the movements of the markets, but this will come much later
  1c. We may later want to differentiate between "positive" and "negative" speculation, while natual laguage
      processing is clearly beyond the scope of this project, simple metrics may be effevtive to get a sense
      of wether some speculation data is BULLish or BEARish. 
  1d. (Zheng) Maybe include market data into our raw data to help explain variances unable to be explained just by twitter?
  ie. (Zheng) number of retweets and number of favorites should give extra weights to our words, but this 
      depends on what method we are gonna eventually use.
2. How can we gather enough unbiased data to be confident it represents a true sample of speculation?
  2a. (Zheng) If we are gathering from "important" people to gather "important" words, we probably needn't to worry about bias so far.
      Just gather enough size of data, and use cross validation to prove our prediction accuracy is high. In another way, our collected
      sample is our population.
3. How can we best model it? (first suggestion is to throw shit at the wall until something sticks)
  
  (Zheng) we should collect data first and then think about what models we should use. Essentially, simple techniques may work,
  like logistic regression or time series analysis, but maybe we will need to go to some machine learning stuff, like support
  vector machine, principle component analysis, or neural network.

  3a. First must determine if any crowd mentality exists, we need to see to what degree "mentionings" of
      currencies coincide with each other past random chance.
      3aa.Also may want to account for weights on currencies based on how widely known the currency is,
      
  3b. Then we want to find the "KEY PLAYERS" in speculation. Who had the most network influence over
      the mentionings of others?
      3ba.A offshoot of this is, do we expect KEY PLAYERS to follow the advice of other key players?
          Will these KEY PLAYERS ignore the speculation shifts they did not start?
          
  3c. If no effective modeling is found from the speculation side, we might try the reverse: watch price changes,
      and see if speculation FOLLOWS instead of LEADS the market. this may become a key question to answer.
  
  3d. finally we will look for correlation between speculative shifts and price shifts, or the reverse.
      3da. do we see more correlation with positive speculation? negative speculation? 
 
4. Can our process be made fast enough for real-time predictions?
5. Will our results, or our process, be useful for anything other than real-time predictions?
  5a. (Zheng) programming and statistical models are just tools. Methods can be flexibly changed to predict other 
      price changes, or even flu trend and box office (done by others).
