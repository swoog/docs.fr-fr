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
# <a name="ifthenelse-directives"></a><span data-ttu-id="f8bb4-102">#If...Then...#Else, directives</span><span class="sxs-lookup"><span data-stu-id="f8bb4-102">#If...Then...#Else Directives</span></span>
<span data-ttu-id="f8bb4-103">Compilation conditionnelle des blocs de code Visual Basic sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-103">Conditionally compiles selected blocks of Visual Basic code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8bb4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8bb4-104">Syntax</span></span>  
  
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
  
## <a name="parts"></a><span data-ttu-id="f8bb4-105">Composants</span><span class="sxs-lookup"><span data-stu-id="f8bb4-105">Parts</span></span>  
 `expression`  
 <span data-ttu-id="f8bb4-106">Requis pour `#If` et `#ElseIf` instructions, facultatives ailleurs.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-106">Required for `#If` and `#ElseIf` statements, optional elsewhere.</span></span> <span data-ttu-id="f8bb4-107">Toute expression, exclusivement consistant en une ou plusieurs constantes de compilation conditionnelle, les littéraux et les opérateurs, qui prend la valeur `True` ou `False`.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-107">Any expression, consisting exclusively of one or more conditional compiler constants, literals, and operators, that evaluates to `True` or `False`.</span></span>  
  
 `statements`  
 <span data-ttu-id="f8bb4-108">Requis pour `#If` instruction bloc, facultatif ailleurs.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-108">Required for `#If` statement block, optional elsewhere.</span></span> <span data-ttu-id="f8bb4-109">Lignes de programme Visual Basic ou des directives de compilateur qui sont compilés si l’expression associée prend la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-109">Visual Basic program lines or compiler directives that are compiled if the associated expression evaluates to `True`.</span></span>  
  
 `#End If`  
 <span data-ttu-id="f8bb4-110">Met fin à la `#If` bloc d’instructions.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-110">Terminates the `#If` statement block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f8bb4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f8bb4-111">Remarks</span></span>  
 <span data-ttu-id="f8bb4-112">Sur la surface, le comportement de la `#If...Then...#Else` directives semble être le même que celui de la `If...Then...Else` instructions.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-112">On the surface, the behavior of the `#If...Then...#Else` directives appears the same as that of the `If...Then...Else` statements.</span></span> <span data-ttu-id="f8bb4-113">Toutefois, le `#If...Then...#Else` directives évaluent ce qui est compilé par le compilateur, alors que le `If...Then...Else` instructions évaluent les conditions au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-113">However, the `#If...Then...#Else` directives evaluate what is compiled by the compiler, whereas the `If...Then...Else` statements evaluate conditions at run time.</span></span>  
  
 <span data-ttu-id="f8bb4-114">Compilation conditionnelle est généralement utilisée pour compiler le même programme sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-114">Conditional compilation is typically used to compile the same program for different platforms.</span></span> <span data-ttu-id="f8bb4-115">Il est également utilisé pour empêcher le débogage de code d’apparaître dans un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-115">It is also used to prevent debugging code from appearing in an executable file.</span></span> <span data-ttu-id="f8bb4-116">Code exclu durant la compilation conditionnelle est totalement absent du fichier exécutable final, afin qu’il n’a aucun effet sur la taille ou de performances.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-116">Code excluded during conditional compilation is completely omitted from the final executable file, so it has no effect on size or performance.</span></span>  
  
 <span data-ttu-id="f8bb4-117">Quel que soit le résultat des évaluations, toutes les expressions sont évaluées à l’aide de `Option Compare Binary`.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-117">Regardless of the outcome of any evaluation, all expressions are evaluated using `Option Compare Binary`.</span></span> <span data-ttu-id="f8bb4-118">Le `Option Compare` instruction n’affecte pas les expressions dans `#If` et `#ElseIf` instructions.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-118">The `Option Compare` statement does not affect expressions in `#If` and `#ElseIf` statements.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f8bb4-119">Aucune forme d’une ligne de la `#If`, `#Else`, `#ElseIf`, et `#End If` directives existe.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-119">No single-line form of the `#If`, `#Else`, `#ElseIf`, and `#End If` directives exists.</span></span> <span data-ttu-id="f8bb4-120">Aucun autre code ne peut apparaître sur la même ligne qu’une des directives.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-120">No other code can appear on the same line as any of the directives.</span></span> 

<span data-ttu-id="f8bb4-121">Les instructions dans un bloc de compilation conditionnelle doivent être complète logique.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-121">The statements within a conditional compilation block must be complete logical statements.</span></span> <span data-ttu-id="f8bb4-122">Par exemple, vous ne pouvez pas effectuer une compilation conditionnelle uniquement les attributs d’une fonction, mais vous pouvez déclarer conditionnelle de la fonction, ainsi que ses attributs :</span><span class="sxs-lookup"><span data-stu-id="f8bb4-122">For example, you cannot conditionally compile only the attributes of a function, but you can conditionally declare the function along with its attributes:</span></span>

```vb
   #If DEBUG Then
   <WebMethod()>
   Public Function SomeFunction() As String
   #Else
   <WebMethod(CacheDuration:=86400)>
   Public Function SomeFunction() As String
   #End If
```

## <a name="example"></a><span data-ttu-id="f8bb4-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="f8bb4-123">Example</span></span>
 <span data-ttu-id="f8bb4-124">Cet exemple utilise le `#If...Then...#Else` construction pour déterminer s’il faut compiler certaines instructions.</span><span class="sxs-lookup"><span data-stu-id="f8bb4-124">This example uses the `#If...Then...#Else` construct to determine whether to compile certain statements.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="f8bb4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8bb4-125">See also</span></span>

- [<span data-ttu-id="f8bb4-126">#Const (directive)</span><span class="sxs-lookup"><span data-stu-id="f8bb4-126">#Const Directive</span></span>](../../../visual-basic/language-reference/directives/const-directive.md)
- [<span data-ttu-id="f8bb4-127">If...Then...Else (instruction)</span><span class="sxs-lookup"><span data-stu-id="f8bb4-127">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [<span data-ttu-id="f8bb4-128">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="f8bb4-128">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
- <xref:System.Diagnostics.ConditionalAttribute?displayProperty=nameWithType>
