---
title: "Commands list"
date: 2018-09-18T17:13:49+02:00
weight: 2
---

This is a comprehensive list of all commands available to you in APEX. They are grouped together by their respective areas of use. Understanding this list requires that you already be familiar with [how commands work](../../tutorials/commands). You may read through the whole list to gain an overview or use it as a reference to look up specific commands.

## Base commands

__BS__  
_Optional parameter: base ID_  
By itself shows an overview over all your bases. Shows more info on a concrete base when followed by a base ID, e.g. by clicking “View Base” in the generic BS window. Provides access to most other base-related commands.

__BSC__  
_Mandatory parameter: planet ID_  
Allows to create a new base on a planet. It shows necessary building materials and allows to select a plot on the surface. 

__BSL__  
_Mandatory parameter: base ID_  
Opens an overview over the buildings in a concrete base. Accessible via the BUILDINGS (formerly “SECTIONS”) button in a concrete BS window. Click “DEMOLISH” to destroy a Section, which will refund some of the resources that went into its construction, depending on its age. The possible refunded materials are listed as “Reclaimable materials”.

__BSC__  
_Mandatory parameter: base ID_  
Opens the Construct window of a concrete base. Accessible via the “Construct” button in a concrete BS window. Use the tabs at the top to cycle through different building categories. The line labeled “Area” indicates a building's area cost and, after the slash, the area left available in your base. The line labeled Workforce” shows the number and type of workforce required to operate this building.

__BUI__  
_Mandatory parameter: building ticker_  
Displays information on a building type: which kind of worker is employed here, how much space the building takes up and which parts go into its construction. Accessible by clicking a building type in the BSC window.

__INV__  
_Optional parameter: address or store ID_  
If no parameters are supplied the command will show a list of all your inventories, including base storage, cargo holds, fuel tanks and warehouse storage units. Clicking on the "open" button will show the contents of the selected inventory. In the top left, you will find several sorting options (AMT: amount, WGT: weight, VOL: volume) as well as a symbol to their left. Click it to toggle between list and grid mode; the latter shows more information on each commodity, such as their weight, volume, and book value.

If the parameter contains a system or planet address (for example `INV XK-745` or `INV XK-745a`) it will only show inventories at that location.

__MTRA__  
_Optional parameter: material ticker_  
_Optional parameter: source store ID_  
_Optional parameter: target store ID_  
Allows you to transfer a specific amount of items between two inventories. The material to be transferred as well as the source and target stores can be specified via the command's parameters or chosen from drop-down menus in the command window itself. Note that this command is also accessible (with pre-filled transfer details) via dragging an item from the source store to the target store and dropping it on the “AMT” slot.

__WF__  
_Mandatory parameter: base ID_  
Shows an overview over a base’s workforce and their needs. The more sophisticated the workforce tier, the higher their needs. If you can’t supply your workers with the consumables they need, the efficiency of buildings they operate will drop. Accessible via the “Workforce” button in a concrete BS window.

__EXP__  
_Mandatory parameter: base ID_  
Lists all fields which can receive bonuses by Experts and shows which Experts are currently being used in the specified base. Hit “REMOVE” to deactivate an expert, who is then listed as available in the rightmost column. Click “ACT” to send them back to work. Accessible via the “Experts” button in a concrete BS window. 
Production Line commands

__PROD__  
_Mandatory parameter: base ID_  
Shows the Production Lines in a specific base. Accessible via the “Production” button in a concrete BS window. Each Production Line may consist of one or more buildings of the same type.

__PRODQ__  
_Mandatory parameter: Production Line ID_  
Allows you to cancel queued orders, but not the ones that are already being processed. The Efficiency value is influenced by multiple factors including your workers’ satisfaction, the bonus provided by Experts and, in some cases, the planet’s soil fertility. Accessible via the “Details” button in a PROD window.

__PRODCO__  
_Mandatory parameter: Production Line ID_  
Allows you to place a new Production order. Select a Primary Output from the dropdown menu, set an order size and queue your order. If your order requires input materials (as shown at the bottom), make sure they are available first. Accessible via the “New Order” button in a PROD window.

__HQ__  
_No possible parameter_  
Shows you which of your bases currently is your company headquarters and allows you to relocate your headquarters to another base for different [faction bonuses](../headquarters). You can also upgrade your headquarters here to unlock additional base permits and production queue slots.

__BRA__  
_Optional parameter: planet ID_
Allows you to select one of your bases and repair multiple of its buildings at once by specifying a minimum building condition. All buildings in the selected base at or below that condition will be included in the repairs.

## Social commands

__FA__  
_Mandatory parameter: Faction code_  
Displays information about the specified faction.

__CO__  
_Mandatory parameter: Company code_  
Displays information about the specified company. (This is where the four-digit code you chose for your company in very the beginning finds its use.) Among other things, allows to view and contact the company’s owner.

__USR__  
_Mandatory parameter: User name_  
Shows a user’s company, registration date, and connection status. Accessible via the “Managing Director” column in a CO window. Clicking the “MUTE USER” button renders all messages this user sends invisible to you.

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
Displays a list of all your contracts from Commodity Exchanges and Local Markets. Click any contract to open its CONT buffer. Note that you can also view Pending Contracts by selecting them from the list in the right sidebar. (If you can’t see the sidebar, toggle it on using the SDBR button on the left.) Learn more about contracts in the “Trading” and “Local Markets” tutorials.

__CONTD__
_Optional parameter: contract ID_
Displays a list of all your contract drafts. Specifying a contract id, or clicking on any draft, will open the draft detail view, where the draft can be edited and sent out.

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

__CXM__  
_Mandatory parameter: material ticker_  
_Optional parameter: planet ID_  
Compares commodity exchange information for the specified material across _all_ commodity exchanges. Exchanges will be sorted by their distance to the given planet (if one was entered).

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
“TRADE”: CXPO, which lets you place Buy and Sell Orders within the current Price Band. The latter is determined by a three-day average and is wider for PRO licensees than FREE licensees. To quickly set the current lowest bid or asking price, use the “set” buttons in the “Ask / Bid” line. The “Inventory” line lets you select the storage location from which to sell your commodities.

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

## Ship building commands

__BLU__
_Optional parameter: blueprint ID_
Opens a list of all your ship blueprints or a specific blueprint if an ID was specified.

__SHY__
_Mandatory parameter: planet ID_
Opens the shipyard buffer of the desired planet.

__SHYP__
_Mandatory parameter: project ID_
Opens the desired shipbuilding project.

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
Use this command to place a foreign exchange order, i.e. to spend one currency to buy another. Enter FXPO followed by the desired ticker, for instance AIC/NCC. Next, select the appropriate tab in order to buy or sell the desired currency. Note that the numbers you indicate are Lots, that is, 1000 of each currency. For more in-depth information, have a look at the [Foreign Exchange tutorial](../../tutorials/foreign-exchange).

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

MU INV: Allows you to view the distribution of your storage in the universe. This is not yet available.

MU POL: Shows a political map. This is not yet available.

__MS__  
_Mandatory parameter: system ID_  
Like on the Universe Map, yellow arrows mark your ships. Turn on “traffic” to also see the location of other users’ ships, which are marked by white arrows. The wireframe structure in the middle is the system’s star; the circles orbiting it are either rocky (white) or gaseous (orange) planets. White square represent space stations. Hovering over a planet or space station shows its ID. Instead of manually entering the system ID, you may click on the desired system in the Universe map.

__SYSI__
_Optional parameter: system ID_
All systems, named or unnamed, have and ID which consists of the sector ID (two letters) and the system number. The system information commands shows basic information about the system, like its name, star type, micrometeoroid density and faction affinity. It has a list of all planets and stations in that system.
If no system ID is provided a search box is being displayed instead of the system data which allows to search for systems.

__PLI__
_Optional parameter: planet ID_
All planets, named or unnamed, have an ID, which is the system’s ID followed by a unique letter. Planet Info contains shortcuts to your Fleet and Inventory on that planet. Among other things, you can see here which Resources can be extracted from this planet and its atmosphere, and whether or not the planet lends itself to growing plants. The bar indicating the latter starts in the middle, and the further it extends to the left or right, the more infertile or fertile the planet is respectively. Finally, the Type and Temperature indicate whether you are going to need [additional Construction Materials](../building-costs) to set up a base on this planet.
Each non-grey plot on a planet can be clicked to obtain more information about it. The following colors exist as of yet: blue (other companies), dark blue (other Corp.'s project), yellow (own company), dark yellow (own Corp.'s project), green (CoGC), red (commodity exchange)
Instead of entering the planet ID by hand, you may also click the planet directly in the System map to access its PLI window.
If no planet ID is provided a search box is being displayed instead of the planet data which allows to search for planets.

__STI__  
_Mandatory parameter: Station ID_  
Shows general information about a space station and provides access to its infrastructure. Accessible by clicking a station (square symbol) on a System map or in a Planet Info window.

## Planetary project commands

__PPS__  
_Mandatory parameter: planet ID_  
Shows all planetary projects on the desired planet.

__PP__  
_Mandatory parameter: planet & project ID_  
Shows information on a concrete planetary project. Due to the long and complex parameter, it is recommended to access this information via the “details” button next to the desired project in the PPS buffer.

__PPI__
_Mandatory parameter: planet_
Shows information about a plot on the planet's surface.

__POPR__
_Mandatory parameter: planet ID_   
Shows the population reports of the specified planet with information on the planetary population's size, need satisfaction and growth.

### Local Market commands

__LMOS__
_No possible parameter_  
Shows all your Local Market Ads.

__LM__
_Mandatory parameter: Planet ID_  
Shows all available Ads at a given Local Market. Accessible by clicking the Infrastructure entry “Local Market” (if existant) in any PLI window.

__LMA__
_Mandatory parameter: Ad ID_  
Shows the details of the specified Local Market ad. Accessible by selecting an ad in the LM window.

__LMP__
_Mandatory parameter: Planet ID_  
Allows placing a Buying Ad or Selling Ad at a given Local Market. Accessible via the “POST AD” button in an LM window.

### Political commands

__ADM__
_Mandatory parameter: Planet ID_  
Shows information on the planet's [Administration Center](../../tutorials/planetary-projects/#administration-center) (if there is one), such as the current Governor, the entity (i.e. Faction or Corporation) collecting fees and taxes, and all candidates for the upcoming term. Allows anyone to run for Governor of the planet and planetary residents to vote for their preferred candidate.

__GOV__
_Mandatory parameter: Planet ID_
Shows information on a planet's current and previous governments and the motions that were voted on.

__LR__
_Mandatory parameter: Planet ID_  
Shows the Local Rules of a planet, given that it has an Administration Center. Local Rules include taxes on production as well as fees for Local Market ads.

__POL__
_Optional parameter: User name_
Shows the current and past political offices held by a user, including current runs.

### Warehouse commands

__WAR__
_Mandatory parameter: Planet ID_  
Shows public and private warehouse information like the amount of available storage units, the rental fees and so on.

## Notification commands

__NOTS__
_No possible parameter_  
Displays a list of in-game notifications. Click a notification to get more information.

__NOTIG__
_No possible paramter_  
Allows you to change your in-game notification settings. Disabled types of notifications will not show up in the `NOTS` command.

__NOTPNS__
_No possible parameter_  
Allows you to change your push notification settings. Choose which types of notifications should be sent to you via email and in which frequency.

## Transmission commands

__TRA__  
_No possible parameter_  
Brings up a list with all transmissions, i.e. video tutorials.

__XIT__  
_Optional parameter: title_  
Brings up a green screen to help you record your own transmission. Use the optional parameter to give it a title.

__XYTV__  
_Mandatory parameter:_ YouTube ID  
Embeds a YouTube video. The ID is the succession of numbers and letters after “v=” in the video’s URL.

## Other commands

__ARC__  
_No possible parameter_  
Shows the current status of your APEX Representation Center and allows you to contribute funds towards raising its level.

__COLIQ__  
_No possible parameter_  
Allows you to liquidate your company. It will be scrapped and you get to start over entirely with the same account. Refresh APEX after using it. The following cooldown times apply to the COLIQ command: The first COLIQ becomes available immediately after company creation, the second one 3 days after using the first one. The wait time for the third COLIQ is 21 days, and every following cooldown is 60 days long. If there have not been any commodity or local market trades and no contributions to planetary or corporation projects an immediate COLIQ might be possible. Please note that misusing the COLIQ command may result in your account being (temporarily) banned!

__CS__  
_No possible parameter_  
Allows you to create a new Screen. To call this command, you may use the “ADD” button at the top. Learn all about Screens in the APEX interface tutorial.

__FIN, FINLA, FINIS, FINBS__  
These four commands provide you with a detailed overview over your company’s financial situation. More information on these commands will follow shortly.

__LEAD__  
_No possible parameter_  
Shows company-level leaderboards. The type of leaderboard can be chosen from a dropdown menu at the top. Some leaderboards support additional selectors (such as specifying the data's time range).

{{% about-this-page %}}