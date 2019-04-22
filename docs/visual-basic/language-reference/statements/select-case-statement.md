---
title: Select...Case, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Select
- vb.Case
helpviewer_keywords:
- Select statement [Visual Basic]
- Case statement [Visual Basic]
- Select...Case statements
- conditional statements [Visual Basic], Select Case
- control flow [Visual Basic], branching
- Else keyword [Visual Basic], in Select...Case statements
- execution [Visual Basic], conditional
- To keyword [Visual Basic], in Select...Case statements
- Select Case statement [Visual Basic], Select...Case
- Select statement [Visual Basic], Select...Case
- Is operator [Visual Basic], in Select...Case statements
- branching [Visual Basic], conditional
- Case Else statement [Visual Basic], Select...Case
- End keyword [Visual Basic], Select Case statements
- Case statement [Visual Basic], Select...Case
ms.assetid: 68877b65-5419-4bf0-a465-20cd0e4c7d44
ms.openlocfilehash: f99db4f1dc224e5f75ee67ba94c3745f28438724
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58814612"
---
# <a name="selectcase-statement-visual-basic"></a>Select...Case, instruction (Visual Basic)
Exécute l’un des groupes d’instructions, selon la valeur d’une expression.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Select [ Case ] testexpression  
    [ Case expressionlist  
        [ statements ] ]  
    [ Case Else  
        [ elsestatements ] ]  
End Select  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`testexpression`|Obligatoire. expression. Doit correspondre à un des types de données élémentaires (`Boolean`, `Byte`, `Char`, `Date`, `Double`, `Decimal`, `Integer`, `Long`, `Object`, `SByte`, `Short`, `Single`, `String`, `UInteger`, `ULong`, et `UShort`).|  
|`expressionlist`|Requis dans un `Case` instruction. Liste des clauses d’expression représentant les valeurs correspondantes pour `testexpression`. Plusieurs clauses d’expression sont séparées par des virgules. Chaque clause peut prendre une des formes suivantes :<br /><br /> -   *expression1* `To` *expression2*<br />-   [ `Is` ] *comparisonoperator* *expression*<br />-   *expression*<br /><br /> Utilisez le `To` mot clé pour spécifier les limites d’une plage de correspondance des valeurs `testexpression`. La valeur de `expression1` doit être inférieure ou égale à la valeur de `expression2`.<br /><br /> Utilisez le `Is` mot clé avec un opérateur de comparaison (`=`, `<>`, `<`, `<=`, `>`, ou `>=`) pour spécifier une restriction sur les valeurs correspondantes pour `testexpression`. Si le `Is` mot clé n’est pas fourni, il est automatiquement insérée avant *comparisonoperator*.<br /><br /> Le formulaire en spécifiant uniquement `expression` est traité comme un cas spécial de la `Is` forment where *comparisonoperator* est le signe égal (`=`). Ce formulaire est évalué comme `testexpression`  =  `expression`.<br /><br /> Les expressions dans `expressionlist` peut être n’importe quel type de données, à condition qu’ils soient implicitement convertibles au type de `testexpression` approprié `comparisonoperator` est valide pour les deux types avec lesquels il est utilisé.|  
|`statements`|Facultatif. Une ou plusieurs instructions qui suivent `Case` s’exécutent si `testexpression` correspond à une clause dans `expressionlist`.|  
|`elsestatements`|Facultatif. Une ou plusieurs instructions qui suivent `Case Else` s’exécutent si `testexpression` ne correspond pas à une clause dans la `expressionlist` de n’importe quel de la `Case` instructions.|  
|`End Select`|Termine la définition de la `Select`... `Case` construction.|  
  
## <a name="remarks"></a>Notes  
 Si `testexpression` correspondant à une `Case` `expressionlist` clause, les instructions qui suivent `Case` instruction s’exécuter jusqu'à la prochaine `Case`, `Case Else`, ou `End Select` instruction. Le contrôle passe à l’instruction qui suit ensuite `End Select`. Si `testexpression` correspond à un `expressionlist` clause dans plusieurs `Case` clause, seules les instructions qui suivent la première correspondance exécutées.  
  
 Le `Case Else` instruction est utilisée pour présenter le `elsestatements` à exécuter si aucune correspondance n’est trouvée entre la `testexpression` et un `expressionlist` clause dans d’autres `Case` instructions. Bien que non obligatoire, il est judicieux d’avoir un `Case Else` instruction dans votre `Select Case` construction pour gérer imprévus `testexpression` valeurs. Si aucun `Case` `expressionlist` clause correspond à `testexpression` et qu’il existe aucune `Case Else` instruction, le contrôle passe à l’instruction qui suit `End Select`.  
  
 Vous pouvez utiliser plusieurs expressions ou plages dans chaque `Case` clause. Par exemple, la ligne suivante est valide.  
  
 `Case 1 To 4, 7 To 9, 11, 13, Is > maxNumber`  
  
> [!NOTE]
>  Le `Is` mot clé utilisé dans le `Case` et `Case Else` instructions n’est pas le même que le [opérateur Is](../../../visual-basic/language-reference/operators/is-operator.md), qui est utilisé pour la comparaison de référence d’objet.  
  
 Vous pouvez spécifier des plages et des expressions multiples pour les chaînes de caractères. Dans l’exemple suivant, `Case` correspond à n’importe quelle chaîne qui est exactement égal à « pommes », a une valeur entre « nuts » et « a » dans l’ordre alphabétique ou contient la même valeur exacte que la valeur actuelle de `testItem`.  
  
 `Case "apples", "nuts" To "soup", testItem`  
  
 Le paramètre de `Option Compare` peut affecter les comparaisons de chaînes. Sous `Option Compare Text`, les chaînes « Apples » et « apples » considérés comme égaux, mais sous `Option Compare Binary`, ils ne sont pas.  
  
> [!NOTE]
>  Un `Case` instruction avec plusieurs clauses peut exposer un comportement appelé *court-circuit*. Visual Basic évalue les clauses de gauche à droite et si une correspondance existe avec `testexpression`, les autres clauses ne sont pas évaluées. Court-circuit peut améliorer les performances, mais il peut produire des résultats inattendus si vous attendez chaque expression dans `expressionlist` à évaluer. Pour plus d’informations sur le court-circuit, consultez [Expressions booléennes](../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md).  
  
 Si le code dans un `Case` ou `Case Else` bloc d’instructions ne doit-elle pas exécuter d’autres instructions dans le bloc, il peut quitter le bloc à l’aide de la `Exit Select` instruction. Il transfère le contrôle immédiatement à l’instruction qui suit `End Select`.  
  
 `Select Case` constructions peuvent être imbriquées. Chaque imbriqués `Select Case` construction doit avoir une correspondance `End Select` instruction et doit être entièrement contenue dans un seul `Case` ou `Case Else` bloc d’instructions d’externe `Select Case` construction dans laquelle elle est imbriquée.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un `Select Case` construction d’écrire une ligne correspondant à la valeur de la variable `number`. La seconde `Case` instruction contient la valeur qui correspond à la valeur actuelle de `number`, de sorte que l’instruction qui écrit « entre 6 et 8, inclusif » s’exécute.  
  
 [!code-vb[VbVbalrStatements#54](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#54)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Interaction.Choose%2A>
- [End (instruction)](../../../visual-basic/language-reference/statements/end-statement.md)
- [If...Then...Else (instruction)](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [Option Compare (instruction)](../../../visual-basic/language-reference/statements/option-compare-statement.md)
- [Exit (instruction)](../../../visual-basic/language-reference/statements/exit-statement.md)
