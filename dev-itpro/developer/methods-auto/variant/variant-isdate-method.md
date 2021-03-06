---
title: "IsDate Method"
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
# IsDate Method
Indicates whether an AL variant contains a Date variable.


## Syntax
```
Ok :=   Variant.IsDate()
```
> [!NOTE]  
> This method can be invoked using property access syntax.  

## Parameters
*Variant*  
&emsp;Type: [Variant](variant-data-type.md)  
An instance of the [Variant](variant-data-type.md) data type.  

## Return Value
*Ok*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
**true** if the AL variant contains a Date variable, otherwise **false**.  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Example  
 The following example determines whether an AL variant contains a Date variable. The code initializes the MyDate variable with a Date value. The MyDate variable is assigned to the variant variable that is named MyVariant. The **ISDATE** method determines whether the variant contains a Date variable and stores the return value in the varResult variable. In this case, the variant contains a Date variable so **true** is returned and displayed in a message box. The [ISCODE Method (Variant)](../../methods/devenv-iscode-method-variant.md) determines whether the variant contains a Code variable. The return value is **false** because the variant does not contain a code. This example requires that you create the following global variables and text constants.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|MyDate|Date|  
|MyVariant|Variant|  
|varResult|Boolean|  
  
|Text constant name|Enu value|  
|------------------------|---------------|  
|Text000|Does the variant >%1\< contain a date variable? %2.|  
|Text001|Does the variant >%1\< contain a code variable? %2.|  
  
```  
MyDate := TODAY;  
MyVariant :=  MyDate;  
varResult := MyVariant.ISDATE;  
MESSAGE(Text000,MyVariant,varResult);  
varResult := MyVariant.ISCODE;  
MESSAGE(Text001,MyVariant,varResult);  
```  
  

## See Also
[Variant Data Type](variant-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)