---
title: "Encrypt Method"
ms.author: solsen
ms.custom: na
ms.date: 02/22/2019
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
author: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# Encrypt Method
Takes a string as input and returns the encrypted value of the string.


## Syntax
```
EncryptedString :=   System.Encrypt(PlainTextString: String)
```
> [!NOTE]  
> This method can be invoked without specifying the data type name.  
## Parameters
*PlainTextString*  
&emsp;Type: [String](../string/string-data-type.md)  
  


## Return Value
*EncryptedString*  
&emsp;Type: [String](../string/string-data-type.md)  
  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  
 If encryption is not enabled or the encryption key is not found, the following error will be displayed: **An encryption key is required to complete the request**.   

## Example  
 The code example requires that you create the following text constant in the **C/AL Globals** window.  

 **Text** Text000  

```  
Text000 := 'ABC123';  
MESSAGE('Value: ' + Text000)  
Text000 := ENCRYPT(Text000);  
MESSAGE('Value: ' + Text000);  
```  

 This code example takes the string value **ABC123** and outputs the encrypted value of the string. The encrypted value will vary from system to system due to differences in the encryption key.  


## See Also
[System Data Type](system-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)