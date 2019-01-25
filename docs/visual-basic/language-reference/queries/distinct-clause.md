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
ms.openlocfilehash: 3761f6d6ba97e7f1a824b70b18a50dae820c7e51
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710038"
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
  
 [!code-vb[VbSimpleQuerySamples#20](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/distinct-clause_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
