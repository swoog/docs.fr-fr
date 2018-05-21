---
title: Protected Friend (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Protected Friend keyword [Visual Basic]
- Protected Friend keyword [Visual Basic], syntax
ms.openlocfilehash: b72cbee0394043620e792d1c014bfe55121e175e
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/18/2018
---
# <a name="protected-friend-visual-basic"></a><span data-ttu-id="aa7e1-102">Protected Friend (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="aa7e1-102">Protected Friend (Visual Basic)</span></span>

<span data-ttu-id="aa7e1-103">La combinaison de mots clés `Protected Friend` est un modificateur d’accès de membre.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-103">The `Protected Friend` keyword combination is a member access modifier.</span></span> <span data-ttu-id="aa7e1-104">Il confère à la fois [Friend](friend.md) accès et [protégé](protected.md) accès aux éléments déclarés, afin qu’ils soient accessibles à partir de n’importe où dans le même assembly, de leur propre classe et de classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-104">It confers both [Friend](friend.md) access and [Protected](protected.md) access on the declared elements, so they are accessible from anywhere in the same assembly, from their own class, and from derived classes.</span></span> <span data-ttu-id="aa7e1-105">Vous pouvez spécifier `Protected Friend` uniquement sur les membres de classes ; vous ne pouvez pas appliquer `Protected Friend` aux membres d’une structure, car les structures ne peuvent pas être héritées.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-105">You can specify `Protected Friend` only on members of classes; you cannot apply `Protected Friend` to members of a structure because structures cannot be inherited.</span></span>

> [!NOTE]
> <span data-ttu-id="aa7e1-106">Dans Visual Studio, en sélectionnant la touche F1 sur `protected friend` fournit une aide pour soit [protégé](protected.md) ou [friend](friend.md).</span><span class="sxs-lookup"><span data-stu-id="aa7e1-106">In Visual Studio, selecting F1 help on `protected friend` provides help for either [protected](protected.md) or [friend](friend.md).</span></span> <span data-ttu-id="aa7e1-107">L’IDE choisit le jeton unique sous le curseur plutôt que le mot composé.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-107">The IDE picks the single token under the cursor rather than the compound word.</span></span>

## <a name="rules"></a><span data-ttu-id="aa7e1-108">Règles</span><span class="sxs-lookup"><span data-stu-id="aa7e1-108">Rules</span></span>

- <span data-ttu-id="aa7e1-109">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="aa7e1-109">**Declaration Context.**</span></span> <span data-ttu-id="aa7e1-110">Vous pouvez utiliser `Protected Friend` uniquement au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-110">You can use `Protected Friend` only at the class level.</span></span> <span data-ttu-id="aa7e1-111">Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être un fichier source, espace de noms, interface, un module, structure ou procédure.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-111">This means the declaration context for a `Protected` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.</span></span> 


## <a name="see-also"></a><span data-ttu-id="aa7e1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa7e1-112">See Also</span></span>

[<span data-ttu-id="aa7e1-113">Public</span><span class="sxs-lookup"><span data-stu-id="aa7e1-113">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)  
[<span data-ttu-id="aa7e1-114">Protected</span><span class="sxs-lookup"><span data-stu-id="aa7e1-114">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)  
<span data-ttu-id="aa7e1-115">[Friend](friend.md) </span><span class="sxs-lookup"><span data-stu-id="aa7e1-115">[Friend](friend.md) </span></span>  
[<span data-ttu-id="aa7e1-116">Private</span><span class="sxs-lookup"><span data-stu-id="aa7e1-116">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)  
<span data-ttu-id="aa7e1-117">[Protégé privé](./private-protected.md) </span><span class="sxs-lookup"><span data-stu-id="aa7e1-117">[Private Protected](./private-protected.md) </span></span>  
[<span data-ttu-id="aa7e1-118">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aa7e1-118">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)  
[<span data-ttu-id="aa7e1-119">Procédures</span><span class="sxs-lookup"><span data-stu-id="aa7e1-119">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
[<span data-ttu-id="aa7e1-120">Structures</span><span class="sxs-lookup"><span data-stu-id="aa7e1-120">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
[<span data-ttu-id="aa7e1-121">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="aa7e1-121">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
