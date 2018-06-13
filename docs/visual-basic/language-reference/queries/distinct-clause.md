---
title: Distinct, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryDistinct
helpviewer_keywords:
- Distinct clause [Visual Basic]
- Distinct statement [Visual Basic]
- queries [Visual Basic], Distinct
ms.assetid: 86f42614-0d8f-4ffc-b888-ce8a37a8d36a
ms.openlocfilehash: 4b0ce12f6361d3dc6e5cc3601e96fc3a9bcf3841
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603975"
---
# <a name="distinct-clause-visual-basic"></a>Distinct, clause (Visual Basic)
Restreint les valeurs de la variable de portée actuelle pour éliminer les valeurs en double dans les clauses de requête suivantes.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Distinct  
```  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser la `Distinct` clause pour retourner une liste d’éléments uniques. Le `Distinct` clause indique que la requête d’ignorer les résultats de requête en double. Le `Distinct` clause s’applique aux valeurs doubles pour tous les champs spécifiés par un retour la `Select` clause. Si aucun `Select` clause est spécifiée, la `Distinct` clause est appliquée à la variable de portée pour la requête identifiée dans la `From` clause. Si la variable de portée n’est pas un type immuable, la requête n’ignore un résultat de requête si tous les membres du type correspond à un résultat de requête existant.  
  
## <a name="example"></a>Exemple  
 L’expression de requête suivante joint une liste de clients et une liste des commandes client. Le `Distinct` clause est incluse pour retourner une liste de noms de clients uniques et les dates de commande.  
  
 [!code-vb[VbSimpleQuerySamples#20](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/distinct-clause_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [Requêtes](../../../visual-basic/language-reference/queries/queries.md)  
 [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)  
 [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)  
 [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
