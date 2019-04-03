---
title: Opérateur DirectCast (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.directCast
- directCast
helpviewer_keywords:
- DirectCast keyword [Visual Basic]
ms.assetid: 63e5a1d0-4d9e-4732-bf8f-e90c0c8784b8
ms.openlocfilehash: 628ce4f06b91d0f514f71dea3aad8ea0fee6dccf
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58821502"
---
# <a name="directcast-operator-visual-basic"></a>Opérateur DirectCast (Visual Basic)
Introduit une opération de conversion de type en fonction d’héritage ou d’implémentation.  
  
## <a name="remarks"></a>Notes  
 `DirectCast` n’utilise pas le routines d’assistance d’exécution pour la conversion, donc il peut fournir un peu de meilleures performances que Visual Basic `CType` lors de la conversion vers et depuis le type de données `Object`.  
  
 Vous utilisez le `DirectCast` mot clé similaire à la façon dont vous utilisez le [CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md) et [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md) mot clé. Vous fournissez une expression comme le premier argument et un type pour le convertir comme deuxième argument. `DirectCast` nécessite une relation d’héritage ou d’implémentation entre les types de données des deux arguments. Cela signifie qu’un type doit hériter ou implémenter l’autre.  
  
## <a name="errors-and-failures"></a>Erreurs et échecs  
 `DirectCast` génère une erreur du compilateur s’il détecte qu’il n’existe aucune relation d’héritage ou d’implémentation. Mais l’absence d’une erreur du compilateur ne garantit pas une conversion réussie. Si la conversion souhaitée est restrictive, il peut échouer au moment de l’exécution. Si cela se produit, le runtime lève une <xref:System.InvalidCastException> erreur.  
  
## <a name="conversion-keywords"></a>Mots clés de conversion  
 Voici une comparaison des mots clés de conversion de type.  
  
|Mot clé|Types de données|Relation d’argument|Échec d’exécution|  
|---|---|---|---|  
|[CType (fonction)](../../../visual-basic/language-reference/functions/ctype-function.md)|Les types de données|Conversion restrictive ou étendue doit être défini entre les deux types de données|Lève <xref:System.InvalidCastException>|  
|`DirectCast`|Les types de données|Un type doit hériter ou implémenter l’autre type|Lève <xref:System.InvalidCastException>|  
|[TryCast (opérateur)](../../../visual-basic/language-reference/operators/trycast-operator.md)|Seuls les types de référence|Un type doit hériter ou implémenter l’autre type|Retourne [Nothing](../../../visual-basic/language-reference/nothing.md)|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre deux utilisations de `DirectCast`, une qui échoue au moment de l’exécution et l’autre qui réussit.  
  
 [!code-vb[VbVbalrKeywords#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#1)]  
  
 Dans l’exemple précédent, type de la durée d’exécution de `q` est `Double`. `CType` réussit car `Double` peut être converti en `Integer`. Toutefois, la première `DirectCast` échoue au moment de l’exécution, car le type de la durée d’exécution de `Double` n’a aucune relation d’héritage avec `Integer`, même s’il existe une conversion. La seconde `DirectCast` réussit car elle convertit du type <xref:System.Windows.Forms.Form> à taper <xref:System.Windows.Forms.Control>, à partir de laquelle <xref:System.Windows.Forms.Form> hérite.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Convert.ChangeType%2A?displayProperty=nameWithType>
- [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
