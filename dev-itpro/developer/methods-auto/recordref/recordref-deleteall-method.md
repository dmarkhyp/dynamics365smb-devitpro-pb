---
title: "DeleteAll Method"
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
# DeleteAll Method
Deletes all records in a table that fall within a specified range.


## Syntax
```
 RecordRef.DeleteAll([RunTrigger: Boolean])
```
## Parameters
*RecordRef*  
&emsp;Type: [RecordRef](recordref-data-type.md)  
An instance of the [RecordRef](recordref-data-type.md) data type.  

*RunTrigger*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
Specifies whether the code in the OnDelete trigger will be executed. If this parameter is true, the code will be executed. If this parameter is false (default), the code will not be executed. This parameter is optional.
          



[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  
 This method works the same way as the [DELETEALL Method \(Record\)](../../methods/devenv-deleteall-method-record.md).  
  
## Example  
 The following example opens table 18 \(Customer\) as a RecordRef variable that is named CustomerRecRef. The [FIELD Method \(RecordRef\)](../../methods/devenv-field-method-recordref.md) creates a FieldRef variable that is named MyFieldRef for field 1 \(No.\). From the No. field, the [SETRANGE Method \(FieldRef\)](../../methods/devenv-setrange-method-fieldref.md) selects records in the range from 10000 to 20000. The number of records in the range is displayed in a message box. The DELETEALL method deletes all records in that range. The number of records is displayed again. This time, 0 is displayed because all the records in the range are deleted. This example requires that you create the following global variable and text constant.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|CustomerRecRef|RecordRef|  
|MyFieldRef|FieldRef|  
  
|Text constant name|DataType|ENU value|  
|------------------------|--------------|---------------|  
|Text000|Text|The number of records in the range is %1.|  
  
```  
  
CustomerRecRef.OPEN(18);  
MyFieldRef := CustomerRecRef.FIELD(1);  
MyFieldRef.SETRANGE('10000' , '20000');  
MESSAGE(Text000 ,CustomerRecRef.COUNT);  
CustomerRecRef.DELETEALL;  
MESSAGE(Text000 ,CustomerRecRef.COUNT);  
```  
  

## See Also
[RecordRef Data Type](recordref-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)