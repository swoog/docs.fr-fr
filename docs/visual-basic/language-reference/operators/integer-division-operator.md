---
title: '\, opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.\
- '\'
helpviewer_keywords:
- division operator [Visual Basic], integer
- integer division operator [Visual Basic]
- zero, division by zero
- arithmetic operators [Visual Basic], division
- division [Visual Basic], by zero
- backslash (\) [Visual Basic]
- '\ operator [Visual Basic]'
- integer quotient
- math operators [Visual Basic]
- quotients, integer
- truncation [Visual Basic], integer division
ms.assetid: 4b0ee347-950c-45c9-8e23-54bc85df208e
ms.openlocfilehash: 7ce7bdaa2bcbf2ba67f24c7e129f8f9a03a28c52
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57201909"
---
# <a name="-operator-visual-basic"></a>\, opérateur (Visual Basic)
Divise deux nombres et retourne un résultat entier.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression1 \ expression2  
```  
  
## <a name="parts"></a>Composants  
 `expression1`  
 Obligatoire. Toute expression numérique.  
  
 `expression2`  
 Obligatoire. Toute expression numérique.  
  
## <a name="supported-types"></a>Types pris en charge  
 Tous les types numériques, y compris les types non signés et à virgule flottante et `Decimal`.  
  
## <a name="result"></a>Résultat  
 Le résultat est le quotient entier de `expression1` divisé par `expression2`, qui abandonne tout élément restant et conserve uniquement la partie entière. Il s’agit *troncation*.  
  
 Le type de données de résultat est un type numérique approprié pour les types de données de `expression1` et `expression2`. Consultez les tableaux « Arithmétique sur les entiers » dans [Types de données de résultats de l’opérateur](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).  
  
 Le [/, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) retourne le quotient complet qui conserve le reste dans la partie fractionnaire.  
  
## <a name="remarks"></a>Notes  
 Avant d’effectuer la division, Visual Basic tente de convertir toute expression numérique à virgule flottante à `Long`. Si `Option Strict` est `On`, une erreur du compilateur se produit. Si `Option Strict` est `Off`, un <xref:System.OverflowException> est possible si la valeur est en dehors de la plage de la [Type de données Long](../../../visual-basic/language-reference/data-types/long-data-type.md). La conversion en `Long` est également soumise à *l’arrondi bancaire*. Pour plus d’informations, consultez « Parties fractionnaires » dans [les fonctions de Conversion de Type](../../../visual-basic/language-reference/functions/type-conversion-functions.md).  
  
 Si `expression1` ou `expression2` prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), il est considéré comme égal à zéro.  
  
## <a name="attempted-division-by-zero"></a>Tentative de Division par zéro  
 Si `expression2` correspond à zéro, le `\` opérateur lève un <xref:System.DivideByZeroException> exception. Cela est vrai pour tous les types de données numériques des opérandes.  
  
> [!NOTE]
>  Le `\` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `\` opérateur effectue la division d’entier. Le résultat est un entier qui représente le quotient entier des deux opérandes, avec le reste abandonné.  
  
 [!code-vb[VbVbalrOperators#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#18)]  
  
 Les expressions dans l’exemple précédent retournent des valeurs de 2, 3, 33 et -22, respectivement.  
  
## <a name="see-also"></a>Voir aussi
- [\\=, Opérateur](../../../visual-basic/language-reference/operators/integer-division-assignment-operator.md)
- [/, Opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md)
- [Option Strict (instruction)](../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
