---
title: Opérateurs de comparaison en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- comparison operators [Visual Basic], comparing strings
- comparison operators [Visual Basic], comparing objects
- strings [Visual Basic], comparing
- comparison operators [Visual Basic]
- string comparison [Visual Basic], operators
- objects [Visual Basic], comparing
- numbers [Visual Basic], comparing
- Visual Basic code, operators
- string comparison [Visual Basic]
- numeric values [Visual Basic], comparing
- comparison operators [Visual Basic], comparing numeric values
- operators [Visual Basic], comparison
ms.assetid: 0b570339-5407-474f-8421-e183a8b303ee
ms.openlocfilehash: d08974a929a723d4037300f9d72ae03c072d47fa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58826156"
---
# <a name="comparison-operators-in-visual-basic"></a>Opérateurs de comparaison en Visual Basic
Opérateurs de comparaison comparent deux expressions et retournent un `Boolean` valeur qui représente la relation de leurs valeurs. Il existe des opérateurs pour comparer des valeurs numériques, des opérateurs de comparaison de chaînes et des opérateurs pour comparer des objets. Les trois types d’opérateurs sont abordées dans cet article.  
  
## <a name="comparing-numeric-values"></a>Comparer des valeurs numériques  
 Visual Basic compare des valeurs numériques à l’aide de six opérateurs de comparaison numériques. Chaque opérateur accepte comme opérandes deux expressions qui correspondent à des valeurs numériques. Le tableau suivant répertorie les opérateurs et présente des exemples de chacun d’eux.  
  
|Opérateur|Condition testée|Exemples|  
|--------------|----------------------|--------------|  
|`=` (Égalité)|Est la valeur de la première expression égale à la valeur de la seconde ?|`23`   `=`   `33    ' False`<br /><br /> `23`   `=`   `23    ' True`<br /><br /> `23`   `=`   `12    ' False`|  
|`<>` (Inégalité)|La valeur de la première expression n’est pas égale à la valeur de la seconde ?|`23`   `<>`   `33    ' True`<br /><br /> `23`   `<>`   `23    ' False`<br /><br /> `23`   `<>`   `12    ' True`|  
|`<` (Inférieur à)|Est la valeur de la première expression inférieure à la valeur de la seconde ?|`23`   `<`   `33    ' True`<br /><br /> `23`   `<`   `23    ' False`<br /><br /> `23`   `<`   `12    ' False`|  
|`>` (Supérieur à)|La valeur de la première expression est supérieure à la valeur de la seconde ?|`23`   `>`   `33    ' False`<br /><br /> `23`   `>`   `23    ' False`<br /><br /> `23`   `>`   `12    ' True`|  
|`<=` (Inférieur ou égal à)|Est la valeur de la première expression inférieure ou égale à la valeur de la seconde ?|`23`   `<=`   `33    ' True`<br /><br /> `23`   `<=`   `23    ' True`<br /><br /> `23`   `<=`   `12    ' False`|  
|`>=` (Supérieur ou égal à)|Est la valeur de la première expression supérieure ou égale à la valeur de la seconde ?|`23`   `>=`   `33    ' False`<br /><br /> `23`   `>=`   `23    ' True`<br /><br /> `23`   `>=`   `12    ' True`|  
  
## <a name="comparing-strings"></a>Comparaison de chaînes  
 Visual Basic compare des chaînes à l’aide de la [opérateur Like](../../../../visual-basic/language-reference/operators/like-operator.md) , ainsi que les opérateurs de comparaison numériques. Le `Like` opérateur vous permet de spécifier un modèle. La chaîne est ensuite comparée au modèle, et si elle correspond, le résultat est `True`. Sinon, le résultat est `False`. Les opérateurs numériques permettent de comparer `String` valeurs selon leur ordre de tri, comme le montre l’exemple suivant.  
  
 `"73" < "9"`  
  
 `' The result of the preceding comparison is True.`  
  
 Le résultat dans l’exemple précédent est `True` car le premier caractère dans la première chaîne est trié avant le premier caractère dans la deuxième chaîne. Si les premiers caractères sont égales, la comparaison continuer jusqu’au caractère suivant dans les deux chaînes et ainsi de suite. Vous pouvez également tester l’égalité des chaînes à l’aide de l’opérateur d’égalité, comme le montre l’exemple suivant.  
  
 `"734" = "734"`  
  
 `' The result of the preceding comparison is True.`  
  
 Si une chaîne est un préfixe d’un autre, tels que « aa » et « aaa », la plus longue chaîne est considéré comme supérieur à la chaîne plus courte. L'exemple suivant illustre ce comportement.  
  
 `"aaa" > "aa"`  
  
 `' The result of the preceding comparison is True.`  
  
 L’ordre de tri est basé sur une comparaison binaire ou une comparaison textuelle selon le paramètre de `Option Compare`. Pour plus d’informations, consultez [instruction Option Compare](../../../../visual-basic/language-reference/statements/option-compare-statement.md).  
  
## <a name="comparing-objects"></a>Comparaison d’objets  
 Visual Basic compare deux variables de référence d’objet avec la [opérateur Is](../../../../visual-basic/language-reference/operators/is-operator.md) et [opérateur IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md). Vous pouvez utiliser un de ces opérateurs pour déterminer si deux variables de référence font référence à la même instance d’objet. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbalrOperators#65](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#65)]  
  
 Dans l’exemple précédent, `x Is y` prend la valeur `True`, car les deux variables font référence à la même instance. Comparez ce résultat à l’exemple suivant.  
  
 [!code-vb[VbVbalrOperators#66](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#66)]  
  
 Dans l’exemple précédent, `x Is y` prend la valeur `False`, car bien que les variables font référence aux objets du même type, ils font référence à différentes instances de ce type.  
  
 Lorsque vous souhaitez tester deux objets ne pointe ne pas vers la même instance, le `IsNot` opérateur vous permet d’éviter une combinaison grammaticalement maladroite de `Not` et `Is`. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbalrOperators#67](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#67)]  
  
 Dans l’exemple précédent, `If a IsNot b` équivaut à `If Not a Is b`.  
  
### <a name="comparing-object-type"></a>Comparaison de Type d’objet  
 Vous pouvez tester si un objet est d’un type particulier avec le `TypeOf`... `Is` expression. La syntaxe est la suivante :  
  
 `TypeOf <objectexpression> Is <typename>`  
  
 Lorsque `typename` spécifie un type d’interface, puis le `TypeOf`... `Is` expression retourne `True` si l’objet implémente le type d’interface. Lorsque `typename` est un type de classe, l’expression retourne `True` si l’objet est une instance de la classe spécifiée ou d’une classe qui dérive de la classe spécifiée. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbalrOperators#68](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#68)]  
  
 Dans l’exemple précédent, le `TypeOf x Is Control` expression prend la valeur `True` , car le type de `x` est `Button`, qui hérite de `Control`.  
  
 Pour plus d’informations, consultez [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md).  
  
## <a name="see-also"></a>Voir aussi

- [Comparaisons de valeurs](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md)
- [Opérateurs de comparaison](../../../../visual-basic/language-reference/operators/comparison-operators.md)
- [Opérateurs](../../../../visual-basic/language-reference/operators/index.md)
- [Opérateurs arithmétiques en Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
- [Opérateurs de concaténation dans Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/concatenation-operators.md)
- [Opérateurs logiques et au niveau du bit en Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
