---
title: "WriteTo_String Method"
ms.author: solsen
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 9
manager: edupont
author: SusanneWindfeldPedersen
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# WriteTo_String Method
Serializes and writes the JSON data of the JsonObject to a given Text object.

```
[Ok := ] JsonObject.WriteTo(var Text)
```

## Parameters
*JsonObject*  
&emsp;Type: [JsonObject](jsonobject-class.md)

*String*  
&emsp;Type: [Text](../datatypes/devenv-text-data-type.md)

The Text object to which the JSON data will be written.

## Property Value/Return Value
&emsp;Type: [Boolean](../datatypes/devenv-boolean-data-type.md)

**True** if the write was successful; otherwise, **false**.

If you omit this optional return value and if the write does not execute successfully, then a run-time error occurs.

## See Also
[JsonObject](jsonobject-class.md)  
[HTTP, JSON, TextBuilder, and XML API](../devenv-restapi-overview.md)  
[Getting Started with AL](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)
