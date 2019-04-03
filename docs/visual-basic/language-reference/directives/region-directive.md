---
title: '#Directive de région (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.Region
- vb.#Region
helpviewer_keywords:
- Visual Basic compiler, compiler directives
- '#region directive'
- region directive (#region)
- '#Region keyword [Visual Basic]'
ms.assetid: 90a6a104-3cbf-47d0-bdc4-b585d0921b87
ms.openlocfilehash: eaaf0f8279ec905767be3f364a88357f0d393bba
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58818868"
---
# <a name="region-directive"></a><span data-ttu-id="fafc3-102">#Region, directive</span><span class="sxs-lookup"><span data-stu-id="fafc3-102">#Region Directive</span></span>
<span data-ttu-id="fafc3-103">Réduit et masque des sections de code dans des fichiers Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fafc3-103">Collapses and hides sections of code in Visual Basic files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fafc3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fafc3-104">Syntax</span></span>  

```vb
#Region "identifier_string"  
#End Region  
```  
  
## <a name="parts"></a><span data-ttu-id="fafc3-105">Composants</span><span class="sxs-lookup"><span data-stu-id="fafc3-105">Parts</span></span>  
  
|<span data-ttu-id="fafc3-106">Terme</span><span class="sxs-lookup"><span data-stu-id="fafc3-106">Term</span></span>|<span data-ttu-id="fafc3-107">Définition</span><span class="sxs-lookup"><span data-stu-id="fafc3-107">Definition</span></span>|  
|---|---|  
|`identifier_string`|<span data-ttu-id="fafc3-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fafc3-108">Required.</span></span> <span data-ttu-id="fafc3-109">Chaîne qui joue le rôle du titre d'une région quand elle est réduite.</span><span class="sxs-lookup"><span data-stu-id="fafc3-109">String that acts as the title of a region when it is collapsed.</span></span> <span data-ttu-id="fafc3-110">Les régions sont réduites par défaut.</span><span class="sxs-lookup"><span data-stu-id="fafc3-110">Regions are collapsed by default.</span></span>|  
|`#End Region`|<span data-ttu-id="fafc3-111">Met fin au bloc `#Region`.</span><span class="sxs-lookup"><span data-stu-id="fafc3-111">Terminates the `#Region` block.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fafc3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fafc3-112">Remarks</span></span>  
 <span data-ttu-id="fafc3-113">Utilisez la directive `#Region` pour spécifier un bloc de code que vous pouvez développer ou réduire dans le mode Plan de l'éditeur de code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fafc3-113">Use the `#Region` directive to specify a block of code to expand or collapse when using the outlining feature of the Visual Studio Code Editor.</span></span> <span data-ttu-id="fafc3-114">Vous pouvez placer, ou *imbriquer*, régions dans d’autres régions pour grouper des régions semblables ensemble.</span><span class="sxs-lookup"><span data-stu-id="fafc3-114">You can place, or *nest*, regions within other regions to group similar regions together.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fafc3-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="fafc3-115">Example</span></span>  
 <span data-ttu-id="fafc3-116">Cet exemple utilise la directive `#Region`.</span><span class="sxs-lookup"><span data-stu-id="fafc3-116">This example uses the `#Region` directive.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="fafc3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fafc3-117">See also</span></span>

- [<span data-ttu-id="fafc3-118">#If...Then...#Else, directives</span><span class="sxs-lookup"><span data-stu-id="fafc3-118">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
- [<span data-ttu-id="fafc3-119">Mode Plan</span><span class="sxs-lookup"><span data-stu-id="fafc3-119">Outlining</span></span>](/visualstudio/ide/outlining)
- [<span data-ttu-id="fafc3-120">Guide pratique pour réduire et masquer des sections de code</span><span class="sxs-lookup"><span data-stu-id="fafc3-120">How to: Collapse and Hide Sections of Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-collapse-and-hide-sections-of-code.md)
