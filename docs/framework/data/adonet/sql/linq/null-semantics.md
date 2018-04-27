---
title: Sémantique Null
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: a97017ae-d634-4cf3-bbaf-054a528fd683
caps.latest.revision: 2
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: 3c4daa5fd37158f1af31f33ba743a56cf76670d8
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="null-semantics"></a>Sémantique Null
Le tableau suivant fournit des liens vers différentes parties de la [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation où `null` (`Nothing` en Visual Basic) décrit des problèmes.  
  
|Rubrique|Description|  
|-----------|-----------------|  
|[Incompatibilité entre types SQL-CLR](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mismatches.md)|La section « Sémantique Null » de cette rubrique inclut une présentation des trois états SQL booléenne et le common language runtime (CLR) de deux états <xref:System.Boolean>, le littéral `Nothing` (Visual Basic) et `null` (c#) et d’autres problèmes similaires.|  
|[Traduction des opérateurs de requête standard](../../../../../../docs/framework/data/adonet/sql/linq/standard-query-operator-translation.md)|La section « Sémantique Null » de cette rubrique décrit la sémantique de comparaison Null dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].|  
|[System.String, méthodes](../../../../../../docs/framework/data/adonet/sql/linq/system-string-methods.md)|La section « Différences par rapport à .NET » de cette rubrique décrit comment un retour de 0 de <xref:System.String.LastIndexOf%2A> peut signifier que la chaîne a la valeur null ou que la position trouvée est 0.|  
|[Calculer la somme de valeurs dans une séquence numérique](../../../../../../docs/framework/data/adonet/sql/linq/compute-the-sum-of-values-in-a-numeric-sequence.md)|Décrit comment la <xref:System.Linq.Enumerable.Sum%2A> opérateur a la valeur `null` (`Nothing` en Visual Basic) au lieu de 0 pour une séquence qui contient uniquement des valeurs NULL ou une séquence vide.|  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions et types de données](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
