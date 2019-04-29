---
title: <<, Opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.<<
helpviewer_keywords:
- bit shift operators [Visual Basic]
- << operator [Visual Basic]
- operator <<, Visual Basic left shift operator
ms.assetid: fdb93d25-81ba-417f-b808-41207bfb8440
ms.openlocfilehash: 75c16c27dc919ba365cbe3c28c61a1e46496b0ae
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768288"
---
# <a name="-operator-visual-basic"></a>\<\< Opérateur (Visual Basic)
Effectue un décalage arithmétique vers la gauche sur un modèle binaire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
result = pattern << amount  
```  
  
## <a name="parts"></a>Composants  
 `result`  
 Obligatoire. Valeur numérique entière. Le résultat du décalage du modèle de bit. Le type de données est identique à celui de `pattern`.  
  
 `pattern`  
 Obligatoire. Expression numérique entière. Le modèle de bits à décaler. Le type de données doit être un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).  
  
 `amount`  
 Obligatoire. Expression numérique. Le nombre de bits pour décaler le modèle binaire. Le type de données doit être `Integer` ou s’étendre au `Integer`.  
  
## <a name="remarks"></a>Notes  
 Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité. Dans un décalage arithmétique vers la gauche, les bits décalés au-delà de la plage du type de données de résultat sont ignorés, et les positions binaires libérées à droite sont définies à zéro.  
  
 Pour éviter un décalage en plus de bits que le résultat peut contenir, Visual Basic masque la valeur de `amount` avec un masque de taille qui correspond au type de données de `pattern`. L’opération AND binaire de ces valeurs est utilisé pour le décalage. Les masques de taille sont les suivantes :  
  
|Type de données `pattern`|Masque de taille (décimal)|Masque de taille (hexadécimal)|  
|----------------------------|---------------------------|-------------------------------|  
|`SByte`, `Byte`|7|&H00000007|  
|`Short`, `UShort`|15|&H0000000F|  
|`Integer`, `UInteger`|31|&H0000001F|  
|`Long`, `ULong`|63|&H0000003F|  
  
 Si `amount` est égal à zéro, la valeur de `result` est identique à la valeur de `pattern`. Si `amount` est négatif, il est considéré comme une valeur non signée et masquée avec le masque de taille appropriée.  
  
 Les décalages arithmétiques ne génèrent jamais des exceptions de dépassement de capacité.  
  
> [!NOTE]
>  Le `<<` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `<<` opérateur pour effectuer une opération arithmétique gauche décale sur des valeurs intégrales. Le résultat a toujours les données de mêmes type que celui de l’expression décalée.  
  
 [!code-vb[VbVbalrOperators#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#12)]  
  
 Les résultats de l’exemple précédent sont les suivantes :  
  
- `result1` is 192 (0000 0000 1100 0000).  
  
- `result2` is 3072 (0000 1100 0000 0000).  
  
- `result3` is -32768 (1000 0000 0000 0000).  
  
- `result4` is 384 (0000 0001 1000 0000).  
  
- `result5` est égal à 0 (décalé de 15 places vers la gauche).  
  
 Le nombre de positions de décalage pour `result4` est calculé comme 17 AND 15, ce qui est égal à 1.  
  
## <a name="see-also"></a>Voir aussi

- [Opérateurs de décalage de bits](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<<= (opérateur)](../../../visual-basic/language-reference/operators/left-shift-assignment-operator.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
