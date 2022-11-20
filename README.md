# Pricing FX Forward Contract


This article discusses the valuation of Foreign Exchange Rate Forward Contract (FEF). An FX forward contract is an obligation to exchange a particular amount of one currency for a certain amount of another currency at a future time. 

Notations used as follows.

t	Valuation Date
T	Maturity Date
 
Settlement Date
 
Spot Exchange Rate at time  

 
Risk-free discount rate of currency Ccy
K	Strike price
 
Forward exchange rate for time interval (t,  ), where  

N	Notional amount

The forward exchange rate is computed as is computed as  , where  . 

The actual pricing (Mark-to-Market) on FEF is done at the inventory level and is in the base currency, which is usually USD. 

Direct Quote

The rates are quoted as  . Payoff currency is always USD and notional currency is either USD or EUR. 


1.	Notional currency = EUR

The payoff at the maturity is defined as   in USD. The expected payoff is then calculated as

 .

where   (1 or –1) is the long / short indicator. The price of the contract in USD is obtained by discounting the expected payoff with USD.

       	                        (1)

where   is the USD discount factor between the settlement date and the valuation date.

2.	Notional currency = USD

The payoff at the maturity is defined as   in USD. Similarly, the price of the contract in USD is given by

       	                        (2)

For all of the above cases, the dollar value Delta in USD is computed as

USD Delta                                         (3)

where   is the spot exchange rate and the perturbation on the spot rate   is set to be 0.00005. This dollar value delta is used for daily hedging.

Indirect Quote

The rates are quoted as  . Payoff currency is always CAD and notional currency is either USD or CAD.

1.	Notional currency = USD

The payoff at the maturity is defined as   in CAD. The price of the contract in USD is obtained by dividing the expected payoff by the forward rate,  , and by discounting it with USD

 	   	              (4)

2.	Notional currency = CAD

The payoff at the maturity is defined as   in CAD. The price of the contract in USD is obtained by dividing the expected payoff by the forward rate,  , and by discounting it with USD

 	   	              (5)

The price of the contract and the perturbation of the spot rate in delta calculation is in USD/CAD. Thus, the perturbation of the spot is done as   and   where  . Thus, the USD Delta is defined by

USD Delta =                                             (6) 

The lag between the maturity date and settlement date is usually 2 business days for direct quote and 1 business day for indirect quote. For instance, the forward rate,  , is observed at the maturity date, T, and settled on the settlement date,   or  . When FEF deals are entered directly into Inventory,   is, by default, set equal to T. Since there is no lag between T and   for FEF, the forward rate in the pricing formulae needs to be specified: it is the rate settled on  . It should also be noted that the discount factor is calculated from the maturity date to the valuation date, i.e.  . In other words, the pricing formulae, equations (1), (2), (4) and (5), become

       	                        (1’)
       	                        (2’)
 	   	              (4’)
 	   	         (5’)

As long as  , which is the case for FEF, the valuation is done based on forward rate settled on   and the discount factor between the settlement date (since  ) and the valuation date. It agrees with the pricing discussed in the previous section. 

Testing results for direct quote are summarized in table 1 (pricing) and table 2 (USD delta). The first case in tables 1 and 2 deals with a matured FEF and the pricing in equations (1) and (2) are modified as the following. 

 	    			(7)
     			(8)

Similarly, testing results for indirect quote are summarized in table 3 (pricing) and table 4 (USD delta). The pricing modification for a matured FEF (first case in tables 3 and 4) is done as following.

 			 (9)
  			(10)

The forward rates in equations (1), (2), (4) and (5) become the spot rate   in the above equations. Since the pricing for these matured FEF involves the spot price, which varies day-to-day, there is non-zero delta values on these cases. You can find similar valuation topics at https://finpricing.com/lib/FiZeroBond.html

