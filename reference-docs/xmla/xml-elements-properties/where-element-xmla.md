---
title: "Where Element (XMLA) | Microsoft Docs"
ms.date: 07/24/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: xmla
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
---
# Where Element (XMLA)

  Defines a filter condition used by the parent [Drop](../xml-elements-commands/drop-element-xmla.md) or [Update](../xml-elements-commands/update-element-xmla.md) command.  
  
## Syntax  
  
```xml  
  
<Drop> <!-- or Update -->  
   ...  
   <Where>  
      <Attributes>...</Attributes>  
   </Where>  
   ...  
</Insert>  
```  
  
## Element characteristics  
  
|Characteristic|Description|  
|--------------------|-----------------|  
|Data type and length|None|  
|Default value|None|  
|Cardinality|1-1: Required element that occurs once and only once.|  
  
## Element relationships  
  
|Relationship|Element|  
|------------------|-------------|  
|Parent elements|[Drop](../xml-elements-commands/drop-element-xmla.md), [Update](../xml-elements-commands/update-element-xmla.md)|  
|Child elements|[Attributes](../xml-elements-properties/attributes-element-xmla.md)|  
  
## Remarks  
 For **Drop** commands, the **Where** element, combined with the [DeleteWithDescendants](../xml-elements-properties/deletewithdescendants-element-xmla.md) element, identifies the scope of attribute members to be dropped.  
  
 For **Update** commands, the **Where** element identifies the scope of attribute members to be updated. Multiple attribute members can be updated by using a combination of attributes included in the **Attributes** collection of the parent **Update** command and the **Attributes** collection of the **Where** element.  
