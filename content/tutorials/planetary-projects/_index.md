---
title: "6. Planetary Projects"
date: 2018-09-18T17:13:49+02:00
weight: 10
---

This guide is also available in video format. __Click below to watch the video or scroll down for the written version.__

{{< youtube dtXVowBEvfQ >}}

## Introduction

Planetary projects are collectively erected and maintained structures that provide a bonus or service to the inhabitants of a planet. If projects are present on a planet, they will be listed under “Infrastructure” in the PLI window as well as the PPS window (accessible at the top of the PLI window).

![PP button](pp-button.png)

Clicking “details” next to an entry in the PPS window will reveal more information on that project.

![PP button](pps-buffer.png)

## Building a planetary project

New planetary projects can be initiated by anybody with a base on the respective planet. To do so, open the planet’s PPS window and select “contribute” next to the desired planetary project.

![Contribute to PP](contribute.png)

In the new project window - the project being a CoGC in this example -, you can track the cost of building the project, the progress that has been made towards its construction, and the individual contributions made by inhabitants of the planet. Use the sliders to select the size your contribution.


![CoGC in construction](cogc-in-construction.png)

Once all contributions have been filled by the planet’s inhabitants, the finished project will become visible as a green plot on the planet. Clicking the plot will open a new buffer about the project.

## Planetary project types

Once built, a planetary project requires an upkeep to stay active. As long as the upkeep is not being paid, the project remains “on strike” and provides no bonuses. Similarly to the construction of a planetary project, contributions towards its upkeep can be made by anyone residing on the planet in question.

![Contribute to upkeep](contribute-to-upkeep.png)

To contribute, open the project’s buffer by clicking its name under “Infrastructure” or its plot on the planet (in a PLI window). Under “Upkeep”, select “contribute”. In the new window, set the slider(s) to the desired amount and hit “CONTRIBUTE”. Your contribution will be listed at the bottom along with all other recently made contributions.

### Chamber of Global Commerce (CoGC)

A Chamber of Global Commerce can run a variety of programs to stimulate a planet’s economy. Open the buffer of a CoGC by clicking its name under “Infrastructure” or its plot on the planet (in a PLI window). In the new CoGC window that opened up, you can see the CoGC’s current and upcoming programs listed under “Programs”.

![CoGC overview](cogc-overview.jpg)

#### Voting for Programs

To vote on the upcoming program, select “programs / vote”, which opens up a list of all available programs. Note that only rated companies can cast their vote, i.e. those which are operating under an APEX [PRO License](https://hub.prosperousuniverse.com/license/purchase).

![CoGC programs](cogc-programs.jpg)

Click a program’s name or the respective “view details / vote” button learn more about it. Hit “Vote” to give your vote to the desired program; the one with the most votes will be listed as the upcoming program in the planet’s COGC buffer.

![Vote buffer](vote-buffer.png)

Votes are not equal, but instead depend on the voting company's influence, which in turn depends on the size and composition of their work force. Each _individual worker_ grants influence; a pioneer grants 1 influence, and hence 100 pioneers grant 100 influence. Higher tier workforces have higher multipliers:  

| Worker type 	|	Influence multiplier	|
|---------------|---------------------------|
| Pioneer 		| 1							|
| Settler		| 1.25						|
| Technician 	| 1.5						|
| Engineer		| 1.75						|
| Scientist		| 2							|

For example, a company employing 200 pioneers, 100 settlers, and 200 technicians has an influence of 200 * 1 + 100 * 1.25 + 200 * 1.5 = 625.

#### Upkeep Costs

The CoGC's programs require payment of an upkeep cost in the form of materials to go into effect.  

![Program upkeep](cogc-upkeep.png)

The materials required as upkeep are DW, MCG, PE and RAT.  The total amount required of each material in upkeep is determined by the number of player bases on the planet multiplied by the material multiplier.  The multipliers are 3x for DW, 4x for MCG and PE, and 2x for RAT.  The minimum upkeep cost of five times the multipliers is used until a planet has enough bases to surpass it.

### Local Markets

Local Markets are a means for exchanging goods outside of Commodity Exchanges. Due to their important role in the economy, please refer to [this dedicated tutorial](../local-markets) on how they are used.

### Administration Center

The AC allows you to hold elections for a planetary governor, who can set taxes and fees. Only planetary residents are eligible to vote, but anyone can run. Each term is two weeks long.

Once erected on a planet, the building will be listed as the “Planetary Administration Center” under Infrastructure in the PLI window. Clicking the entry will open the ADM window, which lists information on the current governor and the next election. The governor's Corporation and Faction are important because one of them always collects the total local fees paid by the planet's residents (see below).

![ADM](adm-overview.png)

#### The Election Campaign

The current candidates for governor are listed at the bottom of the upcoming term section. Select the VOTE button next to your favorite candidate to cast your vote.

![Voting](adm-vote.png)

If you'd like to run for governor, select the RUN button below the list to throw your hat in the ring. All residents of the planet will be notified about the outcome of the election.

![Election outcome](voting-outcome.png)

#### Being the Governor

If you won the election, you may now set the fees that apply on your planet until the end of your term. To do so, bring up the LR window of your planet (e.g. by selecting it at the top of the ADM window). It will show the current fees and feature an EDIT button at the top.

![ADM Edit](adm-edit.png)

Clicking it will allow you to change the metrics shown below. Note that certain restrictions to the rules apply within faction-space, i.e. on the starting planets and other planets in their systems. 

![LR buffer](lr-buffer.png)

**Currency:** The currency in which the fees must be paid. Within Faction space, this will always default to the local Faction's currency. Otherwise, it will be the currency of the selected fee collector (see below).

**Fee collector:** This drop-down allows you to select which entity will receive the collected fees by means of a weekly dividend payout, currently every Monday. Your choice is between the Corporation you are a member of (if applicable) and a Faction.

If you select your Corporation, the money will be distributed among all members according to the shares they own. If, for example, a member owns 50% of a Corp's shares, they will receive 50% of the dividend payouts. The dividend's currency will be the same as the collected fees, regardless of the Corporation's default currency. Your Corporation's past payouts and a countdown to the next one can be viewed in the CORPFIN buffer.

Which Faction you are able to select depends on whether the planet is in Faction space, in which case the ruling Faction can be selected – or not, in which case you may select the Faction you yourself belong to (i.e. the one determined by your original starting planet). Select the desired entity and hit UPDATE below to lock in your choice.

**Local Market fees:** This section allows you to impose fees on the planet's [Local Market](../local-markets) (if there is one). The base fee denotes the up-front cost that residents have to pay to place an ad on the Local Market. The time factor determines what the ad will additionally cost them per day. For instance, setting the values to 100 CIS and 5 CIS respectively will put the total price of an ad running for five days to 125 CIS. Note that both values are limited in faction space; in the example shown above, the limits are 50-150 for the base fee (the value left of the forward slash) and 3-8 for the time factor (after the slash).

**Production fees:** You may set different [production](../production) fees for each industry here. These fees are collected when a production order is placed in any production line on the planet, and they scale linearly with the order size. The amount and collector are listed near the bottom of every PRODCO window as shown below. Note that production fees are also limited within faction space. The possible range is listed at the top of the Local Rules list (10-30 in the example above).

![Production fees example](production-fees-example.png)

*Local Market fees and production fees can only be changed a combined 5 times per term.* The UPDATE button at the bottom locks in your changes for both of them, the figure above it shows how many more changes are possible.

## About this page

This page is part of the advanced tutorial series, which encompasses parts 3 through 8. Use the arrows on the sides to cycle through all available tutorials in order, from introductory to more and more specific topics.

If you encounter an error or cannot find the answers to your questions, we will gladly help you on our [Discord server](https://discordapp.com/invite/G7gj7PT).
