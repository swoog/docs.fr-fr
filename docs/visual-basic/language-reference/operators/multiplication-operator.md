---
title: '* Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.*
helpviewer_keywords:
- arithmetic operators [Visual Basic], multiplication
- operators [Visual Basic], multiplication
- '* operator [Visual Basic]'
- multiplication operator [Visual Basic], syntax
- math operators [Visual Basic]
ms.assetid: 2b210382-99da-4195-89ba-b1d06f5e89ad
ms.openlocfilehash: 09b95585325b05c0b7925c4c1c9e123f45791e10
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61936641"
---
# <a name="-operator-visual-basic"></a>*, opérateur (Visual Basic)
Multiplie deux nombres.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
number1 * number2  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`number1`|Obligatoire. Toute expression numérique.|  
|`number2`|Obligatoire. Toute expression numérique.|  
  
## <a name="result"></a>Résultat  
 Le résultat est le produit de `number1` et `number2`.  
  
## <a name="supported-types"></a>Types pris en charge  
 Tous les types numériques, y compris les types non signés et à virgule flottante et `Decimal`.  
  
## <a name="remarks"></a>Notes  
 Le type de données du résultat dépend des types des opérandes. Le tableau suivant montre comment le type de données du résultat est déterminé.  
  
|Types de données d’opérande|Type de données de résultat|  
|---|---|  
|Les deux expressions sont des types de données intégraux ([SByte](../../../visual-basic/language-reference/data-types/sbyte-data-type.md), [octets](../../../visual-basic/language-reference/data-types/byte-data-type.md), [court](../../../visual-basic/language-reference/data-types/short-data-type.md), [UShort](../../../visual-basic/language-reference/data-types/ushort-data-type.md), [entier](../../../visual-basic/language-reference/data-types/integer-data-type.md), [UInteger](../../../visual-basic/language-reference/data-types/uinteger-data-type.md), [Long](../../../visual-basic/language-reference/data-types/long-data-type.md), [ULong](../../../visual-basic/language-reference/data-types/ulong-data-type.md))|Un type de données numériques approprié pour les types de données de `number1` et `number2`. Consultez les tableaux « Arithmétique sur les entiers » dans [Types de données de résultats de l’opérateur](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).|  
|Les deux expressions sont [décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md)|`Decimal`|  
|Les deux expressions sont [unique](../../../visual-basic/language-reference/data-types/single-data-type.md)|`Single`|  
|Des expressions sont un type de données à virgule flottante (`Single` ou [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)) mais pas les deux `Single` (Remarque `Decimal` n’est pas un type de données à virgule flottante)|`Double`|  
  
 Si une expression correspond à [rien](../../../visual-basic/language-reference/nothing.md), il est considéré comme égal à zéro.  
  
## <a name="overloading"></a>Surcharge  
 Le `*` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `*` opérateur multiplier deux nombres. Le résultat est le produit des deux opérandes.  
  
 [!code-vb[VbVbalrOperators#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#4)]  
  
## <a name="see-also"></a>Voir aussi

- [*= (opérateur)](../../../visual-basic/language-reference/operators/multiplication-assignment-operator.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
