---
title: Create a Query Object
description: Create a Query Object
ms.assetid: 100d5ac7-2701-4dfd-a4eb-28003ab3771e
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Create a Query Object

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/library/windows/desktop/aa965362) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

This code segment creates objQ, a Query object, as a new ActiveXObject object from Ixsso.dll.


```JScript
objQ = new ActiveXObject("IXSSO.Query");
```



 

 



