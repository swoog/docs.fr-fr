---
title: Opérateur TryCast (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.trycast
- trycast
helpviewer_keywords:
- TryCast keyword [Visual Basic]
ms.assetid: d1ef5d47-fef4-491e-b014-1d910628f65c
ms.openlocfilehash: d8825b8eee35ea514d4001a6a5c1cc5139c67454
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="trycast-operator-visual-basic"></a>Opérateur TryCast (Visual Basic)
Introduit une opération de conversion de type qui ne lève pas d’exception.  
  
## <a name="remarks"></a>Notes  
 Si une tentative de conversion échoue, `CType` et `DirectCast` les lèvent une <xref:System.InvalidCastException> erreur. Cela peut nuire aux performances de votre application. `TryCast` Retourne [rien](../../../visual-basic/language-reference/nothing.md), de sorte qu’au lieu de devoir gérer une exception possible, vous devez seulement tester le résultat retourné par rapport à `Nothing`.  
  
 Vous utilisez la `TryCast` mot clé de la même façon que vous utilisez le [CType, fonction](../../../visual-basic/language-reference/functions/ctype-function.md) et le [DirectCast, opérateur](../../../visual-basic/language-reference/operators/directcast-operator.md) (mot clé). Vous fournissez une expression comme premier argument et un type pour convertir comme deuxième argument. `TryCast` fonctionne uniquement sur les types référence, tels que les classes et interfaces. Il requiert une relation d’héritage ou d’implémentation entre les deux types. Cela signifie qu’un type doit hériter ou l’implémenter l’autre.  
  
## <a name="errors-and-failures"></a>Erreurs et échecs  
 `TryCast` génère une erreur du compilateur s’il détecte qu’il n’existe aucune relation d’héritage ou d’implémentation. Mais l’absence d’une erreur du compilateur ne garantit pas une conversion réussie. Si la conversion souhaitée est restrictive, elle peut échouer au moment de l’exécution. Si cela se produit, `TryCast` retourne [rien](../../../visual-basic/language-reference/nothing.md).  
  
## <a name="conversion-keywords"></a>Mots clés de conversion  
 Une comparaison de mots clés de conversion de type est la suivante.  
  
|Mot clé|Types de données|Relation d’argument|Échec d’exécution|  
|---|---|---|---|  
|[CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md)|Les types de données|Conversion restrictive ou étendue doit être défini entre les deux types de données|Lève une exception <xref:System.InvalidCastException>|  
|[DirectCast (opérateur)](../../../visual-basic/language-reference/operators/directcast-operator.md)|Les types de données|Un type doit hériter ou implémenter l’autre type|Lève une exception <xref:System.InvalidCastException>|  
|`TryCast`|Seuls les types référence|Un type doit hériter ou implémenter l’autre type|Retourne [Nothing](../../../visual-basic/language-reference/nothing.md)|  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment utiliser `TryCast`.  
  
 [!code-vb[VbVbalrKeywords#6](../../../visual-basic/language-reference/codesnippet/VisualBasic/trycast-operator_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)  
 [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
