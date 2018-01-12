# Scalable Reinforcement Learning solutions via Neural Networks for Smart Grid applications

# 1. Introduction:


Demand Response is the ability of the energy consumers to modify their load consumption behavior as a reaction to changes in electricity prices. Recent trends in the spiraling rate of consumption (obtain data) of electricity has placed additional stress on utilities to balance supply with demand. In peak periods, generators with a high marginal cost of production have their bids accepted to clear the forecasted demand, which results in increase in electricity prices during this period. In some regions, such as California, the rate of change of demand in peak periods is so severe (the infamous duck curve) that generating units often produce more power than necessary in non-peak periods as a consequence of limits on their ramp rates. Demand response programs encourages consumers to reduce or shift their electricity usage in peak hours to non-peak hours where the prices are lower. The consumers are benefited by lower tariffs, and the utilities can ensure productive utilization of resources, maintain stability of the grid, prevent outages, and reduce harmful emissions that often occur due to the commitment of expensive, inefficient, and high-polluting generating units.

To add:


%Objectives of DR


%Impact of DR


%Current position in 2017


# 2. Aggregators:


CAISO (California ISO) Demand Response Guide: "A Demand Response Provider (DRP) with the ability to aggregate customers capable of reducing their electric demand (load) can participate in the ISO day-ahead, real-time and ancillary services markets as a Proxy Demand Resource (PDR) or Reliability Demand Response Resource (RDRR)."

Aggregators are third party service providers that sell combined demand load reductions to utilities and ISO. They provide a platform for a large-scale consumer participation in Demand Response programs that can be centralized and easily coordinated with the utilities and ISO. 


# 3. Electricity Markets:


Electricity markets are structured as a sequence of forward markets with progressively shorter trading windows which finally culminates into a spot market. This spot market, or the real-time market, is where the final adjustments in trades are made based on real-time load demand. There are two types of markets currently in USA, the wholesale market and the retail market. The wholesale market are moderated by Independent System Operators (CAISO, MISO, ERCOT, PJM, ISO New England) and are centralized i.e. buyers and sellers have no knowledge of each other. This competitive wholesale market has evolved from the need to reduce costs, increase efficiency and bring transparency into the process of generating and supplying electricity. The retail market, however, is currently present in 13-14 states in the US, and aims to empower the final consumer.

The Wholesale Market is controlled and moderated by Independent System Operators (ISO) that ensure a fair market ground and a consistent set of rules to the Generating companies (Gencos) and "Load Serving Entities" (LSE). Once the trading window is closed, it is the responsibility of the ISO to ensure that the supply and demand is balanced on a real-time basis, the operational constraints are factored into the various financial settlements, and that the "unit commitment" and "economic dispatch" signals are appropriately sent to the generators. Though the bulk of electricity purchased by LSEs based on estimated load forecasts is bought in advance through forward contracts, a constant refinement is needed as the delivery date gets closer due to errors in the load forecast. Almost, 65% of the electricity delivered is purchased through forward contracts. Two types of trading, which leads to two different and consecutive financial settlements, exist in almost all (?) Wholesale Markets where the traders can refine and fine tune their purchases to rectify the forecasts errors. Let's look at two types of markets depending on the time of settlement that occurs to mitigate spot-price risk and balance the demand. 

# 3A. Day Ahead Market:

This market is settled 24 hours in advance and allows all participants to submit their bids and offers for the trade of electricity. Bids are submitted by Gencos, and offers are submitted by LSEs. The bids are then arranged in ascending order of cost per KWh (price) and selected sequentially from top to bottom order upto the point in the "stack" where the cumulative supply is equal to or more than the forecasted load estimate (who generates this forecast?). The price at which this "clearance" occurs is considered to be the marginal cost and all the bids below this price in the "stack" are accepted. The price that all bidders receive for their product is the clearance price, and the bidder with the lowest price gains the most profit. This is done to prevent bidders from overestimating their true cost of production while stating their prices, and provide incentives to reduce the price of their bids. The Gencos whose bids are rejected are mostly the expensive ones that get utilised during peak demand, which explains the
increase in pricing during peak hours. The variable cost of production of renewable energy is minimal, hence most of these enter bids of zero dollars thus lowering the clearing price ("price suppression effect"). Nuclear plants typically place bids less than zero dollars (negative bids) as they are more concerned with committing to a longer runtime due to the startup and shutdown costs of a reactor.

# 3B. Real-time Market:
 - Balanced in real-time based on actual load demand. Settlements are made every 15 minutes.
 - Difficulties in predicting RTPrices
 - Highly volatile
 
 
# 4. Pricing Schemes:
Even though the prices at which electricity is traded in centralised markets fluctuates every hour, the rate that most consumers are charged however remains constant (obtain data) unless they have opted for participation in the Demand Response programs offered by utilities. This flat rate may or may not include a peak pricing component; for which the rate per consumption of KWh at certain times in a day is much higher than the flat rate. The pricing schemes vary based on the type and size of the consumer. Some are:

● Time-of-use (TOU)
● Real-time pricing (RTP)
● Critical peak pricing (CPP)
● Extreme day CPP (ED-CPP)
● Extreme day pricing (EDP)
● Peak time rebates (PTR)

