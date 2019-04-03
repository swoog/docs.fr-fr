---
title: '- Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.Negate
- vb.-
helpviewer_keywords:
- operator [Visual Basic]
- operators [Visual Basic], subtraction
- operators [Visual Basic], difference
- negation operator [Visual Basic]
- operators [Visual Basic], arithmetic
- subtraction operator [Visual Basic], syntax
- arithmetic operators [Visual Basic], subtraction
- difference operator [Visual Basic]
- math operators [Visual Basic]
- operators [Visual Basic], negation
- minus operator [Visual Basic]
ms.assetid: bff2c368-662d-4c92-ac87-1d9bdfd3426a
ms.openlocfilehash: 1a5c47a2f1bc8a8b9e1b0263b90006a0e58e17bb
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58830667"
---
# <a name="--operator-visual-basic"></a>-, opérateur (Visual Basic)
Retourne la différence entre deux expressions numériques ou la valeur négative d’une expression numérique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
      expression1 – expression2  
- or -  
– expression1  
```  
  
## <a name="parts"></a>Composants  
 `expression1`  
 Obligatoire. Toute expression numérique.  
  
 `expression2`  
 Requis sauf si le `–` opérateur calcule une valeur négative. Toute expression numérique.  
  
## <a name="result"></a>Résultat  
 Le résultat est la différence entre `expression1` et `expression2`, ou la valeur négative de `expression1`.  
  
 Le type de données de résultat est un type numérique approprié pour les types de données de `expression1` et `expression2`. Consultez les tableaux « Arithmétique sur les entiers » dans [Types de données de résultats de l’opérateur](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).  
  
## <a name="supported-types"></a>Types pris en charge  
 tous les types numériques Cela inclut les types non signés et à virgule flottante et `Decimal`.  
  
## <a name="remarks"></a>Notes  
 Dans la première utilisation indiquée dans la syntaxe précédente, le `–` opérateur est la *binaire* opérateur de soustraction arithmétique pour la différence entre deux expressions numériques.  
  
 Dans la seconde utilisation indiquée dans la syntaxe précédente, le `–` opérateur est la *unaire* opérateur de négation de la valeur négative d’une expression. Dans ce sens, la négation consiste à inverser le signe de `expression1` afin que le résultat est positif si `expression1` est un nombre négatif.  
  
 Si des expressions a la valeur [rien](../../../visual-basic/language-reference/nothing.md), le `–` opérateur considère comme un zéro.  
  
> [!NOTE]
>  Le `–` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `–` opérateur pour calculer et retourner la différence entre deux nombres, puis comment rendre un nombre négatif.  
  
 [!code-vb[VbVbalrOperators#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#10)]  
  
 Après l’exécution de ces instructions, `binaryResult` contient 124,45 et `unaryResult` contient -334,90.  
  
## <a name="see-also"></a>Voir aussi

- [-=, Opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/subtraction-assignment-operator.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
