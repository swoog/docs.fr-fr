---
title: '>> Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.>>
helpviewer_keywords:
- operator>>
- '>> operator [Visual Basic]'
- bit shift operators [Visual Basic]
- operator >>
- right shift operators [Visual Basic]
ms.assetid: 054dc6a6-47d9-47ef-82da-cfa2b59fbf8f
ms.openlocfilehash: 8803dc2e25edde756958a243d429dd30c5c78bcf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58816965"
---
# <a name="-operator-visual-basic"></a>>>, Opérateur (Visual Basic)
Effectue un décalage arithmétique vers la droite sur un modèle binaire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
result = pattern >> amount  
```  
  
## <a name="parts"></a>Composants  
 `result`  
 Obligatoire. Valeur numérique entière. Le résultat du décalage du modèle de bit. Le type de données est identique à celui de `pattern`.  
  
 `pattern`  
 Obligatoire. Expression numérique entière. Le modèle de bits à décaler. Le type de données doit être un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).  
  
 `amount`  
 Obligatoire. Expression numérique. Le nombre de bits pour décaler le modèle binaire. Le type de données doit être `Integer` ou s’étendre au `Integer`.  
  
## <a name="remarks"></a>Notes  
 Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité. Dans un décalage arithmétique à droite, les bits décalés au-delà de la position de bit plus à droite sont supprimés, et le bit de plus à gauche (connexion) est propagé vers les positions de bit libérées à gauche. Cela signifie que si `pattern` a une valeur négative, les positions libérées sont définies sur un ; sinon, elles sont définies à zéro.  
  
 Notez que les types de données `Byte`, `UShort`, `UInteger`, et `ULong` sont non signé, il n’existe aucune propagation du bit de signe. Si `pattern` est de type non signé, les positions libérées ont toujours la valeur zéro.  
  
 Pour éviter un décalage des bits plus que peut contenir le résultat, Visual Basic masque la valeur de `amount` avec un masque de taille correspondant au type de données de `pattern`. L’opération AND binaire de ces valeurs est utilisé pour le décalage. Les masques de taille sont les suivantes :  
  
|Type de données `pattern`|Masque de taille (décimal)|Masque de taille (hexadécimal)|  
|----------------------------|---------------------------|-------------------------------|  
|`SByte`, `Byte`|7|&H00000007|  
|`Short`, `UShort`|15|&H0000000F|  
|`Integer`, `UInteger`|31|&H0000001F|  
|`Long`, `ULong`|63|&H0000003F|  
  
 Si `amount` est égal à zéro, la valeur de `result` est identique à la valeur de `pattern`. Si `amount` est négatif, il est considéré comme une valeur non signée et masquée avec le masque de taille appropriée.  
  
 Les décalages arithmétiques ne génèrent jamais des exceptions de dépassement de capacité.  
  
## <a name="overloading"></a>Surcharge  
 Le `>>` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `>>` opérateur pour effectuer des décalages arithmétiques vers la droite sur des valeurs intégrales. Le résultat a toujours les données de mêmes type que celui de l’expression décalée.  
  
 [!code-vb[VbVbalrOperators#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#14)]  
  
 Les résultats de l’exemple précédent sont les suivantes :  
  
-   `result1` est 2560 (0000 1010 0000 0000).  
  
-   `result2` est de 160 (0000 0000 1010 0000).  
  
-   `result3` est 2 (0000 0000 0000 0010).  
  
-   `result4` est 640 (0000 0010 1000 0000).  
  
-   `result5` est égal à 0 (décalé de 15 places à droite).  
  
 Le nombre de positions de décalage pour `result4` est calculé comme 18 et 15, ce qui est égal à 2.  
  
 L’exemple suivant montre les décalages arithmétiques sur une valeur négative.  
  
 [!code-vb[VbVbalrOperators#55](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#55)]  
  
 Les résultats de l’exemple précédent sont les suivantes :  
  
-   `negresult1` is -512 (1111 1110 0000 0000).  
  
-   `negresult2` est -1 (le bit de signe est propagé).  
  
## <a name="see-also"></a>Voir aussi

- [Opérateurs de décalage de bits](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [>>= (opérateur)](../../../visual-basic/language-reference/operators/right-shift-assignment-operator.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
