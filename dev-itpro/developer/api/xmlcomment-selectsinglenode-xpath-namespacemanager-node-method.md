---
title: "SelectSingleNode Method"
ms.author: solsen
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 1
manager: edupont
author: SusanneWindfeldPedersen
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# SelectSingleNode Method
Selects the first XmlNode that matches the XPath expression.  
```  
[Ok := ] XmlComment.SelectSingleNode(XPath, NamespaceManager, Node)  
```  
## Parameters
*XPath*    
&emsp;Type: [String](../datatypes/devenv-text-data-type.md)  
The XPath expression.  
  
*NamespaceManager*    
&emsp;Type: [XmlNamespaceManager](xmlnamespacemanager-class.md)  
An XmlNamespaceManager to use for resolving namespaces for prefixes in the XPath expression.  
  
*Node*    
&emsp;Type: [XmlNode](xmlnode-class.md)  
The first XmlNode that matches the XPath query.  
  
## Return Value
*Ok*  
&emsp;Type: [Boolean](../datatypes/devenv-boolean-data-type.md)  
**True** if the operation was successful; otherwise, **false**.  
If you omit this optional return value and the operation does not execute successfully, a run-time error will occur.  
  
## See Also
[XmlComment](xmlcomment-class.md)  
[XmlNamespaceManager](xmlnamespacemanager-class.md)  
[XmlNode](xmlnode-class.md)  
[HTTP, JSON, TextBuilder, and XML API](../devenv-restapi-overview.md)  
[Getting Started with AL](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)  
