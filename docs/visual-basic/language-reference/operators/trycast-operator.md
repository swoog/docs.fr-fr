---
title: Opérateur TryCast (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.trycast
- trycast
helpviewer_keywords:
- TryCast keyword [Visual Basic]
ms.assetid: d1ef5d47-fef4-491e-b014-1d910628f65c
ms.openlocfilehash: c0eea4565d5040bb00743fc7864ac15b0fccdea9
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58831590"
---
# <a name="trycast-operator-visual-basic"></a>Opérateur TryCast (Visual Basic)
Introduit une opération de conversion de type qui ne lève pas d’exception.  
  
## <a name="remarks"></a>Notes  
 Si une tentative de conversion échoue, `CType` et `DirectCast` lancent une <xref:System.InvalidCastException> erreur. Cela peut nuire aux performances de votre application. `TryCast` Retourne [rien](../../../visual-basic/language-reference/nothing.md), de sorte qu’au lieu de devoir gérer une exception possible, vous devez seulement tester le résultat retourné par rapport à `Nothing`.  
  
 Vous utilisez le `TryCast` mot clé de la même façon que vous utilisez le [CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md) et le [opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) mot clé. Vous fournissez une expression comme le premier argument et un type pour le convertir comme deuxième argument. `TryCast` fonctionne uniquement sur les types de référence, notamment les classes et interfaces. Il requiert une relation d’héritage ou d’implémentation entre les deux types. Cela signifie qu’un type doit hériter ou implémenter l’autre.  
  
## <a name="errors-and-failures"></a>Erreurs et échecs  
 `TryCast` génère une erreur du compilateur s’il détecte qu’il n’existe aucune relation d’héritage ou d’implémentation. Mais l’absence d’une erreur du compilateur ne garantit pas une conversion réussie. Si la conversion souhaitée est restrictive, il peut échouer au moment de l’exécution. Si cela se produit, `TryCast` retourne [rien](../../../visual-basic/language-reference/nothing.md).  
  
## <a name="conversion-keywords"></a>Mots clés de conversion  
 Voici une comparaison des mots clés de conversion de type.  
  
|Mot clé|Types de données|Relation d’argument|Échec d’exécution|  
|---|---|---|---|  
|[CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md)|Les types de données|Conversion restrictive ou étendue doit être défini entre les deux types de données|Lève <xref:System.InvalidCastException>|  
|[DirectCast (opérateur)](../../../visual-basic/language-reference/operators/directcast-operator.md)|Les types de données|Un type doit hériter ou implémenter l’autre type|Lève <xref:System.InvalidCastException>|  
|`TryCast`|Seuls les types de référence|Un type doit hériter ou implémenter l’autre type|Retourne [Nothing](../../../visual-basic/language-reference/nothing.md)|  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment utiliser `TryCast`.  
  
 [!code-vb[VbVbalrKeywords#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
