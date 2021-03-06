---
title: "DISCOVER_MEMORYGRANT Rowset | Microsoft Docs"
ms.date: 07/25/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: schema-rowsets
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
---
# DISCOVER_MEMORYGRANT Rowset

  Returns a list of internal memory quota grants that are taken by jobs that are currently running on the server. To find out whether a job is running on the server, use `Select * from $System.Discover_Jobs`.  
  
 **Applies to:** tabular models, multidimensional models  
  
## Rowset Columns  
 The **DISCOVER_MEMORYGRANT** rowset contains the following columns.  
  
|Column name|Type indicator|Restriction|Description|  
|-----------------|--------------------|-----------------|-----------------|  
|**MEMORY_ID**|**DBTYPE_I8**||A number that identifies the memory quota grant. Unique within the context of a single DISCOVER_MEMORYGRANT request.|  
|**SPID**|**DBTYPE_I4**|Required|The SPID, which you can obtain by running `Select * from $System.Discover_Sessions`.|  
|**CreationTime**|**DBTYPE_I8 DBTYPE_DBTIMESTAMP**||The time the quota was granted.|  
|**LastRequestTime**|**DBTYPE_DBTIMESTAMP**||The time the quota request was last modified.|  
|**MemoryUsed**|**DBTYPE_I4**||The amount of memory used in association with the quota.|  
|**MemoryGranted**|**DBTYPE_I4**||The amount of memory granted for use by the job that is obtaining the memory quota.|  
|**Blocked**|**DBTYPE_BOOL**||A Boolean that indicates the block status of the job. True indicates that the job is blocked waiting for another job to release sufficient quota to grant its quota request. False indicates that the job has received its quota and can execute.|  
  
 This schema rowset is not sorted.  
  
## Using ADOMD.NET to return the rowset  
 When using ADOMD.NET and the schema rowset to retrieve metadata, you can use either the GUID or string to reference a schema rowset object in the GetSchemaDataSet method.
  
 The following table provides the GUID and string values that identify this rowset.  
  
|Argument|Value|  
|--------------|-----------|  
|GUID|a07ccd23-8148-11d0-87bb-00c04fc33942|  
|ADOMDNAME|MemoryGrant|  
