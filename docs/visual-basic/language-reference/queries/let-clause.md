---
title: Let, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryLet
helpviewer_keywords:
- queries [Visual Basic], Let
- Let clause [Visual Basic]
- Let statement [Visual Basic]
ms.assetid: 981aa516-16eb-4c53-b1f1-5aa3e82f316e
ms.openlocfilehash: ff298f001a2d865446436e8099a2fbbef593a00a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62054196"
---
# <a name="let-clause-visual-basic"></a>Let, clause (Visual Basic)
Calcule une valeur et l’assigne à une nouvelle variable dans la requête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Let variable = expression [, ...]  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`variable`|Obligatoire. Un alias qui peut être utilisé pour référencer les résultats de l’expression fournie.|  
|`expression`|Obligatoire. Une expression qui sera évaluée et assignée à la variable spécifiée.|  
  
## <a name="remarks"></a>Notes  
 Le `Let` clause vous permet de calculer des valeurs pour chaque résultat de la requête et les référencent en utilisant un alias. L’alias peut être utilisé dans d’autres clauses, telles que le `Where` clause. Le `Let` clause vous permet de créer une instruction de requête qui est plus facile à lire, car vous pouvez spécifier un alias pour une clause d’expression incluse dans la requête et substituer l’alias chaque fois que la clause d’expression est utilisée.  
  
 Vous pouvez inclure un nombre quelconque de `variable` et `expression` attributions dans le `Let` clause. Séparez chaque affectation par une virgule (,).  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise le `Let` clause pour calculer une remise de 10 pour cent sur les produits.  
  
 [!code-vb[VbSimpleQuerySamples#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#16)]  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
