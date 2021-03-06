---
title: "TextConst Data Type"
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
# TextConst Data Type
Denotes a multi-language string constant.




[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks
The TextConst data type is typically used for UI messages; process or error messages. Keeping the `TextConst` data type in global scope, makes it easier to reuse the same message for several situations. The data type can be declared with the syntax as shown below:

```
codeunit 50100 MyCodeunit
{
    procedure MyProcedure()
    var
        localTextConst: TextConst ENU = 'My text', DAN = 'Min tekst';
    begin
        Message(localTextConst);
    end;

    var
        globalTextConst: TextConst ENU = 'My text', DAN = 'Min tekst';
}

```

## See Also  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)  