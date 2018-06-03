---
title: DnsServerResourceRecordMX class
description: DNS Server Resource Record MX.
audience: developer
ms.assetid: b02c4e5c-b048-4970-ab90-d64a9ed0e032
ms.prod: windows-server-dev
ms.technology:
- dns-server
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- DnsServerResourceRecordMX class
- DnsServerResourceRecordMX class, described
topic_type:
- apiref
api_name:
- DnsServerResourceRecordMX
- DnsServerResourceRecordMX.Preference
- DnsServerResourceRecordMX.MailExchange
api_location:
- DnsServerPSProvider.dll
api_type:
- DllExport
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# DnsServerResourceRecordMX class

DNS Server Resource Record MX.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.

## Syntax

``` syntax
[ClassVersion("1.0.0"), dynamic, provider("DnsServerPSProvider"), AMENDMENT]
class DnsServerResourceRecordMX : DnsServerResourceRecordData
{
  uint16 Preference;
  string MailExchange;
};
```

## Members

The **DnsServerResourceRecordMX** class has these types of members:

-   [Properties](#properties)

### Properties

The **DnsServerResourceRecordMX** class has these properties.

<dl> <dt>

**MailExchange**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read/write
</dt> </dl>

Mail Exchange.

</dd> <dt>

**Preference**
</dt> <dd> <dl> <dt>

Data type: **uint16**
</dt> <dt>

Access type: Read/write
</dt> </dl>

Preference.

</dd> </dl>

## Requirements



|                                     |                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                          |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                                     |
| Namespace<br/>                | Root\\Microsoft\\Windows\\Dns<br/>                                                           |
| MOF<br/>                      | <dl> <dt>DnsServerPSProvider.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DnsServerPSProvider.dll</dt> </dl> |



## See also

<dl> <dt>

[**DnsServerResourceRecordData**](dnsserverresourcerecorddata.md)
</dt> <dt>

[DnsServerPSProvider Provider](dns-server-classes.md)
</dt> </dl>

 

 




