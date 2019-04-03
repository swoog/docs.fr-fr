---
title: Priorité des opérateurs en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- arithmetic operators [Visual Basic], precedence
- operator precedence
- logical operators [Visual Basic], precedence
- operators [Visual Basic], associativity
- operators [Visual Basic], resolution
- associativity of operators [Visual Basic]
- operators [Visual Basic], precedence
- precedence [Visual Basic], of operators
- comparison operators [Visual Basic], precedence
- math operators [Visual Basic]
- order of precedence
ms.assetid: cbbdb282-f572-458e-a520-008a675f8063
ms.openlocfilehash: 568927eb4759c214311ad34a5b45e28094dd80be
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58830030"
---
# <a name="operator-precedence-in-visual-basic"></a>Priorité des opérateurs en Visual Basic
Lorsque plusieurs opérations se produisent dans une expression, chaque partie est évaluée et résolue dans un ordre prédéterminé *priorité des opérateurs*.  
  
## <a name="precedence-rules"></a>Règles de priorité  
 Les expressions contenant des opérateurs à partir de plusieurs catégories, ils sont évalués selon les règles suivantes :  
  
-   Les opérateurs arithmétiques et de concaténation ont l’ordre de priorité décrite dans la section suivante, et que tous ont une priorité supérieure à celle de la comparaison, logiques et les opérateurs au niveau du bit.  
  
-   Tous les opérateurs de comparaison ont la même priorité et avoir une priorité supérieure à celle des opérateurs logiques et au niveau du bit, mais une priorité inférieure à celle des opérateurs arithmétiques et de concaténation.  
  
-   Les opérateurs logiques et au niveau du bit ont l’ordre de priorité décrite dans la section suivante, et leur priorité inférieure à celle des opérations arithmétiques, concaténation, les opérateurs de comparaison.  
  
-   Opérateurs ayant la même priorité sont évalués de gauche à droite dans l’ordre dans lequel ils apparaissent dans l’expression.  
  
## <a name="precedence-order"></a>Ordre de priorité  
 Les opérateurs sont évalués dans l’ordre de priorité suivant :  
  
### <a name="await-operator"></a>Await, opérateur  
 Await  
  
### <a name="arithmetic-and-concatenation-operators"></a>Opérations arithmétiques et les opérateurs de concaténation  
 Élévation (`^`)  
  
 Unaire identité et la négation (`+`, `–`)  
  
 Multiplication et division à virgule flottante (`*`, `/`)  
  
 Division d’entier (`\`)  
  
 Modulo arithmétique (`Mod`)  
  
 Addition et soustraction (`+`, `–`)  
  
 Concaténation de chaînes (`&`)  
  
 Décalage de bits arithmétique (`<<`, `>>`)  
  
### <a name="comparison-operators"></a>Opérateurs de comparaison  
 Tous les opérateurs de comparaison (`=`, `<>`, `<`, `<=`, `>`, `>=`, `Is`, `IsNot`, `Like`, `TypeOf`... `Is`)  
  
### <a name="logical-and-bitwise-operators"></a>Opérateurs de bits et opérateurs logiques  
 Négation (`Not`)  
  
 Association (`And`, `AndAlso`)  
  
 Disjonction inclusive (`Or`, `OrElse`)  
  
 Disjonction exclusive (`Xor`)  
  
### <a name="comments"></a>Commentaires  
 Le `=` opérateur est uniquement l’opérateur d’égalité, pas l’opérateur d’assignation.  
  
 L’opérateur de concaténation de chaîne (`&`) n’est pas un opérateur arithmétique, mais il est groupé avec les opérateurs arithmétiques priorités.  
  
 Le `Is` et `IsNot` opérateurs sont des opérateurs de comparaison de référence objet. Ils ne comparent pas les valeurs de deux objets ; ils vérifient uniquement pour déterminer si deux variables d’objet font référence à la même instance d’objet.  
  
## <a name="associativity"></a>l'associativité  
 Lorsque les opérateurs de même priorité apparaissent ensemble dans une expression, par exemple multiplication et division, le compilateur évalue chaque opération qu’elle rencontre de gauche à droite. L'exemple suivant illustre ce comportement.  
  
```  
Dim n1 As Integer = 96 / 8 / 4  
Dim n2 As Integer = (96 / 8) / 4  
Dim n3 As Integer = 96 / (8 / 4)  
```  
  
 La première expression évalue la division 96 / 8 (ce qui entraîne à 12), puis la division 12 / 4, ce qui se traduit dans trois. Étant donné que le compilateur évalue les opérations pour `n1` de gauche à droite, la version d’évaluation est le même lorsque cet ordre est indiqué explicitement pour `n2`. Les deux `n1` et `n2` ont pour résultat trois. En revanche, `n3` a un résultat de 48, étant donné que les parenthèses forcent le compilateur à évaluer 8 / 4 première.  
  
 Étant donné ce comportement, les opérateurs sont dits *associatifs sur leur gauche* en Visual Basic.  
  
## <a name="overriding-precedence-and-associativity"></a>Substitution de priorité et associativité  
 Vous pouvez utiliser des parenthèses pour forcer certaines parties d’une expression à évaluer avant les autres. Cela peut remplacer l’ordre de priorité et l’associativité de gauche. Visual Basic exécute toujours les opérations qui sont placées entre parenthèses avant celles en dehors. Toutefois, dans les parenthèses, il maintient ordinaire priorité et associativité, sauf si vous utilisez des parenthèses dans les parenthèses. L'exemple suivant illustre ce comportement.  
  
```  
Dim a, b, c, d, e, f, g As Double  
a = 8.0  
b = 3.0  
c = 4.0  
d = 2.0  
e = 1.0  
f = a - b + c / d * e  
' The preceding line sets f to 7.0. Because of natural operator   
' precedence and associativity, it is exactly equivalent to the   
' following line.  
f = (a - b) + ((c / d) * e)  
' The following line overrides the natural operator precedence   
' and left associativity.  
g = (a - (b + c)) / (d * e)  
' The preceding line sets g to 0.5.  
```  
  
## <a name="see-also"></a>Voir aussi

- [= (opérateur)](../../../visual-basic/language-reference/operators/assignment-operator.md)
- [Is (opérateur)](../../../visual-basic/language-reference/operators/is-operator.md)
- [IsNot (opérateur)](../../../visual-basic/language-reference/operators/isnot-operator.md)
- [Like (opérateur)](../../../visual-basic/language-reference/operators/like-operator.md)
- [TypeOf (opérateur)](../../../visual-basic/language-reference/operators/typeof-operator.md)
- [Await (opérateur)](../../../visual-basic/language-reference/operators/await-operator.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs et expressions](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
