---
title: Changing Interface-Specific and Global Information for Clients
description: To change the interface information for a specific client, for example NAT, first use the appropriate \ 0034;GetInfo \ 0034; function to retrieve the current information.
ms.assetid: '208e356b-328e-416d-881c-732fed460ebf'
---

# Changing Interface-Specific and Global Information for Clients

To change the interface information for a specific client, for example NAT, first use the appropriate "GetInfo" function to retrieve the current information. If the router is running, use [**MprAdminInterfaceTransportGetInfo**](mpradmininterfacetransportgetinfo.md). If the router is not running, use the [**MprConfigInterfaceTransportGetInfo**](mprconfiginterfacetransportgetinfo.md). This call retrieves the information for all the clients running on the specified interface. For example, if both OSPF and RIP are running on a particular interface, this call retrieves the interface information for both. Use the [**MprInfoBlockFind**](mprinfoblockfind.md) function to locate the information block that corresponds to the client you want to modify. Then use the [**MprInfoBlockSet**](mprinfoblockset.md) function to perform the modifications. Lastly, use [**MprAdminInterfaceTransportSetInfo**](mpradmininterfacetransportsetinfo.md) or [**MprConfigInterfaceSetInfo**](mprconfiginterfacesetinfo.md) to make the changes to either the running router or the router configuration in the registry.

Global client information is information that is not specific to any particular interface on which the client is running. Use a similar procedure to modify global information for a specific client. First retrieve the global information for all the clients using [**MprAdminTransportGetInfo**](mpradmintransportgetinfo.md) or [**MprConfigTransportGetInfo**](mprconfigtransportgetinfo.md). Then use the MprInfo functions to modify the information. Lastly, use the [**MprAdminTransportSetInfo**](mpradmintransportsetinfo.md) or [**MprConfigTransportSetInfo**](mprconfigtransportsetinfo.md) functions to save the modified information back to either the running router or the registry.

Calls to the preceding administration functions go through the Dynamic Interface Manager (DIM), and eventually translate into calls from the router manager to the clients themselves. All clients, whether or not they are routing protocols, must conform to the interface described in the section [Router Protocol Interface](about-routing-protocol-interface.md). As part of this interface, the routing protocol must support the following functions (among others):

-   [**GetGlobalInfo**](getglobalinfo.md)
-   [**SetGlobalInfo**](setglobalinfo.md)
-   [**GetInterfaceInfo**](getinterfaceinfo.md)
-   [**SetInterfaceInfo**](setinterfaceinfo.md)

The router manager calls the [**GetInterfaceInfo**](getinterfaceinfo.md) functions for each of the clients to gather the information that is returned from a call to [**MprAdminInterfaceTransportGetInfo**](mpradmininterfacetransportgetinfo.md). Similarly, when the router manager receives updated information via [**MprAdminInterfaceTransportSetInfo**](mpradmininterfacetransportsetinfo.md) call, it uses the [**SetInterfaceInfo**](setinterfaceinfo.md) functions to update the interface information for each of the clients.

 

 



