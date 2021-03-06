---
title: "MDSCHEMA_MEASUREGROUP_DIMENSIONS Rowset | Microsoft Docs"
ms.date: 05/03/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: schema-rowsets
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
---
# MDSCHEMA_MEASUREGROUP_DIMENSIONS Rowset
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
  Enumerates the dimensions of measure groups.  
  
## Rowset Columns  
 The **MDSCHEMA_MEASUREGROUP_DIMENSIONS** rowset contains the following columns.  
  
|Column name|Type indicator|Length|Description|  
|-----------------|--------------------|------------|-----------------|  
|**CATALOG_NAME**|**DBTYPE_WSTR**||The name of the catalog to which this measure group belongs. **NULL** if the provider does not support catalogs.|  
|**SCHEMA_NAME**|**DBTYPE_WSTR**||Not supported.|  
|**CUBE_NAME**|**DBTYPE_WSTR**||The name of the cube to which this measure group belongs.|  
|**MEASUREGROUP_NAME**|**DBTYPE_WSTR**||The name of the measure group.|  
|**MEASUREGROUP_CARDINALITY**|**DBTYPE_WSTR**||The number of instances a measure in the measure group can have for a single dimension member. Possible values include:<br /><br /> **ONE**<br /><br /> **MANY**|  
|**DIMENSION_UNIQUE_NAME**|**DBTYPE_WSTR**||The unique name for the dimension.|  
|**DIMENSION_CARDINALITY**|**DBTYPE_WSTR**||The number of instances a dimension member can have for a single instance of a measure group measure. Possible values include:<br /><br /> **ONE**<br /><br /> **MANY**|  
|**DIMENSION_IS_VISIBLE**|**DBTYPE_BOOL**||A Boolean that indicates whether hieararchies in the dimension are visible.<br /><br /> Returns **TRUE** if one or more hierarchies in the dimension is visible; otherwise, **FALSE**.|  
|**DIMENSION_IS_FACT_DIMENSION**|**DBTYPE_BOOL**||A Boolean that indicates whether the dimension is a fact dimension.<br /><br /> Returns **TRUE** if the dimension is a fact dimension; otherwise, **FALSE**.|  
|**DIMENSION_PATH**|**DBTYPE_HCHAPTER**||A list of dimensions for the reference dimension.|  
|**DIMENSION_GRANULARITY**|**DBTYPE_WSTR**||The unique name of the granularity hierarchy.|  
  
 The rowset supports sorting on **CATALOG_NAME**, **SCHEMA_NAME**, **CUBE_NAME**, **MEASUREGROUP_NAME**, **DIMENSION_UNIQUE_NAME**.  
  
## Restriction Columns  
 The **MDSCHEMA_MEASUREGROUP_DIMENSIONS** rowset can be restricted on the columns listed in the following table.  
  
|Column name|Type indicator|Restriction State|  
|-----------------|--------------------|-----------------------|  
|**CATALOG_NAME**|**DBTYPE_WSTR**|Optional.|  
|**SCHEMA_NAME**|**DBTYPE_WSTR**|Optional.|  
|**CUBE_NAME**|**DBTYPE_WSTR**|Optional.|  
|**MEASUREGROUP_NAME**|**DBTYPE_WSTR**|Optional.|  
|**DIMENSION_UNIQUE_NAME**|**DBTYPE_WSTR**|Optional.|  
|**DIMENSION_VISIBILITY**|**DBTYPE_UI2**|(Optional) A bitmap with one of the following valid values:<br /><br /> 1 Visible<br /><br /> 2 Not visible<br /><br /> Default restriction is a value of 1.|  
  
## See Also  
 [OLE DB for OLAP Schema Rowsets](../../../analysis-services/schema-rowsets/ole-db-olap/ole-db-for-olap-schema-rowsets.md)  
  
  
