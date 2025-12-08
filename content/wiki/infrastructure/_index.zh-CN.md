---
title: Infrastructure
date: 2025-11-06T17:00:49+02:00
---

{{% notice style="secondary" title="Note" %}}
This article is a preview of the upcoming gateway release.
{{% /notice %}}

## General information

Infrastructure projects are large, planetary projects that are being initiated by a planetary government. They are constructed and operated by individual companies via specialized contractor contracts offered by the government.

So far the only type of infrastructure is [gateways](../infrastructure-gateway).

A planet's infrastructure is listed in the `PLI` and `INF` commands. Please note that `INF` also shows planetary projects.

![Infrastructure List](./infrastructure-list.png)

## Infrastructure Construction

Infrastructure can only be built by a planetary government. There are a variety of infrastructure-related motion components, and the one to build any infrastructure is "Infrastructure construction".

![Infrastructure Construction](./infrastructure-construction.png)

The following describes the typical steps to build an infrastructure.

First, the "Infrastructure construction" motion has to be filled out. It specifies the payment the constructor will receive for their services. It also allows setting a deadline until which the construction has to be finished. The constructor can be any user.

![Infrastructure Construction Motion](./infrastructure-construction-motion.png)

Once the motion has been successfully voted upon, a new contract between the government and the constructor's company is formed. The constructor can choose to accept/close the contract or reject it if they received it in error.

![Infrastructure Construction Contract](./infrastructure-construction-contract.png)

The contract consists of three parts. First, the contractor's payment. Second, a contract condition that starts the construction process. This condition has to be fulfilled by the constructor. Upon its fulfillment, the infrastructure project is started at the given location and a construction store is created. Lastly, once all construction materials have been delivered to the construction site, the last condition fulfills automatically and the infrastructure is complete.

![Infrastructure Construction Store](./infrastructure-construction-store.png)

Please note that all infrastructures that are located in orbit have their own addresses. That means that flying to a planet's orbit is not enough to transfer construction materials, for example. The ships have to be directed to the specific infrastructure or construction site.

## Infrastructure Management

Most infrastructures require weekly upkeep to be operational. The `INFU` (infrastructure upkeep) command provides an overview of all upkeep-related information.

![Infrastructure Upkeep](./infrastructure-upkeep.png)

It shows which and how many materials are required per weekly upkeep phase, information about the current upkeep phase and a history of the last upkeep phases.

The infrastructure's operational state will switch from "upkeep missing" to "operational" once all required materials have been transferred to the upkeep store. The upkeep store can hold upkeep materials for three upkeep phases. To gain access to the upkeep store, a contractor has to be appointed via a motion. Only these contractors can access the upkeep store.

![Infrastructure Upkeep Motion](./infrastructure-upkeep-motion.png)

In the motion editor various parameters can be selected. It defines the phase in which the upkeep contract should start and for how many phases it should run. It also allows specifying the contractor and the payment per phase. The service level objective defines the minimum ratio of the infrastructure being operational versus in "upkeep missing" state.

For example, if the service level is defined to be 50% and the contractor provides the necessary upkeep materials on the fifth day of the upkeep phase, the contract condition will be violated, as the infrastructure has been in "upkeep missing" state for ~71%.

It is possible to have multiple contractors for the same upkeep phase.

## Infrastructure Upgrades

Some infrastructures can be upgraded. The motion's selection depends on the type of the infrastructure. Here is an example of a gateway upgrade:

![Infrastructure Upgrade Motion](./infrastructure-upgrade.png)

Once the motion passes, a contract with the specified contractor is formed. Once the contractor accepts the contract, they will gain access to a construction store, similarly as to the infrastructure construction contract.

The infrastructure remains operational during the upgrade process.

## Infrastructure Naming

It is possible to give any infrastructure a name. Again, this is possible via a motion. There is no limit on how often the name of an infrastructure can be changed.

## Assets

The `ASTS` (Assets) command provides an overview of infrastructure projects in their various stages. It lists infrastructure projects that are under construction, owned infrastructure (i.e., finished projects) and constructed projects. The command is available in the company and government contexts, and its content is adjusted accordingly: a company can never have an entry in the "Own" subsection, a government cannot construct infrastructure directly, thus the "Constructed" subsection will be empty.

The command will also show helpful links to the respective construction stores in the "Under construction" section.

![Assets command](./assets.png)