---
title: Protected Friend (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Protected Friend keyword [Visual Basic]
- Protected Friend keyword [Visual Basic], syntax
ms.openlocfilehash: 331c63dc290d4096e8158f265ee869b47743a273
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59151773"
---
# <a name="protected-friend-visual-basic"></a><span data-ttu-id="8f0c6-102">Protected Friend (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8f0c6-102">Protected Friend (Visual Basic)</span></span>

<span data-ttu-id="8f0c6-103">La combinaison de mots clés `Protected Friend` est un modificateur d’accès de membre.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-103">The `Protected Friend` keyword combination is a member access modifier.</span></span> <span data-ttu-id="8f0c6-104">Elle confère à la fois [Friend](friend.md) accès et [protégé](protected.md) accès sur les éléments déclarés, afin qu’ils soient accessibles à partir de n’importe où dans le même assembly, de leur propre classe et de classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-104">It confers both [Friend](friend.md) access and [Protected](protected.md) access on the declared elements, so they are accessible from anywhere in the same assembly, from their own class, and from derived classes.</span></span> <span data-ttu-id="8f0c6-105">Vous pouvez spécifier `Protected Friend` uniquement sur les membres de classes ; vous ne pouvez pas appliquer `Protected Friend` aux membres d’une structure, car les structures ne peuvent pas être héritées.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-105">You can specify `Protected Friend` only on members of classes; you cannot apply `Protected Friend` to members of a structure because structures cannot be inherited.</span></span>

> [!NOTE]
> <span data-ttu-id="8f0c6-106">Dans Visual Studio, en sélectionnant la touche F1 sur `protected friend` fournit une aide pour soit [protégé](protected.md) ou [friend](friend.md).</span><span class="sxs-lookup"><span data-stu-id="8f0c6-106">In Visual Studio, selecting F1 help on `protected friend` provides help for either [protected](protected.md) or [friend](friend.md).</span></span> <span data-ttu-id="8f0c6-107">L’IDE choisit le jeton unique sous le curseur plutôt que le mot composé.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-107">The IDE picks the single token under the cursor rather than the compound word.</span></span>

## <a name="rules"></a><span data-ttu-id="8f0c6-108">Règles</span><span class="sxs-lookup"><span data-stu-id="8f0c6-108">Rules</span></span>

- <span data-ttu-id="8f0c6-109">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="8f0c6-109">**Declaration Context.**</span></span> <span data-ttu-id="8f0c6-110">Vous pouvez utiliser `Protected Friend` uniquement au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-110">You can use `Protected Friend` only at the class level.</span></span> <span data-ttu-id="8f0c6-111">Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être une fichier source, un espace de noms, un module, une structure ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-111">This means the declaration context for a `Protected` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.</span></span> 

## <a name="see-also"></a><span data-ttu-id="8f0c6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f0c6-112">See also</span></span>

- [<span data-ttu-id="8f0c6-113">Public</span><span class="sxs-lookup"><span data-stu-id="8f0c6-113">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="8f0c6-114">Protected</span><span class="sxs-lookup"><span data-stu-id="8f0c6-114">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)
- [<span data-ttu-id="8f0c6-115">Friend</span><span class="sxs-lookup"><span data-stu-id="8f0c6-115">Friend</span></span>](friend.md)
- [<span data-ttu-id="8f0c6-116">Private</span><span class="sxs-lookup"><span data-stu-id="8f0c6-116">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)
- [<span data-ttu-id="8f0c6-117">Private Protected</span><span class="sxs-lookup"><span data-stu-id="8f0c6-117">Private Protected</span></span>](./private-protected.md)
- [<span data-ttu-id="8f0c6-118">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8f0c6-118">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="8f0c6-119">Procédures</span><span class="sxs-lookup"><span data-stu-id="8f0c6-119">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="8f0c6-120">Structures</span><span class="sxs-lookup"><span data-stu-id="8f0c6-120">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="8f0c6-121">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="8f0c6-121">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
