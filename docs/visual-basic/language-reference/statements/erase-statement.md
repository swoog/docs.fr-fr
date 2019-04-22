---
title: Erase, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Erase
helpviewer_keywords:
- Erase keyword [Visual Basic]
- Erase statement [Visual Basic]
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
ms.openlocfilehash: bf3eb6476dc1485faeddab475f29e508175d3378
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58840404"
---
# <a name="erase-statement-visual-basic"></a><span data-ttu-id="e4b76-102">Erase, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e4b76-102">Erase Statement (Visual Basic)</span></span>
<span data-ttu-id="e4b76-103">Permet de libérer des variables tableau ainsi que la mémoire utilisée pour leurs éléments.</span><span class="sxs-lookup"><span data-stu-id="e4b76-103">Used to release array variables and deallocate the memory used for their elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4b76-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4b76-104">Syntax</span></span>  
  
```  
Erase arraylist  
```  
  
## <a name="parts"></a><span data-ttu-id="e4b76-105">Composants</span><span class="sxs-lookup"><span data-stu-id="e4b76-105">Parts</span></span>  
 `arraylist`  
 <span data-ttu-id="e4b76-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e4b76-106">Required.</span></span> <span data-ttu-id="e4b76-107">Liste des variables tableau à effacer.</span><span class="sxs-lookup"><span data-stu-id="e4b76-107">List of array variables to be erased.</span></span> <span data-ttu-id="e4b76-108">Les variables multiples sont séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e4b76-108">Multiple variables are separated by commas.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e4b76-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e4b76-109">Remarks</span></span>  
 <span data-ttu-id="e4b76-110">La `Erase` instruction peut apparaître seulement au niveau de la procédure.</span><span class="sxs-lookup"><span data-stu-id="e4b76-110">The `Erase` statement can appear only at procedure level.</span></span> <span data-ttu-id="e4b76-111">Cela signifie que vous pouvez libérer des tableaux à l’intérieur d’une procédure mais pas au niveau de classe ou le module.</span><span class="sxs-lookup"><span data-stu-id="e4b76-111">This means you can release arrays inside a procedure but not at class or module level.</span></span>  
  
 <span data-ttu-id="e4b76-112">Le `Erase` instruction est équivalente à l’attribution `Nothing` à chaque variable de tableau.</span><span class="sxs-lookup"><span data-stu-id="e4b76-112">The `Erase` statement is equivalent to assigning `Nothing` to each array variable.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e4b76-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4b76-113">Example</span></span>  
 <span data-ttu-id="e4b76-114">L’exemple suivant utilise la `Erase` instruction pour effacer les deux tableaux et libérer leur mémoire (1 000 et 100 éléments de stockage, respectivement).</span><span class="sxs-lookup"><span data-stu-id="e4b76-114">The following example uses the `Erase` statement to clear two arrays and free their memory (1000 and 100 storage elements, respectively).</span></span> <span data-ttu-id="e4b76-115">La `ReDim` instruction assigne ensuite une nouvelle instance de tableau au tableau tridimensionnel.</span><span class="sxs-lookup"><span data-stu-id="e4b76-115">The `ReDim` statement then assigns a new array instance to the three-dimensional array.</span></span>  
  
 [!code-vb[VbVbalrStatements#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#19)]  
  
## <a name="see-also"></a><span data-ttu-id="e4b76-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b76-116">See also</span></span>

- [<span data-ttu-id="e4b76-117">Nothing</span><span class="sxs-lookup"><span data-stu-id="e4b76-117">Nothing</span></span>](../../../visual-basic/language-reference/nothing.md)
- [<span data-ttu-id="e4b76-118">ReDim (instruction)</span><span class="sxs-lookup"><span data-stu-id="e4b76-118">ReDim Statement</span></span>](../../../visual-basic/language-reference/statements/redim-statement.md)
