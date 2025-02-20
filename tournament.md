---
layout: page
title: Tournament
permalink: /tournament/
---

* Ranking
* Rules
* Prizes
  * Most Interesting Strategy Agent Prize
{:toc .large-only}

Agents will be evaluated based on their average ranking over several
tournaments. Each tournament is a scenario where each agents has
a fixed fleet, consisting of different vessels, which will run through
a number of years of shipping operation. The shipping operation depends on cargoes to be transported that are auctioned off in a reverse second-price (aka Vickrey) auction on a regular basis.
For heterogeneous fleets, each competition will be repeated so that every agent has operated each fleet exactly once.
The fleets' sizes will vary from smaller to larger.


Your agent should be generic enough to play with different fleet sizes of different ship types and cargoes in various locations.

# Ranking

Each agent will participate in the same number of maritime shipping scenarios against the agents designed by other teams. 
The agent’s ranking is based on the income the agent made.
This income is the difference between the revenue from the contracts won by the agent and the cost of running the fleet and any penalties for not fulfilling contracts.
The agents will be ranked in each scenario and the overall ranking is the average ranking over all scenarios.

# Rules

Agents may be disqualified if they violate the spirit of fair play.

Additionally, the following behaviours are strictly prohibited: 

1. Designing an agent in such a way that it benefits
some specific other agent
2. Starting new Threads/Processes
3. Hacking the API in any way
4. Access private fields, i.e. any field that starts with an underscore, e.g. _name.
5. Accessing parts of the simulation or modifying parts of the simulation including:
   1. the core simulation,
   2. vessels, trades, your competitors or any other parts that are not part of your implemented agents class.

# Prizes

The first three teams according to the average tournament ranking will receive a certificate and a cash prize.
The overall winner will receive £500, the runner-up will receive £300 and the team placing third will receive £100.

Additionally, the team with the *most interesting strategy agent* prize will receive £100.

## Most Interesting Strategy Agent Prize

Besides the agents' tournament, teams also have the opportunity to receive the most interesting strategy agent prize.
For this prize we will evaluate the reports that are submitted with the agents as well as the presentations during the competition session.
We will award this prize after a deliberation by a panel following the presentations.
Therefore only those teams that present their work are eligible for this prize.
The most important criterion for the award will be the innovation of the presented strategy.
