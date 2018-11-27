---
title: "Commands list"
date: 2018-09-18T17:13:49+02:00
weight: 9
draft: true
---

This is a comprehensive list of all commands available to you in APEX. They are grouped together by their respective areas of use. Understanding this list requires that you already be familiar with [how commands work](LINK). You may read through the whole list to gain an overview or use it as a reference to look up specific commands.

## Base commands

__BS__  
_Optional parameter: base ID_  
By itself shows an overview over all your bases. Shows more info on a concrete base when followed by a base ID, e.g. by clicking “View Base” in the generic BS window. Provides access to most other base-related commands.

__BSL__  
_Mandatory parameter: base ID_  
Opens a Sections overview of a concrete base. Accessible via the “Sections” button in a concrete BS window. Click “DEMOLISH” to destroy a Section, which will not give you any construction resources back as of yet.

__BSC__  
_Mandatory parameter: base ID_  
Opens the Construct window of a concrete base. Accessible via the “Construct” button in a concrete BS window. Use the tabs at the top to cycle through different building categories.

__BUI__  
_Mandatory parameter: building ticker_  
Displays information on a building type: which kind of worker is employed here, how much space the building takes up and which parts go into its construction. Accessible by clicking a building type in the BSC window.

__INV__  
_No possible parameter_  
Opens a list of all your inventories, not counting cargo holds on ships.

__INVP__  
_Mandatory parameter: planet ID_  
Opens the Inventory of the base on the specified planet. Accessible via the “Inventory” button in a concrete BS window or “Open Inventory” in the INV window.

__POP__  
_Mandatory parameter: base ID_  
Shows an overview over a base’s population and their needs. The more sophisticated the population tier, the higher their needs. If you can’t supply your workers with the consumables they need, the efficiency of buildings they operate will drop. Accessible via the “Population” button in a concrete BS window.

__EXP__  
_Mandatory parameter: base ID_  
Lists all fields which can receive bonuses by Experts and shows which Experts are currently being used in the specified base. Hit “REMOVE” to deactivate an expert, who is then listed as available in the rightmost column. Click “ACT” to send them back to work. Accessible via the “Experts” button in a concrete BS window. 
Production Line commands

__PROD__  
_Optional parameter: base ID_  
By itself shows an overview of all Production Lines your company owns. Followed by a base ID, it shows the Production Lines in a specific base. Accessible via the “Production” button in a concrete BS window. Each Production Line may consist of one or more buildings of the same type.

__PRODQ__  
_Mandatory parameter: Production Line ID_  
Allows you to cancel queued orders, but not the ones that are already being processed. The Efficiency value is influenced by multiple factors including your workers’ satisfaction, the bonus provided by Experts and, in some cases, the planet’s soil fertility. Accessible via the “Details” button in a PROD window.

__PRODCO__  
_Mandatory parameter: Production Line ID_  
Allows you to place a new Production order. Select a Primary Output from the dropdown menu, set an order size and queue your order. If your order requires input materials (as shown at the bottom), make sure they are available first. Accessible via the “New Order” button in a PROD window.

## Social commands

__CO__  
_Mandatory parameter: Company code_  
Displays information about the specified company. (This is where the four-digit code you chose for your company in very the beginning finds its use.) Among other things, allows to view and contact the company’s owner.

__USR__  
_Mandatory parameter: User name_  
Shows a user’s company, registration date, and connection status. Accessible via the “Managing Director” column in a CO window.

__COM__  
_No possible parameters_  
Lists all communication channels you have joined in the past. You automatically join a channel when first clicking on it. To leave a channel again, open it and select “LEAVE”.

__COMC__  
_No possible parameters_  
Lists all public communication channels. You can join a channel by selecting it from the list.

__COMG__  
_Mandatory parameter: channel ID_  
Opens a private group chat. If you previously joined it, entering its name will open the chat directly. If you enter the name of a room that does not exist yet or that you haven’t previously entered, “Start Conversation” will open the chat. Also accessible via the “NEW GROUP” button in the COM window.

__COMP__  
_Mandatory parameter: channel ID_  
Opens an existing public chat like “global” or “help”. You cannot create a new public chat.

__COMU__  
_Mandatory parameter: user name_  
Starts a private two-person conversation with the specified user. Start entering their name until it appears in the list, then click it. Accessible via the “NEW PRIVATE” button in the COM window.

__CONS__  
_No possible parameters_  
Shows you who is currently online in APEX. Accessible via the “CONS” button in the bottom right of APEX.

## Contract commands

__CONT__  
_Mandatory parameter: contract ID_  
This command allows you to view a specific contract. It must be followed up with a long and complex parameter identifying the contract, which is why it is generally recommended to use “CONTS” command and then clicking the desired contract(s).

__CONTS__  
_No possible parameter_  
Displays a list of all your contracts. Click any contract to open its CONT buffer. Note that you can also view Pending Contracts by selecting them from the list in the right sidebar. (If you can’t see the sidebar, toggle it on using the SDBR button on the left.) Learn more about contracts in the “Getting Started” tutorial.

## Commodity Exchange commands
These following commands all pertain to Commodity Exchanges. The first two are probably the most useful. See all these commands in action in the “Getting Started” tutorial.

__CXOS__  
_No possible parameter_  
Shows a history of your Sell and Buy orders, which you can view and delete from here. By deleting an order that hasn’t been filled yet, or at least not completely, you withdraw it from the market.

__CXO__  
_Mandatory parameter: Contract ID_  
Shows information on an order you made in the past. Accessible via the “VIEW” buttons in the CXOS window.

__CXL__  
_No possible parameter_  
Lists all existing Commodity Exchanges. From here, you can quickly access a concrete Commodity Exchange without having to remember its particular parameter for the CX command.

__CX__  
_Mandatory parameter: Commodity Exchange ID_  
This is where you can buy and sell items from a particular market. Select the commodity category from the dropdown menu. Accessible for example by clicking the name of a commodity exchange in the CXL window.

__MAT__  
_Mandatory parameter: material ID_  
Materials and commodities are essentially the same thing. Their ticker is the two- or three-letter identifier you can see in each of their little icons. For example, the ticker for Steel is STL. “Wrought product” indicates what can be made from this material and in which Production Line, while “Production” shows you how and where the material itself can be produced. Accessible for example by clicking a commodity’s icon in the CX window.

__CXP, CXPC, CXOB, CXPO__  
_Mandatory parameter: commodity ID + ComEx ID_  
These four commands relate to concrete commodities on a concrete market. Next to an entry of a commodity in the CX window, you’ll find the buttons labeled “INFO”, “CHART”, “ORDERS”, and “TRADE”.
“INFO”: CXP, which shows an overview over current bids, ask amounts, all-time highs and lows etc.
“CHART”: CXPC. Shows a candlestick chart of a commodity’s price over time. If it says “No data”, the commodity hasn’t been sold in the indicated time period. Select a longer time window to fix it.
“ORDERS”: CXOB command, where you can see pending requests and offers.
“TRADE”: CXPO, which lets you place Buy and Sell Orders.

## Space flight commands
It is recommended you use the FLT command and access the other commands from there. To see all these commands in action, have a look at the space-flight tutorial.

__FLT__  
_Optional parameter: system ID / planet ID_  
Entered by itself, the Fleet command shows all of your ships. Every line shows data on one of your ships, like its transponder code, name, status, fill status, location, and information about an ongoing flight. Following up the fleet command with the ID of a system or planet shows all of your ships currently stationed there. (The ID is simply the parameter you can see at the top of a buffer by selecting a system in the Universe Map or a planet in a system map.)

__SHP__
_Mandatory parameter: ship transponder code_
Shows information on one of your ships. Rename your ship by clicking its current name (or “unnamed”) and entering a new one.
Accessible by clicking the Transponder code of a ship in the FLT window.

__SHPF__
_Mandatory parameter: ship transponder code_
Shows a ship’s fuel status. Accessible by clicking the fuel bar of a ship in the FLT window.

__SHPI__
_Mandatory parameter: ship transponder code_
Shows a ship’s inventory, which is limited in the weight and volume of its cargo. Accessible by clicking the inventory bar of a ship in the FLT window.


__SFC__  
_Mandatory parameter: ship transponder code_  
The “FLY” button next to each ship in the FLT list calls the SFC command followed by the ship’s transponder code. By entering a planet ID or station ID into the Location property, setting the desired Fuel usage and hitting Start, you can send a ship to a new destination.

__SI__
_Mandatory parameter: ship transponder code_
Shows all the public information available on the selected ship. Accessible by clicking a ship triangle in a System map or Planet Info window.


## Foreign Exchange commands
To see these commands in action, have a look at the “Foreign Exchange” tutorial.

__FX__  
_No possible parameter_  
FX shows you a matrix of exchange rates where you can see how much one currency is worth in terms of another. The base currencies are arranged vertically, the quote currencies horizontally.

__FXP__  
_Mandatory parameter: commodity pair ticker_  
Use FXP followed by a ticker of two currency identifiers divided by a slash or dot, for example: FXP AIC/CIS. Alternatively, just click the respective value in the FX matrix.

__FXOB__  
_Mandatory parameter: commodity pair ticker_  
Use this command to see open orders of any currency pair, for example: FXOB AIC/CIS.

__FXPC__  
_Mandatory parameter: commodity pair ticker_  
Shows the exchange rate history of any currency pair, for example: FXPC AIC/CIS.

__FXPO__  
_Mandatory parameter: commodity pair ticker_  
Use this command to place a foreign exchange order, that is, to spend one currency to buy another. Enter FXPO followed by the desired ticker, for instance AIC/NCC. Note that the order of the two matters; a buy order for currency A which you pay for in currency B is not the equivalent of a sell order for currency B which you pay in currency A. If this confuses you, have a look at the Foreign Exchange tutorial. To place a ForEx order, select the number of Lots - which is a thousand units - you want to buy and indicate the number of Lots you’re willing to spend.

__FXOS__  
_No possible parameter_  
Shows all foreign exchange orders you placed.

## Map commands
Maps can be navigated by dragging and dropping the left mouse button to move around and the right mouse button to rotate. Some maps can be displayed in 2D instead of 3D by toggling on the “Fix 2D” property.

__MU__  
_Mandatory parameter: CX/NAV/INV/POL_  
Opens one of the four different Universe maps. They all show the same Universe, but they serve different purposes, as described below. The interconnected dots on the map are star systems. By hovering over a system, you can see its identifier. Throughout all maps, you can toggle the display of different types of information on or off at the bottom. You may also filter that data by time period (e.g. 1 hours, 12 hours, 24 hours).
MU CX: Shows where your commodity exchanges are taking place.
MU NAV: Shows traffic data. As long as “fleet” is toggled on, your ships’ locations are marked by yellow arrows. Learn more about traffic data in the “Space Flight” tutorial.
MU INV: Allows you to view the distribution of your storage in the universe.
MU POL: Shows a political map. This is not yet available.

__MS__  
_Mandatory parameter: system ID_  
Like on the Universe Map, yellow arrows mark your ships. Turn on “traffic” to also see the location of other users’ ships, which are marked by white arrows. The wireframe structure in the middle is the system’s star; the circles orbiting it are either rocky (white) or gaseous (orange) planets. White square represent space stations. Hovering over a planet or space station shows its ID. Instead of manually entering the system ID, you may click on the desired system in the Universe map.

__PLI__  
_Mandatory parameter: planet ID_  
All planets, named or unnamed, have an ID, which is the system’s ID followed by a unique letter. Planet Info contains shortcuts to your Fleet and Inventory on that planet. Among other things, you can see here which Resources can be extracted from this planet and its atmosphere, and whether or not the planet lends itself to growing plants. The bar indicating the latter starts in the middle, and the further it extends to the left or right, the more infertile or fertile the planet is respectively. Finally, the Type and Temperature indicate whether you’re going to need additional Construction Materials to set up a base on this planet. Building on a gaseous planet requires Aerostat Foundation. Planets colder than minus twenty-five degrees Celcius or warmer than seventy-five degrees Celcius need to be fitted with a Climate Control Unit and InsuFoam. The amount of InsuFoam required depends on the building’s Area Cost. Additionally, buildings on hot planets require thermal shielding.
Instead of entering the ID by hand, you may also click the planet directly in the System map.

__STI__
_Obligatory parameter: Station ID_
Shows general information about a space station and provides access to its  Accessible by clicking a station (square symbol) on a System map or in a Planet Info window.


## Planetary project commands

__PPS__  
_Mandatory parameter: planet ID_  
Shows all planetary projects on the desired planet.

__PP__  
_Mandatory parameter: planet & project ID_  
Shows information on a concrete planetary project. Due to the long and complex parameter, it is recommended to access this information via the “details” button next to the desired project in the PPS buffer.

## Transmission commands

__TRA__  
_No possible parameter_  
Brings up a list with all transmissions, i.e. video tutorials.

__XIT__  
_Optional parameter: title_  
Brings up a green screen to help you record your own transmission. Use the optional parameter to give it a title.

__XYTV__  
_Mandatory parameter:_  
Embeds a YouTube video. The ID is the succession of numbers and letters after “v=” in the video’s URL. Please note that this works only with official transmissions listed in the TRA window for now, although there are plans to allow for external content in the future.


## Other commands

__CS__  
_No possible parameter_  
Allows you to create a new Screen. To call this command, you may use the “ADD” button at the top. Learn all about Screens in the APEX interface tutorial.

__FIN, FINLA, FINIS, FINBS__  
These four commands provide you with a detailed overview over your company’s financial situation. More information on these commands will follow shortly.


## More tutorials

If you are first starting out, check out the “APEX overview” and “Getting started” tutorials:  
* [APEX overview](LINK)  
* [Getting started](LINK)  
* [Space flight](LINK)  
* [Foreign Exchange](LINK)  
* More to come!

Use the arrows on the sides to cycle through all available tutorials in order, from introductory to more and more specific topics.