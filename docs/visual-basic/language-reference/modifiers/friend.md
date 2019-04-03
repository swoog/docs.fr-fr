---
title: Friend (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Friend
helpviewer_keywords:
- Friend keyword [Visual Basic]
- Friend access modifier
- Friend keyword [Visual Basic], syntax
- Protected Friend keyword combination
- Friend keyword [Visual Basic], and Protected
ms.assetid: b664605e-1c79-4728-b996-aa59c50846bc
ms.openlocfilehash: 18681935d0380f9be3970fdb5d17ffb089152f59
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819149"
---
# <a name="friend-visual-basic"></a><span data-ttu-id="7e19f-102">Friend (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7e19f-102">Friend (Visual Basic)</span></span>
<span data-ttu-id="7e19f-103">Spécifie qu’un ou plusieurs éléments de programmation déclarés sont accessibles uniquement à partir de l’assembly qui contient leur déclaration.</span><span class="sxs-lookup"><span data-stu-id="7e19f-103">Specifies that one or more declared programming elements are accessible only from within the assembly that contains their declaration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7e19f-104">Notes</span><span class="sxs-lookup"><span data-stu-id="7e19f-104">Remarks</span></span>  
 <span data-ttu-id="7e19f-105">Dans de nombreux cas, vous souhaitez la programmation des éléments tels que des classes et des structures à utiliser par l’assembly entier, non seulement par le composant qui les déclare.</span><span class="sxs-lookup"><span data-stu-id="7e19f-105">In many cases, you want programming elements such as classes and structures to be used by the entire assembly, not only by the component that declares them.</span></span> <span data-ttu-id="7e19f-106">Toutefois, vous souhaitiez les accessibles par le code en dehors de l’assembly (par exemple, si l’application est propriétaire).</span><span class="sxs-lookup"><span data-stu-id="7e19f-106">However, you might not want them to be accessible by code outside the assembly (for example, if the application is proprietary).</span></span> <span data-ttu-id="7e19f-107">Si vous souhaitez limiter l’accès à un élément de cette façon, vous pouvez la déclarer à l’aide de la `Friend` modificateur.</span><span class="sxs-lookup"><span data-stu-id="7e19f-107">If you want to limit access to an element in this way, you can declare it by using the `Friend` modifier.</span></span>  
  
 <span data-ttu-id="7e19f-108">Le code dans d’autres classes, structures et les modules qui sont compilés dans le même assembly peut accéder à tous les `Friend` éléments dans cet assembly.</span><span class="sxs-lookup"><span data-stu-id="7e19f-108">Code in other classes, structures, and modules that are compiled to the same assembly can access all the `Friend` elements in that assembly.</span></span>  
  
 <span data-ttu-id="7e19f-109">`Friend` l’accès est souvent le niveau par défaut pour les éléments de programmation d’une application, et `Friend` est l’accès par défaut au niveau d’une interface, un module, une classe ou une structure.</span><span class="sxs-lookup"><span data-stu-id="7e19f-109">`Friend` access is often the preferred level for an application's programming elements, and `Friend` is the default access level of an interface, a module, a class, or a structure.</span></span>  
  
 <span data-ttu-id="7e19f-110">Vous pouvez utiliser `Friend` uniquement au niveau du module, interface ou espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7e19f-110">You can use `Friend` only at the module, interface, or namespace level.</span></span> <span data-ttu-id="7e19f-111">Par conséquent, le contexte de déclaration pour un `Friend` élément doit être un fichier source, un espace de noms, une interface, un module, une classe ou une structure ; il ne peut pas être une procédure.</span><span class="sxs-lookup"><span data-stu-id="7e19f-111">Therefore, the declaration context for a `Friend` element must be a source file, a namespace, an interface, a module, a class, or a structure; it can't be a procedure.</span></span>  

> [!NOTE]
> <span data-ttu-id="7e19f-112">Vous pouvez également utiliser le [Protected Friend](protected-friend.md) modificateur d’accès, ce qui rend un membre de classe accessible à partir de cette classe, à partir de classes dérivées et à partir de l’assembly dans lequel la classe est définie.</span><span class="sxs-lookup"><span data-stu-id="7e19f-112">You can also use the [Protected Friend](protected-friend.md) access modifier, which makes a class member accessible from within that class, from derived classes, and from the same assembly in which the class is defined.</span></span> <span data-ttu-id="7e19f-113">Pour restreindre l’accès à un membre à partir de sa classe et à partir de classes dérivées dans le même assembly, vous utilisez le [Private Protected](private-protected.md) modificateur d’accès.</span><span class="sxs-lookup"><span data-stu-id="7e19f-113">To restrict access to a member from within its class and from derived classes in the same assembly, you use the [Private Protected](private-protected.md) access modifier.</span></span>

 <span data-ttu-id="7e19f-114">Pour obtenir une comparaison de `Friend` et d’autres modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7e19f-114">For a comparison of `Friend` and the other access modifiers, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7e19f-115">Vous pouvez spécifier qu’un autre assembly est un assembly friend, ce qui permet d’accéder à tous les types et membres qui sont marqués comme `Friend`.</span><span class="sxs-lookup"><span data-stu-id="7e19f-115">You can specify that another assembly is a friend assembly, which allows it to access all types and members that are marked as `Friend`.</span></span> <span data-ttu-id="7e19f-116">Pour plus d’informations, consultez [Assemblys friend](../../../standard/assembly/friend-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="7e19f-116">For more information, see [Friend Assemblies](../../../standard/assembly/friend-assemblies.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e19f-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="7e19f-117">Example</span></span>  
 <span data-ttu-id="7e19f-118">La classe suivante utilise le `Friend` modificateur pour autoriser d’autres éléments de programmation dans le même assembly pour accéder à certains membres.</span><span class="sxs-lookup"><span data-stu-id="7e19f-118">The following class uses the `Friend` modifier to allow other programming elements within the same assembly to access certain members.</span></span>  
  
 [!code-vb[VbVbalrAccessModifiers#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalraccessmodifiers/vb/class1.vb#1)]  
  
## <a name="usage"></a><span data-ttu-id="7e19f-119">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7e19f-119">Usage</span></span>  
 <span data-ttu-id="7e19f-120">Vous pouvez utiliser le `Friend` modificateur dans ces contextes :</span><span class="sxs-lookup"><span data-stu-id="7e19f-120">You can use the `Friend` modifier in these contexts:</span></span>  
  
 [<span data-ttu-id="7e19f-121">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-121">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [<span data-ttu-id="7e19f-122">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-122">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [<span data-ttu-id="7e19f-123">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-123">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="7e19f-124">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-124">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [<span data-ttu-id="7e19f-125">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-125">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="7e19f-126">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-126">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [<span data-ttu-id="7e19f-127">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-127">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="7e19f-128">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-128">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="7e19f-129">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-129">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [<span data-ttu-id="7e19f-130">Module (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-130">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)  
  
 [<span data-ttu-id="7e19f-131">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-131">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="7e19f-132">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-132">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [<span data-ttu-id="7e19f-133">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="7e19f-133">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="7e19f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e19f-134">See also</span></span>

- <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>
- [<span data-ttu-id="7e19f-135">Public</span><span class="sxs-lookup"><span data-stu-id="7e19f-135">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="7e19f-136">Protected</span><span class="sxs-lookup"><span data-stu-id="7e19f-136">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)
- [<span data-ttu-id="7e19f-137">Private</span><span class="sxs-lookup"><span data-stu-id="7e19f-137">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)
- [<span data-ttu-id="7e19f-138">Private Protected</span><span class="sxs-lookup"><span data-stu-id="7e19f-138">Private Protected</span></span>](./private-protected.md)
- [<span data-ttu-id="7e19f-139">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="7e19f-139">Protected Friend</span></span>](./protected-friend.md)
- [<span data-ttu-id="7e19f-140">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7e19f-140">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="7e19f-141">Procédures</span><span class="sxs-lookup"><span data-stu-id="7e19f-141">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="7e19f-142">Structures</span><span class="sxs-lookup"><span data-stu-id="7e19f-142">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="7e19f-143">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="7e19f-143">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
