---
title: "Adding Pages and Reports to Tell me"
description: "Description of how you use AL to add pages and reports so that they are discoverable through search in the client."
author: SusanneWindfeldPedersen
ms.custom: na
ms.date: 12/17/2018
ms.topic: article
ms.service: "dynamics365-business-central"
ms.author: solsen
---

[!INCLUDE[d365fin_dev_blog](includes/d365fin_dev_blog.md)]

# Adding Pages and Reports to Tell me
When you have added a page or a report in your extension, you most likely want it to be discoverable to the user. AL provides navigational support for pages and reports in the client. You enable a page or report to be available through **Tell me** in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] by setting the **UsageCategory** property in code. The **UsageCategory** setting will make the page or report searchable, and the value chosen for the setting will further sub categorize the item.

![TellMe](../media/tellme.jpg)

## Working with Tell me
When you create a [Page](devenv-page-object.md) or a [Report](devenv-report-object.md), you add the [UsageCategory Property](properties/devenv-usagecategory-property.md). If the **UsageCategory** is set to **None**, or if you do not specify **UsageCategory**, the page or report will not show up when you search in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. 

## UsageCategory property values
The values for the **UsageCategory** property are listed below. The sub category will help the user navigate through the search results and it is a best practice to be consistent when categorizing the pages and the reports that you add. A consistent approach will help guiding the user and improve productivity.

|Value           |Description                                  |
|----------------|---------------------------------------------|
|None            |The page or report is not included in search.|
|Lists           |The page or report is listed as **Lists** under the **Pages and Tasks** category.|
|Tasks           |The page or report is listed as **Tasks** under the **Pages and Tasks** category.|
|ReportsAndAnalysis |The page or report is listed as **Reports and Analysis** under the **Reports and Analysis** category.|
|Documents       |The page or report is listed as **Documents** under the **Reports and Analysis** category.|
|History         |The page or report is listed as **Archive** under the **Reports and Analysis** category.|
|Administration  |The page or report is listed as **Administration** under the **Pages and Tasks** category.|

## Example
The following example creates a `SimpleCustomerCard` page and sets a `UsageCategory` property to the page, so that the `SimpleCustomerCard` page is discoverable through search using the Tell me functionality. 

```
page 50210 SimpleCustomerCard 
{ 
    PageType = Card; 
    SourceTable = Customer; 
    UsageCategory = Documents;  
    AccessByPermission = page SimpleCustomerCard = X;
    ApplicationArea = All;
    layout 
    { 
        area(content) 
        { 
            group(General) 
            { 
                field("No.";"No.") {} 
                field(Name;Name) {} 
                field(Address;Address) {} 
            } 
        } 
    } 
} 
```

## Optional settings
In addition to making a page or report searchable, you can control the access of an object by providing **Read**, **Insert**, **Modify**, **Delete**, and **Execute** (RIMDX) permissions by adding the [AccessByPermission property](properties/devenv-accessbypermission-property.md). Likewise, control the application area access on the specified object by adding the [ApplicationArea Property](properties/devenv-applicationarea-property.md). 

The **AccessByPermission** property and **ApplicationArea** property are the optional settings, which can be applied with the **UsageCategory** property. These settings are used to set restrictions on an object when you enable the Search functionality.

## Working in the [!INCLUDE[nav_dev_long_md](includes/nav_dev_long_md.md)]
If you are using the [!INCLUDE[nav_dev_long_md](includes/nav_dev_long_md.md)], you can also set UsageCategory, AccessByPermission, and ApplicationArea properties on pages and reports to control their search.

After you change these properties, before the changes take effect in the client, you must run **Build Object Search Index** from the **Tools** menu.

## See Also
[Adding Menus to the Navigation Pane](devenv-adding-menus-to-navigation-pane.md)  
[UsageCategory Property](properties/devenv-usagecategory-property.md)  
[Page Object](devenv-page-object.md)  
[Report Object](devenv-report-object.md)  
[AL Development Environment](devenv-reference-overview.md)
