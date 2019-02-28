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
ms.openlocfilehash: 00a2e52bd6669869bb2e25bc2857f1598da5763f
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56971245"
---
# <a name="distinct-clause-visual-basic"></a>Distinct, clause (Visual Basic)
Restreint les valeurs de la variable de portée actuelle pour éliminer les valeurs en double dans les clauses de requête suivantes.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Distinct  
```  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser le `Distinct` clause pour retourner une liste d’éléments uniques. Le `Distinct` clause provoque la requête d’ignorer les résultats de requête en double. Le `Distinct` clause s’applique aux valeurs en double pour tous les champs spécifiés par de retour le `Select` clause. Si aucun `Select` clause est spécifiée, le `Distinct` clause est appliquée à la variable de portée pour la requête identifiée dans le `From` clause. Si la variable de portée n’est pas un type immuable, la requête ignore uniquement un résultat de requête si tous les membres du type correspond à un résultat de requête existant.  
  
## <a name="example"></a>Exemple  
 L’expression de requête suivante joint une liste de clients et une liste de commandes du client. Le `Distinct` clause est incluse pour retourner une liste de noms de clients uniques et dates de commande.  
  
 [!code-vb[VbSimpleQuerySamples#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#20)]  
  
## <a name="see-also"></a>Voir aussi
- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
