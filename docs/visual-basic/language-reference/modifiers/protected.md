---
title: Protected (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Protected
helpviewer_keywords:
- Protected Friend keyword combination
- Protected keyword [Visual Basic], and Friend
- Protected keyword [Visual Basic], syntax
- Protected access modifier
- Protected keyword [Visual Basic]
ms.assetid: 74ad3d56-309f-49d2-b60c-1d0157d010e8
ms.openlocfilehash: 88e13fcd03c6a10cf1450cec90f9ca60aedc3eb1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778709"
---
# <a name="protected-visual-basic"></a><span data-ttu-id="43b44-102">Protected (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="43b44-102">Protected (Visual Basic)</span></span>
<span data-ttu-id="43b44-103">Un modificateur d’accès de membre qui spécifie qu’un ou plusieurs éléments de programmation déclarés sont accessibles uniquement à partir de leur propre classe ou d’une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="43b44-103">A member access modifier that specifies that one or more declared programming elements are accessible only from within their own class or from a derived class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="43b44-104">Notes</span><span class="sxs-lookup"><span data-stu-id="43b44-104">Remarks</span></span>  
 <span data-ttu-id="43b44-105">Parfois, un élément de programmation déclaré dans une classe contient des données sensibles ou du code restreint et vous souhaitez limiter l’accès à l’élément.</span><span class="sxs-lookup"><span data-stu-id="43b44-105">Sometimes a programming element declared in a class contains sensitive data or restricted code, and you want to limit access to the element.</span></span> <span data-ttu-id="43b44-106">Toutefois, si la classe peut être héritée et que vous prévoyez une hiérarchie de classes dérivées, il peut être nécessaire pour ces classes dérivées accéder aux données ou du code.</span><span class="sxs-lookup"><span data-stu-id="43b44-106">However, if the class is inheritable and you expect a hierarchy of derived classes, it might be necessary for these derived classes to access the data or code.</span></span> <span data-ttu-id="43b44-107">Dans ce cas, vous souhaitez l’élément accessible à la fois à partir de la classe de base et à partir de toutes les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="43b44-107">In such a case, you want the element to be accessible both from the base class and from all derived classes.</span></span> <span data-ttu-id="43b44-108">Pour limiter l’accès à un élément de cette manière, vous pouvez le déclarer avec `Protected`.</span><span class="sxs-lookup"><span data-stu-id="43b44-108">To limit access to an element in this manner, you can declare it with `Protected`.</span></span>  

> [!NOTE]
> <span data-ttu-id="43b44-109">Le `Protected` modificateur d’accès peut être combiné avec deux autres modificateurs :</span><span class="sxs-lookup"><span data-stu-id="43b44-109">The `Protected` access modifier can be combined with two other modifiers:</span></span>
> - <span data-ttu-id="43b44-110">Le [Protected Friend](protected-friend.md) modificateur rend un membre de classe accessible à partir de cette classe, à partir de classes dérivées et à partir de l’assembly dans lequel la classe est définie.</span><span class="sxs-lookup"><span data-stu-id="43b44-110">The [Protected Friend](protected-friend.md) modifier makes a class member accessible from within that class, from derived classes, and from the same assembly in which the class is defined.</span></span> 
> - <span data-ttu-id="43b44-111">Le [Private Protected](private-protected.md) modificateur rend un membre de classe accessible par les types dérivés, mais uniquement au sein de son assembly conteneur.</span><span class="sxs-lookup"><span data-stu-id="43b44-111">The [Private Protected](private-protected.md) modifier makes a class member accessible by derived types, but only within its containing assembly.</span></span>
  
## <a name="rules"></a><span data-ttu-id="43b44-112">Règles</span><span class="sxs-lookup"><span data-stu-id="43b44-112">Rules</span></span>  
  
- <span data-ttu-id="43b44-113">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="43b44-113">**Declaration Context.**</span></span> <span data-ttu-id="43b44-114">Vous pouvez utiliser `Protected` uniquement au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="43b44-114">You can use `Protected` only at the class level.</span></span> <span data-ttu-id="43b44-115">Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être une fichier source, un espace de noms, un module, une structure ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="43b44-115">This means the declaration context for a `Protected` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.</span></span>  

## <a name="behavior"></a><span data-ttu-id="43b44-116">Comportement</span><span class="sxs-lookup"><span data-stu-id="43b44-116">Behavior</span></span>  
  
- <span data-ttu-id="43b44-117">**Niveau d’accès.**</span><span class="sxs-lookup"><span data-stu-id="43b44-117">**Access Level.**</span></span> <span data-ttu-id="43b44-118">Tout le code dans une classe peut accéder à ses éléments.</span><span class="sxs-lookup"><span data-stu-id="43b44-118">All code in a class can access its elements.</span></span> <span data-ttu-id="43b44-119">Code dans n’importe quelle classe qui dérive d’une classe de base peut accéder à tous les `Protected` éléments de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="43b44-119">Code in any class that derives from a base class can access all the `Protected` elements of the base class.</span></span> <span data-ttu-id="43b44-120">Cela est vrai pour toutes les générations de dérivation.</span><span class="sxs-lookup"><span data-stu-id="43b44-120">This is true for all generations of derivation.</span></span> <span data-ttu-id="43b44-121">Cela signifie qu’une classe peut accéder à `Protected` éléments de la classe de base de la classe de base et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="43b44-121">This means that a class can access `Protected` elements of the base class of the base class, and so on.</span></span>  
  
     <span data-ttu-id="43b44-122">Accès protégé n’est pas un sur-ensemble ou un sous-ensemble de l’accès ami.</span><span class="sxs-lookup"><span data-stu-id="43b44-122">Protected access is not a superset or subset of friend access.</span></span>  
  
- <span data-ttu-id="43b44-123">**Modificateurs d’accès.**</span><span class="sxs-lookup"><span data-stu-id="43b44-123">**Access Modifiers.**</span></span> <span data-ttu-id="43b44-124">Les mots clés qui spécifient le niveau d’accès sont appelés *modificateurs d’accès*.</span><span class="sxs-lookup"><span data-stu-id="43b44-124">The keywords that specify access level are called *access modifiers*.</span></span> <span data-ttu-id="43b44-125">Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="43b44-125">For a comparison of the access modifiers, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
 <span data-ttu-id="43b44-126">Le modificateur `Protected` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="43b44-126">The `Protected` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="43b44-127">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-127">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [<span data-ttu-id="43b44-128">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-128">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [<span data-ttu-id="43b44-129">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-129">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="43b44-130">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-130">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [<span data-ttu-id="43b44-131">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-131">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="43b44-132">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-132">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [<span data-ttu-id="43b44-133">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-133">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="43b44-134">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-134">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="43b44-135">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-135">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [<span data-ttu-id="43b44-136">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-136">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="43b44-137">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-137">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [<span data-ttu-id="43b44-138">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="43b44-138">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="43b44-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b44-139">See also</span></span>

- [<span data-ttu-id="43b44-140">Public</span><span class="sxs-lookup"><span data-stu-id="43b44-140">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="43b44-141">Friend</span><span class="sxs-lookup"><span data-stu-id="43b44-141">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)
- [<span data-ttu-id="43b44-142">Private</span><span class="sxs-lookup"><span data-stu-id="43b44-142">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)
- [<span data-ttu-id="43b44-143">Private Protected</span><span class="sxs-lookup"><span data-stu-id="43b44-143">Private Protected</span></span>](private-protected.md)
- [<span data-ttu-id="43b44-144">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="43b44-144">Protected Friend</span></span>](protected-friend.md)
- [<span data-ttu-id="43b44-145">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="43b44-145">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="43b44-146">Procédures</span><span class="sxs-lookup"><span data-stu-id="43b44-146">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="43b44-147">Structures</span><span class="sxs-lookup"><span data-stu-id="43b44-147">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="43b44-148">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="43b44-148">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
