---
title: Mod, opérateur (Visual Basic)
ms.date: 04/24/2018
f1_keywords:
- vb.Mod
helpviewer_keywords:
- remainder (Mod operator)
- division operator [Visual Basic], Mod operator
- modulus operator [Visual Basic], Visual Basic
- Mod operator [Visual Basic]
- operators [Visual Basic], division
- arithmetic operators [Visual Basic], Mod
- math operators [Visual Basic]
ms.assetid: 6ff7e40e-cec8-4c77-bff6-8ddd2791c25b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 456c19fc8e28517a0662b58e338028e1c75cd8c8
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "44756897"
---
# <a name="mod-operator-visual-basic"></a>Mod, opérateur (Visual Basic)
Divise deux nombres et retourne uniquement le reste.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
number1 Mod number2  
```  
  
## <a name="parts"></a>Composants  
 `number1`  
 Obligatoire. Toute expression numérique.  
  
 `number2`  
 Obligatoire. Toute expression numérique.  
  
## <a name="supported-types"></a>Types pris en charge  
 Tous les types numériques. Cela inclut les types non signés et à virgule flottante et `Decimal`.  
  
## <a name="result"></a>Résultat

Le résultat est le reste après `number1` est divisé par `number2`. Par exemple, l’expression `14 Mod 4` renvoie la valeur 2.  

> [!NOTE]
> Il existe une différence entre *reste* et *modulo* en mathématiques, avec des résultats différents pour les nombres négatifs. Le `Mod` opérateur en Visual Basic, le .NET Framework `op_Modulus` opérateur et sous-jacent [rem](<xref:System.Reflection.Emit.OpCodes.Rem>) instruction IL tous effectuer une opération de reste.

Le résultat d’une `Mod` opération conserve le signe du dividende, `number1`, et par conséquent, il peut être positif ou négatif. Le résultat est toujours dans la plage (-`number2`, `number2`), de manière exclusive. Exemple :

```vb
Public Module Example
   Public Sub Main()
      Console.WriteLine($" 8 Mod  3 = {8 Mod 3}")
      Console.WriteLine($"-8 Mod  3 = {-8 Mod 3}")
      Console.WriteLine($" 8 Mod -3 = {8 Mod -3}")
      Console.WriteLine($"-8 Mod -3 = {-8 Mod -3}")
   End Sub
End Module
' The example displays the following output:
'       8 Mod  3 = 2
'      -8 Mod  3 = -2
'       8 Mod -3 = 2
'      -8 Mod -3 = -2
```

## <a name="remarks"></a>Notes  
 Si `number1` ou `number2` est une valeur à virgule flottante, le reste de la division à virgule flottante est retourné. Le type de données du résultat est le plus petit type de données qui peut contenir toutes les valeurs possibles qui résultent de la division avec les types de données de `number1` et `number2`.  
  
 Si `number1` ou `number2` prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), il est considéré comme égal à zéro.  
  
 Les opérateurs connexes sont les suivantes :  
  
-   Le [\, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md) renvoie le quotient entier d’une division. Par exemple, l’expression `14 \ 4` prend la valeur 3.  
  
-   Le [/, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) retourne le quotient complet, y compris le reste, comme un nombre à virgule flottante. Par exemple, l’expression `14 / 4` prend la valeur 3.5.  
  
## <a name="attempted-division-by-zero"></a>Tentative de division par zéro  
 Si `number2` prend la valeur zéro, le comportement de la `Mod` opérateur varie selon le type de données des opérandes. Une division intégrale lève un <xref:System.DivideByZeroException> exception. Retourne une division à virgule flottante <xref:System.Double.NaN>.  
  
## <a name="equivalent-formula"></a>Formule équivalente  
 L’expression `a Mod b` correspond à une des formules suivantes :  
  
 `a - (b * (a \ b))`  
  
 `a - (b * Fix(a / b))`  
  
## <a name="floating-point-imprecision"></a>À virgule flottante imprécision  
 Lorsque vous travaillez avec des nombres à virgule flottante, n’oubliez pas qu’ils n’ont pas toujours de représentation décimale précise dans la mémoire. Cela peut entraîner des résultats inattendus à partir de certaines opérations, comme la comparaison de valeurs et les `Mod` opérateur. Pour plus d’informations, consultez [dépannage des Types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).  
  
## <a name="overloading"></a>Surcharge  
 Le `Mod` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement. Si votre code s’applique `Mod` à une instance d’une classe ou une structure qui inclut une telle surcharge, assurez-vous que vous comprenez son comportement redéfini. Pour plus d’informations, consultez [procédures d’opérateur](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Mod` opérateur diviser deux nombres et retourner uniquement le reste. Si des nombres sont un nombre à virgule flottante, le résultat est un nombre à virgule flottante qui représente le reste.  
  
 [!code-vb[VbVbalrOperators#31](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/mod-operator_1.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre l’imprécision potentielle des opérandes à virgule flottante. Dans la première instruction, les opérandes sont `Double`, et 0,2 représente une fraction binaire se répétant avec une valeur stockée de 0,20000000000000001. Dans la deuxième instruction, le littéral de type caractère `D` force les deux opérandes de `Decimal`, et 0,2 a une représentation précise.  
  
 [!code-vb[VbVbalrOperators#32](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/mod-operator_2.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Conversion.Int%2A>  
 <xref:Microsoft.VisualBasic.Conversion.Fix%2A>  
 [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)  
 [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)  
 [Dépannage des types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)  
 [\, Opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md)
