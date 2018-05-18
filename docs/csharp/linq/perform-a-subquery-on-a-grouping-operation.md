---
title: Effectuer une sous-requête sur une opération de regroupement
description: Guide pratique pour effectuer une sous-requête sur une opération de regroupement.
ms.date: 12/1/2016
ms.assetid: d75a588e-9b6f-4f37-b195-f99ec8503855
ms.openlocfilehash: 209d05c2fe8719fa9116061d199272366146f465
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="perform-a-subquery-on-a-grouping-operation"></a>Effectuer une sous-requête sur une opération de regroupement

Cette rubrique présente deux façons de créer une requête qui organise les données sources en groupes et effectue ensuite une sous-requête sur chacun de ces groupes. Dans chaque exemple, la technique de base consiste à regrouper les éléments sources en utilisant une *continuation* nommée `newGroup`, puis en créant une sous-requête sur `newGroup`. Cette sous-requête est exécutée sur chaque groupe créé par la requête externe. Notez que, dans cet exemple particulier, le résultat final n’est pas un groupe, mais une séquence plate de types anonymes.  
  
 Pour plus d’informations sur les regroupements, consultez [group, clause](../language-reference/keywords/group-clause.md).  
  
 Pour plus d’informations sur les continuations, consultez [into](../language-reference/keywords/into.md). L’exemple suivant utilise une structure de données en mémoire comme source de données, mais les mêmes principes s’appliquent à tous les types de sources de données LINQ.  
  
## <a name="example"></a>Exemple 

 > [!NOTE]
 > Cet exemple contient des références aux objets définis dans l’exemple de code qui est présenté dans [Interroger une collection d’objets](query-a-collection-of-objects.md).

 [!code-csharp[csProgGuideLINQ#23](../../../samples/snippets/csharp/concepts/linq/how-to-perform-a-subquery-on-a-grouping-operation_1.cs)]  
   
## <a name="see-also"></a>Voir aussi  
 [Expressions de requête LINQ](index.md)
