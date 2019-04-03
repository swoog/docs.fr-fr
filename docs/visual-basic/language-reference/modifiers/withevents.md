---
title: WithEvents (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.WithEvents
- WithEvents
helpviewer_keywords:
- WithEvents keyword [Visual Basic]
ms.assetid: 19d461f5-d72f-4de9-8c1d-0a6650316990
ms.openlocfilehash: 75d118ee2bd4918c3a936cb341864ddc5315726b
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58826611"
---
# <a name="withevents-visual-basic"></a><span data-ttu-id="52e91-102">WithEvents (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="52e91-102">WithEvents (Visual Basic)</span></span>
<span data-ttu-id="52e91-103">Spécifie qu’une ou plusieurs variables membres déclarées font référence à une instance d’une classe qui peut déclencher des événements.</span><span class="sxs-lookup"><span data-stu-id="52e91-103">Specifies that one or more declared member variables refer to an instance of a class that can raise events.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="52e91-104">Notes</span><span class="sxs-lookup"><span data-stu-id="52e91-104">Remarks</span></span>  
 <span data-ttu-id="52e91-105">Lorsqu’une variable est définie à l’aide de `WithEvents`, vous pouvez spécifier de manière déclarative qu’une méthode gère les événements de la variable à l’aide de la `Handles` mot clé.</span><span class="sxs-lookup"><span data-stu-id="52e91-105">When a variable is defined using `WithEvents`, you can declaratively specify that a method handles the variable's events using the `Handles` keyword.</span></span>  
  
 <span data-ttu-id="52e91-106">Vous pouvez utiliser `WithEvents` uniquement au niveau de la classe ou le module.</span><span class="sxs-lookup"><span data-stu-id="52e91-106">You can use `WithEvents` only at class or module level.</span></span> <span data-ttu-id="52e91-107">Cela signifie que le contexte de déclaration pour un `WithEvents` variable doit être une classe ou un module et ne peut pas être un fichier source, un espace de noms, une structure ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="52e91-107">This means the declaration context for a `WithEvents` variable must be a class or module and cannot be a source file, namespace, structure, or procedure.</span></span>  
  
 <span data-ttu-id="52e91-108">Vous ne pouvez pas utiliser `WithEvents` sur un membre de structure.</span><span class="sxs-lookup"><span data-stu-id="52e91-108">You cannot use `WithEvents` on a structure member.</span></span>  
  
 <span data-ttu-id="52e91-109">Vous pouvez déclarer des variables individuelles, pas les tableaux — avec `WithEvents`.</span><span class="sxs-lookup"><span data-stu-id="52e91-109">You can declare only individual variables—not arrays—with `WithEvents`.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="52e91-110">Règles</span><span class="sxs-lookup"><span data-stu-id="52e91-110">Rules</span></span>  
  
-   <span data-ttu-id="52e91-111">**Types d’éléments.**</span><span class="sxs-lookup"><span data-stu-id="52e91-111">**Element Types.**</span></span> <span data-ttu-id="52e91-112">Vous devez déclarer `WithEvents` variables comme des variables d’objet afin qu’ils acceptent les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="52e91-112">You must declare `WithEvents` variables to be object variables so that they can accept class instances.</span></span> <span data-ttu-id="52e91-113">Toutefois, vous ne pouvez pas déclarer en tant que `Object`.</span><span class="sxs-lookup"><span data-stu-id="52e91-113">However, you cannot declare them as `Object`.</span></span> <span data-ttu-id="52e91-114">Vous devez les déclarer en tant que la classe spécifique capable de déclencher les événements.</span><span class="sxs-lookup"><span data-stu-id="52e91-114">You must declare them as the specific class that can raise the events.</span></span>  
  
 <span data-ttu-id="52e91-115">Le `WithEvents` modificateur peut être utilisé dans ce contexte : [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)</span><span class="sxs-lookup"><span data-stu-id="52e91-115">The `WithEvents` modifier can be used in this context: [Dim Statement](../../../visual-basic/language-reference/statements/dim-statement.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52e91-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52e91-116">See also</span></span>

- [<span data-ttu-id="52e91-117">Handles</span><span class="sxs-lookup"><span data-stu-id="52e91-117">Handles</span></span>](../../../visual-basic/language-reference/statements/handles-clause.md)
- [<span data-ttu-id="52e91-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="52e91-118">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="52e91-119">Événements</span><span class="sxs-lookup"><span data-stu-id="52e91-119">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
