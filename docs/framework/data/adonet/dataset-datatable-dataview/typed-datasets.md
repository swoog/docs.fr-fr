---
title: Datasets typés
ms.date: 03/30/2017
ms.assetid: 033d2548-cf24-4c05-8179-67d8b009c048
ms.openlocfilehash: 92ed3f8fd392238785fd2d205668f14fe477f2b8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59098649"
---
# <a name="typed-datasets"></a>Datasets typés
En plus d'un accès par liaison tardive aux valeurs via des variables faiblement typées, l'objet <xref:System.Data.DataSet> permet un accès aux données par l'intermédiaire d'une métaphore fortement typée. Tables et colonnes qui font partie de la **DataSet** sont accessibles à l’aide des noms conviviaux et de variables fortement typées.  
  
 Typé **DataSet** est une classe qui dérive un **DataSet**. Par conséquent, il hérite de toutes les méthodes, événements et propriétés d’un **DataSet**. En outre, typé **DataSet** fournit des méthodes fortement typées, propriétés et événements. Cela signifie que vous pouvez accéder à des tables et à des colonnes par leur nom au lieu d'utiliser les méthodes associées à des collections. À part d’améliorer la lisibilité du code, typé **DataSet** autorise également le code de Visual Studio .NET éditeur complète automatiquement les lignes en cours de frappe.  
  
 En outre, fortement typée **DataSet** donne accès aux valeurs avec le type approprié au moment de la compilation. Avec fortement typé **DataSet**, interception des erreurs d’incompatibilité de type lorsque le code est compilé et non au moment de l’exécution.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Génération de datasets fortement typés](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-strongly-typed-datasets.md)  
 Décrit comment créer et utiliser fortement typé **DataSet**.  
  
 [Annotation de DataSet typés](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/annotating-typed-datasets.md)  
 Explique comment annoter le schéma XML Schema definition language (XSD) permet de générer un fortement typée **DataSet**afin de donner aux **DataSet** noms conviviaux d’éléments sans modifier le schéma sous-jacent.  
  
## <a name="see-also"></a>Voir aussi

- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
