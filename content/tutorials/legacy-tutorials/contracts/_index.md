---
title: "2.4 Contracts"
date: 2018-09-18T17:13:49+02:00
weight: 5
---

This guide is also available in video format. __Click below to watch the video or scroll down for the written version.__

{{< youtube X-du1P3KfXY >}}

### Contracts

If the commodities you bought are in none of your inventories yet, you now have to go and get them. This happens when neither your base nor any of your ships are currently at the location where you made the purchase. The moment you made your first purchase, a contract popped up in the sidebar. (If you cannot see the sidebar, you can toggle it on by clicking “SDBR” on the left.) Click a contract ID to see more information.

![Contract](pending-contract.png)

Alternatively, you can open a list of your contracts by using the “CONTS” command. Next, click “view” to open the details of a contract, and you will see that the units you ordered have been paid, reserved for you and are awaiting pick-up. The button labeled “Fulfill” is greyed out because you have no ship at the location to pick the cargo up with, so you have to send one.

You are now going to learn the exact steps required to pick up your cargo. For more extensive information on the subject of space travel, check out the [Space flight tutorial](../space-flight). If your Fleet window is not open yet, bring it up now using the FLT command shortcut in the left sidebar, then open one of your ships’ cargo holds by clicking its cargo space. Note that a ship’s cargo space is limited, and for bigger purchases it might be necessary to send multiple ships. Your cargo hold is limited by the available space (in cubic meters) and maximum weight (in tonnes) of its contents.

![Cargo space](ship-cargo.gif)

In the Contract buffer that opens up, you can see the target planet’s ID:

![Pending contract](pending-contract.gif)

Now hit the “FLY” button next to the desired ship's entry in the Fleet window to bring up the Ship Flight Control. Copy the target planet's ID into the Flight Control’s Destination field. Next, make sure to toggle on “Planetary landing” (if your target is a planet and not a station) before you set the fuel usage. The higher the fuel usage, the sooner your spacecraft will arrive, but setting it to 100 % means that it won’t have a drop of fuel left to return home and the trip would be unreasonably expensive. Note that, depending on the distance of your trip, you may not be able to spend 100 % of your fuel.

![Flying to contract](flying-to-contract.gif)

In any case, the flight will take several hours during which you cannot do anything but wait. Your ship’s position is tracked in the System Map and Universe Map as a yellow triangle. If you do not see it, toggle on “fleet” in the bottom right corner.

![Ship in system](ship-in-system.png)

![Ship in universe](ship-in-universe.png)

Once your ship has arrived, the Fulfill buttons of the active contracts you have at your target location will turn green. If they don’t, the reason might be that the target market is on the planet surface and your ship is still in orbit.

![Orbiting ship](orbiting-ship.png)

To fix that, select the ship’s FLY button in the Fleet window again, enter the ID of the planet it is orbiting, check “Planetary landing” and select “START” once more.

![Surface landing](surface-landing.png)

By now, the “Fulfill” buttons on the active contracts you have on that market should have turned green. Click them to load up your ship with the goods you purchased. Before you send your ship back home, make sure to also buy any input materials while your ships are still at the market. You can learn which input materials to buy in the [Production tutorial](../production)

Once you have all your wares, have your ship return to your base. If you do not know your home planet's ID, click the BS command shortcut on the left. You will find the ID listed under “Planet”. Once it arrives back home, make sure to drag and drop the materials you purchased from its cargo space into your Base’s inventory.

![Fulfill contract](fulfill-contract.png)


## About this page

This page is part of the introductory tutorial, which encompasses parts 1 and 2 (2.1-2.5). Use the arrows on the sides to cycle through all available tutorials in order, from introductory to more and more specific topics.

If you encounter an error or cannot find the answers to your questions, we will gladly help you on our [Discord server](https://discordapp.com/invite/G7gj7PT).