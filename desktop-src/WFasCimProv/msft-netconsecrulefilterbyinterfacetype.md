---
Description: Filters a connection security rule by interface type.
ms.assetid: 2176940d-1cac-4fe0-aa0d-7e93e490d360
title: MSFT\_NetConSecRuleFilterByInterfaceType class
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MSFT\_NetConSecRuleFilterByInterfaceType class

Filters a connection security rule by interface type.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.

## Syntax

``` syntax
class MSFT_NetConSecRuleFilterByInterfaceType : MSFT_NetConSecRuleFilters
{
  MSFT_NetConSecRule          REF GroupComponent;
  MSFT_NetInterfaceTypeFilter REF PartComponent;
};
```

## Members

The **MSFT\_NetConSecRuleFilterByInterfaceType** class has these types of members:

-   [Properties](#properties)

### Properties

The **MSFT\_NetConSecRuleFilterByInterfaceType** class has these properties.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Data type: **MSFT\_NetConSecRule**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **Key**, **Override**
</dt> </dl>

The connection security rule being filtered.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Data type: **MSFT\_NetInterfaceTypeFilter**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **Key**, **Override**
</dt> </dl>

The interface type filter applied to the rule.

</dd> </dl>

## Requirements



|                                     |                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8<br/>                                                                   |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                         |
| Namespace<br/>                | Root\\StandardCimv2<br/>                                                         |
| MOF<br/>                      | <dl> <dt>WFasCim.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WFasCim.dll</dt> </dl> |



 

 



