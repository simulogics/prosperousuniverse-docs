---
title: "Commands list"
date: 2018-09-18T17:13:49+02:00
---

This is a comprehensive list of all commands available to you in APEX. They are grouped together by their respective areas of use. Understanding this list requires that you already be familiar with [how commands work](../../tutorials/legacy-tutorials/commands). You may read through the whole list to gain an overview or use it as a reference to look up specific commands.

Parameters in `<angle brackets>` are required, parameters in `[square brackets]` are optional.

| Category | Commands |
|----------|----------|
| [Bases](#bases) | [`BS`](#bs), [`BSC`](#bsc), [`BBL`](#bbl), [`BBC`](#bbc), [`BUI`](#bui), [`WF`](#wf), [`EXP`](#exp), [`HQ`](#hq), [`BRA`](#bra) |
| [Production](#production) | [`PROD`](#prod), [`PRODQ`](#prodq), [`PRODCO`](#prodco) |
| [Inventory](#inventory) | [`INV`](#inv), [`MTRA`](#mtra), [`UPCK`](#upck) |
| [Ships and flights](#ships-and-flights) | [`FLT`](#flt), [`SHP`](#shp), [`SHPF`](#shpf), [`SHPI`](#shpi), [`SFC`](#sfc), [`SI`](#si), [`RT`](#rt), [`RTE`](#rte) |
| [Ship building](#ship-building) | [`BLU`](#blu), [`SHY`](#shy), [`SHYP`](#shyp) |
| [Contracts](#contracts) | [`CONTS`](#conts), [`CONT`](#cont), [`CONTD`](#contd) |
| [Commodity exchange](#commodity-exchange) | [`CXL`](#cxl), [`CX`](#cx), [`CXM`](#cxm), [`CXP`](#cxp), [`CXPC`](#cxpc), [`CXOB`](#cxob), [`CXPO`](#cxpo), [`CXOS`](#cxos), [`CXO`](#cxo), [`MAT`](#mat) |
| [Foreign exchange](#foreign-exchange) | [`FX`](#fx), [`FXP`](#fxp), [`FXPC`](#fxpc), [`FXOB`](#fxob), [`FXPO`](#fxpo), [`FXOS`](#fxos), [`FXO`](#fxo) |
| [Local markets](#local-markets) | [`LMOS`](#lmos), [`LM`](#lm), [`LMA`](#lma), [`LMP`](#lmp) |
| [Maps and locations](#maps-and-locations) | [`MU`](#mu), [`MS`](#ms), [`SYSI`](#sysi), [`PLI`](#pli), [`STNS`](#stns) |
| [Planetary projects](#planetary-projects) | [`PPS`](#pps), [`PP`](#pp), [`PPI`](#ppi), [`POPR`](#popr), [`WAR`](#war) |
| [Infrastructure](#infrastructure) | [`INF`](#inf), [`INFU`](#infu), [`ASTS`](#asts), [`GTW`](#gtw), [`GTWI`](#gtwi), [`GTWT`](#gtwt) |
| [Politics](#politics) | [`ADM`](#adm), [`GOV`](#gov), [`LR`](#lr), [`MOTS`](#mots), [`MOT`](#mot), [`POL`](#pol) |
| [Social](#social) | [`FA`](#fa), [`CO`](#co), [`USR`](#usr), [`BDGS`](#bdgs), [`CONS`](#cons), [`COM`](#com), [`COMC`](#comc), [`COMP`](#comp), [`COMG`](#comg), [`COMU`](#comu) |
| [Notifications](#notifications) | [`NOTS`](#nots), [`NOTIG`](#notig), [`NOTPNS`](#notpns) |
| [Company and finances](#company-and-finances) | [`FIN`](#fin), [`FINBS`](#finbs), [`FINIS`](#finis), [`FINLA`](#finla), [`LEAD`](#lead), [`ARC`](#arc), [`GIFT`](#gift), [`COLIQ`](#coliq) |
| [Interface and transmissions](#interface-and-transmissions) | [`CS`](#cs), [`SCRN`](#scrn), [`LIC`](#lic), [`TRA`](#tra), [`XIT`](#xit), [`XYTV`](#xytv) |

## Bases

Base commands identify a base by the planet it is on, for example `BS XK-745a`.

### BS – Bases {#bs}

`BS [planet ID]`

Shows an overview of all your bases, or the details of your base on the given planet. The base view has buttons for most other base commands.

### BSC – Base construction {#bsc}

`BSC <planet ID>`

Creates a new base on a planet. Shows the required building materials and lets you choose a plot.

### BBL – Base buildings {#bbl}

`BBL <planet ID>`

Lists the buildings of a base. DEMOLISH removes a building and refunds part of its materials, depending on its age. The possible refund is listed as "Reclaimable materials".

**Shortcut:** the BUILDINGS button in `BS`.

### BBC – Construct building {#bbc}

`BBC <planet ID>`

Constructs a new building in a base. The tabs at the top switch between building categories. "Area" shows the building's area cost and the area left in your base, "Workforce" shows the workers it needs.

**Shortcut:** the CONSTRUCT button in `BS`.

### BUI – Building information {#bui}

`BUI <building ticker>`

Shows a building type: the workforce it employs, the area it takes up and the materials needed to build it.

**Shortcut:** click a building type in `BBC`.

### WF – Workforce {#wf}

`WF <planet ID>`

Shows the workforce of a base and their needs. Higher workforce tiers have more needs. If workers don't get the consumables they need, the efficiency of their buildings drops.

**Shortcut:** the WORKFORCE button in `BS`.

### EXP – Experts {#exp}

`EXP <planet ID>`

Shows the fields experts can boost and the experts assigned to a base. REMOVE deactivates an expert, ACT puts them back to work.

**Shortcut:** the EXPERTS button in `BS`.

### HQ – Headquarters {#hq}

`HQ`

Shows which base is your headquarters. Relocate it to another base for different [faction bonuses](../headquarters), or upgrade it to unlock more base permits and production queue slots.

### BRA – Building repair assistant {#bra}

`BRA [planet ID]`

Repairs several buildings of a base at once: all buildings at or below the condition you set are included.

## Production

### PROD – Production {#prod}

`PROD [planet ID]`

Shows the production lines of all your bases, or of the base on the given planet. Each production line consists of one or more buildings of the same type.

**Shortcut:** the PRODUCTION button in `BS`.

### PRODQ – Production queue {#prodq}

`PRODQ <production line ID>`

Shows the order queue of a production line. Queued orders can be cancelled, orders in progress can't. The efficiency shown depends on worker satisfaction, experts and, for some buildings, the planet's fertility.

**Shortcut:** the DETAILS button in `PROD`.

### PRODCO – Production order {#prodco}

`PRODCO <production line ID>`

Queues a new production order. Choose the output and the order size, and make sure the input materials shown at the bottom are available.

**Shortcut:** the NEW ORDER button in `PROD`.

## Inventory

### INV – Inventories {#inv}

`INV [address or store ID]`

Lists all your inventories: base stores, cargo holds, fuel tanks and warehouse units. With a system or planet (for example `INV XK-745` or `INV XK-745a`), only the inventories at that location are listed. With a store ID, that inventory opens.

Inside an inventory, sort by amount (AMT), weight (WGT) or volume (VOL). The grid view shows each material's weight, volume and book value.

### MTRA – Material transfer {#mtra}

`MTRA [material ticker] [source store ID] [target store ID]`

Transfers an amount of a material between two inventories. Anything not given as a parameter can be chosen in the window.

**Shortcut:** drag a material from the source inventory and drop it on the AMT slot of the target inventory.

### UPCK – Unpack {#upck}

`UPCK <store ID>`

Lists the consumable bundles in a store and unpacks them. Bundles are unpacked into the store they are in.

## Ships and flights

Start with `FLT`: most other ship commands can be opened from there. The [space flight tutorial](../../tutorials/legacy-tutorials/space-flight) shows them in action.

### FLT – Fleet {#flt}

`FLT [system or planet ID]`

Lists all your ships with their transponder code, name, status, cargo, location and current flight. With a system or planet ID, only the ships at that location are listed.

### SHP – Ship {#shp}

`SHP <transponder code>`

Shows the details of one of your ships. Click the ship's name to rename it.

**Shortcut:** click a ship's transponder code in `FLT`.

### SHPF – Ship fuel {#shpf}

`SHPF <transponder code>`

Shows the fuel levels of a ship.

**Shortcut:** click a ship's fuel bar in `FLT`.

### SHPI – Ship inventory {#shpi}

`SHPI <transponder code>`

Shows the cargo hold of a ship. The hold is limited by weight and volume.

**Shortcut:** click a ship's cargo bar in `FLT`.

### SFC – Ship flight control {#sfc}

`SFC <transponder code>`

Plans and starts a flight. Enter a planet or station as the destination, set the fuel usage and press Start.

**Shortcut:** the FLY button in `FLT`.

### SI – Ship information {#si}

`SI <transponder code>`

Shows the public information on any ship, including ships of other players.

**Shortcut:** click a ship's triangle on a system map or in `PLI`.

### RT – Routes {#rt}

`RT [route ID]`

Lists all your routes, or opens a single route. Create and edit routes and assign ships to them. See [Routes](../routes).

### RTE – Route executions {#rte}

`RTE [transponder code]`

Shows the progress of all ships on routes, or of a single ship. See [Routes](../routes/#monitoring-route-execution).

## Ship building

### BLU – Blueprints {#blu}

`BLU [blueprint ID]`

Lists all your ship blueprints, or opens one.

### SHY – Shipyard {#shy}

`SHY [planet ID]`

Shows the shipyard of a planet.

### SHYP – Shipyard projects {#shyp}

`SHYP [project ID]`

Lists all your shipbuilding projects, or opens one.

## Contracts

### CONTS – Contracts {#conts}

`CONTS`

Lists all your contracts. Click a contract to open it in `CONT`. Pending contracts are also listed in the right sidebar, which the SDBR button on the left toggles. See the [contracts tutorial](../../tutorials/legacy-tutorials/contracts).

### CONT – Contract {#cont}

`CONT <contract ID>`

Shows a single contract. Contract IDs are long, so it's easier to open contracts from `CONTS`.

### CONTD – Contract drafts {#contd}

`CONTD [draft ID]`

Lists your contract drafts, or opens one to edit and send it. See [custom contracts](../custom-contracts).

## Commodity exchange

A commodity exchange ticker combines a material and an exchange, for example `RAT.NC1`. The [market guide](../../tutorials/current-tutorials/05-market-guide) shows these commands in action.

### CXL – Commodity exchanges {#cxl}

`CXL`

Lists all commodity exchanges.

### CX – Commodity exchange {#cx}

`CX <exchange code>`

Shows a commodity exchange and its materials, sorted into categories. Each material has buttons for the ticker commands below.

**Shortcut:** click an exchange in `CXL`.

### CXM – Material comparison {#cxm}

`CXM <material ticker> [planet ID]`

Compares a material across all commodity exchanges. With a planet ID, the exchanges are sorted by their distance to that planet.

### CXP – Price information {#cxp}

`CXP <ticker>`

Shows current bids and asks, all-time highs and lows, and more.

**Shortcut:** the INFO button in `CX`.

### CXPC – Price chart {#cxpc}

`CXPC <ticker>`

Shows a candlestick chart of the price over time. "No data" means nothing was traded in the selected period. Choose a longer one.

**Shortcut:** the CHART button in `CX`.

### CXOB – Order book {#cxob}

`CXOB <ticker>`

Shows the open buy and sell orders.

**Shortcut:** the ORDERS button in `CX`.

### CXPO – Place order {#cxpo}

`CXPO <ticker>`

Places a buy or sell order within the current price band. The band is based on a three-day average and is wider for PRO users. The "set" buttons fill in the current best bid or ask, "Inventory" selects where to sell from.

**Shortcut:** the TRADE button in `CX`.

### CXOS – Commodity exchange orders {#cxos}

`CXOS`

Lists your buy and sell orders. Deleting an order that isn't completely filled withdraws it from the market.

### CXO – Commodity exchange order {#cxo}

`CXO <order ID>`

Shows one of your orders.

**Shortcut:** the VIEW button in `CXOS`.

### MAT – Material {#mat}

`MAT <material ticker>`

Shows a material: what can be made from it ("Wrought product") and how it is produced ("Production"). The ticker is the short code on the material's icon, for example STL for steel.

**Shortcut:** click a material's icon, for example in `CX`.

## Foreign exchange

A currency pair is written as two currency codes, separated by a slash or a dot, for example `AIC/CIS`. See the [foreign exchange tutorial](../../tutorials/legacy-tutorials/foreign-exchange).

### FX – Exchange rates {#fx}

`FX`

Shows a matrix of exchange rates, with the base currencies arranged vertically and the quote currencies horizontally.

### FXP – Exchange rate information {#fxp}

`FXP <currency pair>`

Shows exchange rate information for a currency pair.

**Shortcut:** click a rate in `FX`.

### FXPC – Exchange rate chart {#fxpc}

`FXPC <currency pair>`

Shows the exchange rate history of a currency pair.

### FXOB – Order book {#fxob}

`FXOB <currency pair>`

Shows the open orders for a currency pair.

### FXPO – Place order {#fxpo}

`FXPO <currency pair>`

Places a foreign exchange order, buying one currency with another. Amounts are in lots of 1,000 units of each currency.

### FXOS – Foreign exchange orders {#fxos}

`FXOS`

Lists all your foreign exchange orders.

### FXO – Foreign exchange order {#fxo}

`FXO <order ID>`

Shows one of your foreign exchange orders.

**Shortcut:** click a notification about a foreign exchange trade.

## Local markets

### LMOS – Local market ads {#lmos}

`LMOS`

Lists all your local market ads.

### LM – Local market {#lm}

`LM <planet or station ID>`

Shows the ads at a local market.

**Shortcut:** the Local Market infrastructure entry in `PLI`.

### LMA – Local market ad {#lma}

`LMA <ad ID>`

Shows the details of an ad.

**Shortcut:** click an ad in `LM`.

### LMP – Post ad {#lmp}

`LMP <planet or station ID>`

Posts an ad at a local market.

**Shortcut:** the POST AD button in `LM`.

## Maps and locations

Drag with the left mouse button to move a map and with the right mouse button to rotate it. Some maps can be shown in 2D with the "Fix 2D" option.

### MU – Universe map {#mu}

`MU [CX | NAV]`

Shows the universe map. The connected dots are star systems. Hover over one to see its ID. The toggles at the bottom switch map layers on and off, and some data can be filtered by time period.

* `MU CX` shows the commodity exchanges.
* `MU NAV` shows traffic. While "fleet" is on, your ships are marked by yellow arrows. See the [space flight tutorial](../../tutorials/legacy-tutorials/space-flight).

### MS – System map {#ms}

`MS <system ID>`

Shows a star system with its star in the middle. Circles are rocky (white) or gaseous (orange) planets, squares are space stations. Hover over one to see its ID. Your ships are marked by yellow arrows. Turn on "traffic" to see other users' ships as white arrows.

**Shortcut:** click a system on the universe map.

### SYSI – System information {#sysi}

`SYSI [system ID]`

Shows a system's name, star type, micrometeoroid density and faction affinity, and lists its planets and stations. A system ID is the sector ID (two letters) followed by the system number, for example `XK-745`. Without an ID, you can search for systems.

### PLI – Planet information {#pli}

`PLI [planet ID]`

Shows a planet: the resources in its ground and atmosphere, its fertility, and its type and temperature, which decide whether a base needs [additional construction materials](../building-costs). Also links to your fleet and inventories on the planet. A planet ID is the system ID followed by a letter, for example `XK-745a`. Without an ID, you can search for planets.

The fertility bar starts in the middle: the further it extends to the left, the less fertile the planet, the further to the right, the more fertile.

Click a coloured plot for details:

* blue: other companies
* dark blue: another corporation's project
* yellow: your company
* dark yellow: your corporation's project
* green: Chamber of Global Commerce
* red: commodity exchange

**Shortcut:** click a planet on a system map.

### STNS – Stations {#stns}

`STNS [station ID]`

Lists all space stations, or shows the public information and infrastructure of one station.

**Shortcut:** click a station (square symbol) on a system map or in `PLI`.

## Planetary projects

### PPS – Planetary projects {#pps}

`PPS <planet ID>`

Lists all planetary projects on a planet.

### PP – Planetary project {#pp}

`PP <planet ID> <project ID>`

Shows a planetary project. It's easier to open with the DETAILS button in `PPS`.

### PPI – Plot information {#ppi}

`PPI <plot ID>`

Shows information about a plot on a planet's surface.

### POPR – Population report {#popr}

`POPR <planet ID>`

Shows the population reports of a planet: the population's size, need satisfaction and growth.

### WAR – Warehouse {#war}

`WAR <planet or station ID>`

Shows public and private warehouse information, such as the available storage units and the rental fees.

## Infrastructure

See [infrastructure](../infrastructure) and [gateways](../infrastructure-gateway).

### INF – Infrastructure {#inf}

`INF [system ID]`

Lists the infrastructure of a system's planets, including planetary projects.

### INFU – Infrastructure upkeep {#infu}

`INFU <infrastructure ID>`

Shows the upkeep of an infrastructure: the materials required per weekly upkeep phase, the current phase and a history of past phases. See [infrastructure management](../infrastructure/#infrastructure-management).

### ASTS – Assets {#asts}

`ASTS`

Lists infrastructure projects under construction, owned infrastructure and constructed infrastructure. The list depends on the context: a company never owns infrastructure, a government never constructs it. See [assets](../infrastructure/#assets).

### GTW – Gateways {#gtw}

`GTW [system, planet or gateway ID]`

Lists all gateways, or only those in a system or at a planet, for example `GTW LS-300` or `GTW LS-300c`. With a gateway ID, shows the details of that gateway.

### GTWI – Gateway information {#gtwi}

`GTWI`

Plans new gateways and upgrades to existing ones. Shows the capacity, volume and distance of a configuration, its building or upgrade costs, the weekly upkeep and the systems in range. See [gateway design and construction](../infrastructure-gateway/#gateway-design-and-construction).

### GTWT – Gateway traffic {#gtwt}

`GTWT <gateway ID>`

Shows a gateway's traffic and fuel: jumps in the last 24 hours, the current capacity, the available fuel, the fuel contractors, and outgoing and incoming jumps per phase, including failed jumps and why they failed. See [gateway traffic](../infrastructure-gateway/#gateway-traffic).

## Politics

### ADM – Administration center {#adm}

`ADM <planet ID>`

Shows a planet's [administration center](../planetary-projects/#administration-center): the current governor, the faction or corporation collecting fees and taxes, and the candidates for the next term. Anyone can run for governor here, and planetary residents vote here.

### GOV – Government {#gov}

`GOV <planet ID>`

Shows a planet's current and previous governments and the motions they voted on.

### LR – Local rules {#lr}

`LR <planet ID>`

Shows the [local rules](../local-rules) of a planet with an administration center, such as production fees and local market fees.

### MOTS – Motions {#mots}

`MOTS [motion ID]`

Lists the motions of the currently active government context.

### MOT – Motion {#mot}

`MOT <administration center> <motion ID>`

Shows a motion with its components, current status and votes.

### POL – Political offices {#pol}

`POL [username]`

Shows the current and past political offices of a user, including current runs.

## Social

### FA – Faction {#fa}

`FA <faction code>`

Shows information about a faction.

### CO – Company {#co}

`CO <company code>`

Shows information about a company, including its owner, whom you can contact from here.

### USR – User {#usr}

`USR <username>`

Shows a user's company, registration date and online status. MUTE USER hides all their messages from you.

**Shortcut:** click the managing director in `CO`.

### BDGS – Badges {#bdgs}

`BDGS`

Lists all user badges and what they stand for.

### CONS – Users online {#cons}

`CONS`

Shows who is currently online in APEX.

**Shortcut:** the CONS button in the bottom right of APEX.

### COM – Channels {#com}

`COM`

Lists the channels you have joined. Opening a channel joins it. To leave, open the channel and select LEAVE.

### COMC – Channel catalog {#comc}

`COMC`

Lists all public channels. Select one to join it.

### COMP – Public channel {#comp}

`COMP <channel>`

Opens a public channel, such as "global" or "help". Public channels can't be created.

### COMG – Group chat {#comg}

`COMG <channel>`

Opens a private group chat. If it doesn't exist yet or you haven't joined it, "Start Conversation" opens it.

**Shortcut:** the NEW GROUP button in `COM`.

### COMU – Private chat {#comu}

`COMU <username>`

Starts a private conversation with a user.

**Shortcut:** the NEW PRIVATE button in `COM`.

## Notifications

### NOTS – Notifications {#nots}

`NOTS`

Lists your in-game notifications. Click one for details.

### NOTIG – In-game notification settings {#notig}

`NOTIG`

Sets which notifications show up in `NOTS`.

### NOTPNS – Push notification settings {#notpns}

`NOTPNS`

Sets which notifications are sent to you by email, and how often.

## Company and finances

### FIN – Finances {#fin}

`FIN`

Shows a financial overview and recent cash bookings.

### FINBS – Balance sheet {#finbs}

`FINBS`

Shows your assets and liabilities.

### FINIS – Income statement {#finis}

`FINIS`

Shows your profit and loss.

### FINLA – Liquid assets {#finla}

`FINLA`

Shows your liquid assets, such as cash.

### LEAD – Leaderboards {#lead}

`LEAD`

Shows company leaderboards. Choose the leaderboard at the top. Some have additional filters, such as a time range.

### ARC – APEX Representation Center {#arc}

`ARC`

Shows the level of your APEX Representation Center and lets you contribute funds to raise it.

### GIFT – Gift PRO license {#gift}

`GIFT`

Gifts PRO license time to other players and lists the gifts you sent and received.

### COLIQ – Liquidate company {#coliq}

`COLIQ`

Liquidates your company, so you can start over with the same account. Refresh APEX afterwards.

Cooldowns:

* the first liquidation is available right after company creation
* the second 3 days after the first
* the third 21 days after the second
* every further one 60 days after the previous one

An immediate liquidation may be possible if you haven't traded on a commodity exchange or local market and haven't contributed to planetary or corporation projects.

**Misusing `COLIQ` may get your account (temporarily) banned.**

## Interface and transmissions

### CS – Create screen {#cs}

`CS`

Creates a new screen, like the ADD button at the top. See the [interface guide](../../tutorials/current-tutorials/07-interface-guide).

### SCRN – Screens {#scrn}

`SCRN`

Lists your screens. Rename, copy or delete them, and manage screen variables.

### LIC – License {#lic}

`LIC`

Shows your current APEX license and when it expires. From here you can manage your license or gift PRO time to other players.

### TRA – Transmissions {#tra}

`TRA`

Lists all transmissions (video tutorials).

### XIT – Green screen {#xit}

`XIT [title]`

Shows a green screen for recording your own transmission, with an optional title.

### XYTV – YouTube video {#xytv}

`XYTV <video ID>`

Embeds a YouTube video. The ID is the part after `v=` in the video's URL.

{{% about-this-page %}}
