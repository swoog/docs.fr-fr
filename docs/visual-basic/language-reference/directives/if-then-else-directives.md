---
title: '#If... Then... #Else, Directives (Visual Basic)'
ms.date: 04/11/2018
f1_keywords:
- vb.#EndIf
- '#End If'
- '#Then'
- '#ElseIf'
- vb.#ElseIf
- vb.#Else
- vb.#If
helpviewer_keywords:
- Visual Basic code, compiling
- '#If directive [Visual Basic]'
- conditional compilation [Visual Basic], directives
- '#End if directive [Visual Basic]'
- selective compiling
- else directive (#else)
- '#Else directive [Visual Basic]'
ms.assetid: 10bba104-e3fd-451b-b672-faa472530502
ms.openlocfilehash: 8c0aece749edf144fdd5c8ede9ec7e2e4c96ad54
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58823387"
---
# <a name="ifthenelse-directives"></a>#If...Then...#Else, directives
Compilation conditionnelle des blocs de code Visual Basic sélectionnés.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
#If expression Then  
   statements  
[ #ElseIf expression Then  
   [ statements ]  
...  
#ElseIf expression Then  
   [ statements ] ]  
[ #Else  
   [ statements ] ]  
#End If  
```  
  
## <a name="parts"></a>Composants  
 `expression`  
 Requis pour `#If` et `#ElseIf` instructions, facultatives ailleurs. Toute expression, exclusivement consistant en une ou plusieurs constantes de compilation conditionnelle, les littéraux et les opérateurs, qui prend la valeur `True` ou `False`.  
  
 `statements`  
 Requis pour `#If` instruction bloc, facultatif ailleurs. Lignes de programme Visual Basic ou des directives de compilateur qui sont compilés si l’expression associée prend la valeur `True`.  
  
 `#End If`  
 Met fin à la `#If` bloc d’instructions.  
  
## <a name="remarks"></a>Notes  
 Sur la surface, le comportement de la `#If...Then...#Else` directives semble être le même que celui de la `If...Then...Else` instructions. Toutefois, le `#If...Then...#Else` directives évaluent ce qui est compilé par le compilateur, alors que le `If...Then...Else` instructions évaluent les conditions au moment de l’exécution.  
  
 Compilation conditionnelle est généralement utilisée pour compiler le même programme sur différentes plateformes. Il est également utilisé pour empêcher le débogage de code d’apparaître dans un fichier exécutable. Code exclu durant la compilation conditionnelle est totalement absent du fichier exécutable final, afin qu’il n’a aucun effet sur la taille ou de performances.  
  
 Quel que soit le résultat des évaluations, toutes les expressions sont évaluées à l’aide de `Option Compare Binary`. Le `Option Compare` instruction n’affecte pas les expressions dans `#If` et `#ElseIf` instructions.  
  
> [!NOTE]
>  Aucune forme d’une ligne de la `#If`, `#Else`, `#ElseIf`, et `#End If` directives existe. Aucun autre code ne peut apparaître sur la même ligne qu’une des directives. 

Les instructions dans un bloc de compilation conditionnelle doivent être complète logique. Par exemple, vous ne pouvez pas effectuer une compilation conditionnelle uniquement les attributs d’une fonction, mais vous pouvez déclarer conditionnelle de la fonction, ainsi que ses attributs :

```vb
   #If DEBUG Then
   <WebMethod()>
   Public Function SomeFunction() As String
   #Else
   <WebMethod(CacheDuration:=86400)>
   Public Function SomeFunction() As String
   #End If
```

## <a name="example"></a>Exemple
 Cet exemple utilise le `#If...Then...#Else` construction pour déterminer s’il faut compiler certaines instructions.  
  
 [!code-vb[VbVbalrConditionalComp#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [#Const (directive)](../../../visual-basic/language-reference/directives/const-directive.md)
- [If...Then...Else (instruction)](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
- <xref:System.Diagnostics.ConditionalAttribute?displayProperty=nameWithType>
