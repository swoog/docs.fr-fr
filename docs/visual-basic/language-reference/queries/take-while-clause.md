---
title: Take While, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTakeWhile
helpviewer_keywords:
- queries [Visual Basic], Take While
- Take While clause [Visual Basic]
- Take While statement [Visual Basic]
ms.assetid: db8f9f2f-fc9f-4a6c-b0b8-1bf048147e11
ms.openlocfilehash: 181cc641bb12329c898cc3bb226ea49f0836e979
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44085353"
---
# <a name="take-while-clause-visual-basic"></a>Take While, clause (Visual Basic)
Inclut les éléments d'une collection tant qu'une condition spécifiée a la valeur `true` et ignore les éléments restants.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Take While expression  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`expression`|Obligatoire. Une expression qui représente une condition pour tester des éléments. L’expression doit retourner un `Boolean` valeur ou un équivalent fonctionnel, comme un `Integer` soit évaluée comme un `Boolean`.|  
  
## <a name="remarks"></a>Notes  
 Le `Take While` clause inclut des éléments à partir du début d’un résultat de requête jusqu'à fourni `expression` retourne `false`. Après le `expression` retourne `false`, la requête ignore tous les éléments restants. Le `expression` est ignoré pour les autres résultats.  
  
 Le `Take While` diffère de la clause le `Where` clause dans qui le `Where` clause peut être utilisée pour inclure tous les éléments à partir d’une requête qui remplissent une condition particulière. Le `Take While` clause inclut des éléments uniquement jusqu'à la première fois que la condition n’est pas satisfaite. Le `Take While` clause est particulièrement utile lorsque vous travaillez avec un résultat de requête ordonnée.  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise le `Take While` clause pour récupérer les résultats jusqu'à ce que le premier client sans commande est trouvé.  
  
 [!code-vb[VbSimpleQuerySamples#2](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/take-while-clause_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [Requêtes](../../../visual-basic/language-reference/queries/index.md)  
 [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)  
 [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)  
 [Take (clause)](../../../visual-basic/language-reference/queries/take-clause.md)  
 [Skip While (clause)](../../../visual-basic/language-reference/queries/skip-while-clause.md)  
 [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
