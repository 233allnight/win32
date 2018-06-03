---
title: CLUSCTL\_NETINTERFACE\_GET\_NETWORK control code
description: Retrieves the name of the network to which a network interface is connected.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 13dd855d-1e52-466c-8709-5d6a5fd8e73c
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- CLUSCTL_NETINTERFACE_GET_NETWORK control code Failover Cluster
topic_type:
- apiref
api_name:
- CLUSCTL_NETINTERFACE_GET_NETWORK
api_location:
- ClusAPI.h
api_type:
- HeaderDef
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# CLUSCTL\_NETINTERFACE\_GET\_NETWORK control code

Retrieves the name of the [network](networks.md) to which a [network interface](network-interfaces.md) is connected. Applications use this [control code](about-control-codes.md) as a [**ClusterNetInterfaceControl**](/previous-versions/windows/desktop/api/ClusAPI/nf-clusapi-clusternetinterfacecontrol) parameter.


```C++
ClusterNetInterfaceControl( 
  hNetInterface,                     // network interface handle
  hHostNode,                         // optional host node
  CLUSCTL_NETINTERFACE_GET_NETWORK,  // this control code
  NULL,                              // input buffer (not used)
  0,                                 // input buffer size (not used)
  lpOutBuffer,                       // output buffer: string
  cbOutBufferSize,                   // allocated buffer size (bytes)
  lpcbBytesReturned                // actual size of resulting data (bytes)
);
```



## Parameters

The following control code function parameter is specific to this control code. For complete parameter descriptions, see [**ClusterNetInterfaceControl**](/previous-versions/windows/desktop/api/ClusAPI/nf-clusapi-clusternetinterfacecontrol).

<dl> <dt>

*lpOutBuffer* 
</dt> <dd>

On a successful return, points to a null-terminated Unicode string containing the name of the network interface.

</dd> </dl>

## Return value

[**ClusterNetInterfaceControl**](/previous-versions/windows/desktop/api/ClusAPI/nf-clusapi-clusternetinterfacecontrol) returns one of the following values.

<dl> <dt>

**ERROR\_SUCCESS**
</dt> <dd>

0

The operation completed successfully. The *lpcbBytesReturned* parameter points to the actual size of the returned data.

</dd> <dt>

**ERROR\_MORE\_DATA**
</dt> <dd>

234 (0xEA)

More data is available. The output buffer pointed to by *lpOutBuffer* was not large enough to hold the data resulting from the operation. The *lpcbBytesReturned* parameter points to the size required for the output buffer.

</dd> <dt>

**[System error code](https://msdn.microsoft.com/library/windows/desktop/ms681381)**
</dt> <dd>

If any other value is returned, then the operation failed. The value of *lpcbBytesReturned* is unreliable.

</dd> </dl>

## Remarks

The network name is stored in the network interface [**Network**](network-interfaces-network.md) property. To retrieve the **Network** property along with the other read-only [network interface common properties](network-interface-common-properties.md), use the [CLUSCTL\_NETINTERFACE\_GET\_RO\_COMMON\_PROPERTIES](clusctl-netinterface-get-ro-common-properties.md) control code.

ClusAPI.h defines the 32 bits of CLUSCTL\_NETINTERFACE\_GET\_NETWORK as follows (for more information, see [Control Code Architecture](control-code-architecture.md)).



| Component      | Bit location | Value                                           |
|----------------|--------------|-------------------------------------------------|
| Object code    | 24 31        | **CLUS\_OBJECT\_NETINTERFACE** (0x6)<br/> |
| Global bit     | 23           | **CLUS\_NOT\_GLOBAL** (0x0)<br/>          |
| Modify bit     | 22           | **CLUS\_NO\_MODIFY** (0x0)<br/>           |
| User bit       | 21           | **CLCTL\_CLUSTER\_BASE** (0x0)<br/>       |
| Type bit       | 20           | External (0x0)<br/>                       |
| Operation code | 0 23         | **CLCTL\_GET\_NETWORK** (0x35)<br/>       |
| Access code    | 0 1          | **CLUS\_ACCESS\_READ** (0x1)<br/>         |



 

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                            |
| Minimum supported server<br/> | Windows Server 2008 Enterprise, Windows Server 2008 Datacenter<br/>            |
| Header<br/>                   | <dl> <dt>ClusAPI.h</dt> </dl> |



## See also

<dl> <dt>

[Network Interface Control Codes](network-interface-control-codes.md)
</dt> <dt>

[CLUSCTL\_NETINTERFACE\_GET\_RO\_COMMON\_PROPERTIES](clusctl-netinterface-get-ro-common-properties.md)
</dt> <dt>

[**ClusterNetInterfaceControl**](/previous-versions/windows/desktop/api/ClusAPI/nf-clusapi-clusternetinterfacecontrol)
</dt> </dl>

 

 




