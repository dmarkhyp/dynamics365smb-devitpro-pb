---
title: "SETFILTER Method (TestPage Filter)"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: 39fdbfdd-30af-4bcc-91cb-dcb2b3b14377
caps.latest.revision: 5
manager: edupont
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# SETFILTER Method (TestPage Filter)
Applies a filter to the specified field on a test page.  
  
## Syntax  
  
```  
TestPage.Part.Fiter.SETFILTER(Field, String);  
```  
  
#### Parameters  
 *TestPage*  
 Type: TestPage  
  
 The test page that displays the dataset that contains the specified field.  
  
 *Part*  
 Type: Part  
  
 The control on the test page that contains the dataset.  
  
 *Filter*  
 Type: Filter  
  
 The filter that is applied to the dataset.  
  
 *Field*  
 Type: Field  
  
 The field that you want to apply the filter to.  
  
 *String*  
 Type: Text  
  
 The filter to apply to the specified field.  
  
## See Also  
 [TestPage Filter Methods](devenv-TestPage-Filter-Methods.md)