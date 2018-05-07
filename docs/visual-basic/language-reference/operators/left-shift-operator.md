---
title: '&lt;&lt; Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.<<
helpviewer_keywords:
- bit shift operators [Visual Basic]
- << operator [Visual Basic]
- operator <<, Visual Basic left shift operator
ms.assetid: fdb93d25-81ba-417f-b808-41207bfb8440
ms.openlocfilehash: bdec015309526aeac2499bc7b459b6ccab6f1e4d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="ltlt-operator-visual-basic"></a>&lt;&lt; Opérateur (Visual Basic)
Effectue un décalage arithmétique vers la gauche sur un modèle binaire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
result = pattern << amount  
```  
  
## <a name="parts"></a>Composants  
 `result`  
 Obligatoire. Valeur numérique intégrale. Le résultat du décalage du modèle binaire. Le type de données est identique à celle de `pattern`.  
  
 `pattern`  
 Obligatoire. Expression numérique intégrale. Le modèle de bits à décaler. Le type de données doit être un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).  
  
 `amount`  
 Obligatoire. Expression numérique. Le nombre de bits à décaler le modèle binaire. Le type de données doit être `Integer` ou s’étendre à `Integer`.  
  
## <a name="remarks"></a>Notes  
 Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité. Dans un décalage arithmétique vers la gauche, les bits décalés au-delà de la plage du type de données du résultat sont ignorés, et les positions de bit libérées à droite sont définies à zéro.  
  
 Pour éviter un décalage en plus de bits que peut en contenir le résultat, Visual Basic masque la valeur de `amount` avec un masque de taille qui correspond au type de données de `pattern`. L’opérateur binaire AND de ces valeurs est utilisé pour le décalage. Les masques de taille sont les suivantes :  
  
|Type de données `pattern`|Masque de taille (décimal)|Masque de taille (hexadécimal)|  
|----------------------------|---------------------------|-------------------------------|  
|`SByte`, `Byte`|7|&AMP; H00000007|  
|`Short`, `UShort`|15|&AMP; H0000000F|  
|`Integer`, `UInteger`|31|&AMP; H0000001F|  
|`Long`, `ULong`|63|&AMP; H0000003F|  
  
 Si `amount` est égal à zéro, la valeur de `result` est identique à la valeur de `pattern`. Si `amount` est négatif, il est considéré comme une valeur non signée et masquée avec le masque de la taille appropriée.  
  
 Les décalages arithmétiques ne génèrent jamais des exceptions de dépassement de capacité.  
  
> [!NOTE]
>  Le `<<` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, assurez-vous que vous comprenez son comportement redéfini. Pour plus d’informations, consultez [procédures d’opérateur](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `<<` opérateur pour effectuer une opération arithmétique gauche des équipes sur des valeurs intégrales. Le résultat a toujours les mêmes données de type que celui de l’expression décalée.  
  
 [!code-vb[VbVbalrOperators#12](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/left-shift-operator_1.vb)]  
  
 Les résultats de l’exemple précédent sont les suivantes :  
  
-   `result1` est 192 (0000 0000 1100 0000).  
  
-   `result2` est 3072 (0000 1100 0000 0000).  
  
-   `result3` est-32 768 (1000 0000 0000 0000).  
  
-   `result4` est 384 (0000 0001 1000 0000).  
  
-   `result5` est égal à 0 (décalé de 15 places vers la gauche).  
  
 Le nombre de positions de décalage pour `result4` est calculé comme 17 AND 15, ce qui est égal à 1.  
  
## <a name="see-also"></a>Voir aussi  
 [Opérateurs de décalage de bits](../../../visual-basic/language-reference/operators/bit-shift-operators.md)  
 [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)  
 [<<= (opérateur)](../../../visual-basic/language-reference/operators/left-shift-assignment-operator.md)  
 [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)  
 [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
