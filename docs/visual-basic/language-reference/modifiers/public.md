---
title: Public (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Public
helpviewer_keywords:
- Public keyword [Visual Basic]
- Public keyword [Visual Basic], syntax
- Public access modifier
ms.assetid: 284c9e1b-ed23-499b-9bc9-ad87c11485a5
ms.openlocfilehash: a5e9161132ba6d571daa30ce82e1bfb1dd2b064f
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
---
# <a name="public-visual-basic"></a><span data-ttu-id="b60c2-102">Public (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b60c2-102">Public (Visual Basic)</span></span>
<span data-ttu-id="b60c2-103">Spécifie ne qu’aucune restriction d’accès à un ou plusieurs éléments de programmation déclarés.</span><span class="sxs-lookup"><span data-stu-id="b60c2-103">Specifies that one or more declared programming elements have no access restrictions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b60c2-104">Notes</span><span class="sxs-lookup"><span data-stu-id="b60c2-104">Remarks</span></span>  
 <span data-ttu-id="b60c2-105">Si vous publiez un composant ou un ensemble de composants, tels que d’une bibliothèque de classes, vous souhaitez généralement les éléments de programmation accessibles par tout code qui interagit avec votre assembly.</span><span class="sxs-lookup"><span data-stu-id="b60c2-105">If you are publishing a component or set of components, such as a class library, you usually want the programming elements to be accessible by any code that interoperates with your assembly.</span></span> <span data-ttu-id="b60c2-106">Pour octroyer cet accès illimité sur un élément, vous pouvez déclarer avec `Public`.</span><span class="sxs-lookup"><span data-stu-id="b60c2-106">To confer such unlimited access on an element, you can declare it with `Public`.</span></span>  
  
 <span data-ttu-id="b60c2-107">Accès public est le niveau normal pour un élément de programmation lorsque vous n’avez pas besoin de restreindre l’accès.</span><span class="sxs-lookup"><span data-stu-id="b60c2-107">Public access is the normal level for a programming element when you do not need to limit access to it.</span></span> <span data-ttu-id="b60c2-108">Notez que le niveau d’accès d’un élément déclaré dans une interface, un module, une classe ou une structure de valeur par défaut est `Public` si vous ne déclarez pas une dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b60c2-108">Note that the access level of an element declared within an interface, module, class, or structure defaults to `Public` if you do not declare it otherwise.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="b60c2-109">Règles</span><span class="sxs-lookup"><span data-stu-id="b60c2-109">Rules</span></span>  
  
-   <span data-ttu-id="b60c2-110">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="b60c2-110">**Declaration Context.**</span></span> <span data-ttu-id="b60c2-111">Vous pouvez utiliser `Public` uniquement au niveau du module, interface ou espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b60c2-111">You can use `Public` only at module, interface, or namespace level.</span></span> <span data-ttu-id="b60c2-112">Cela signifie que le contexte de déclaration pour un `Public` élément doit être un fichier source, un espace de noms, une interface, un module, une classe ou une structure et ne peut pas être une procédure.</span><span class="sxs-lookup"><span data-stu-id="b60c2-112">This means the declaration context for a `Public` element must be a source file, namespace, interface, module, class, or structure, and cannot be a procedure.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="b60c2-113">Comportement</span><span class="sxs-lookup"><span data-stu-id="b60c2-113">Behavior</span></span>  
  
-   <span data-ttu-id="b60c2-114">**Niveau d’accès.**</span><span class="sxs-lookup"><span data-stu-id="b60c2-114">**Access Level.**</span></span> <span data-ttu-id="b60c2-115">Tout le code qui peut accéder à un module, classe ou structure peut accéder à ses `Public` éléments.</span><span class="sxs-lookup"><span data-stu-id="b60c2-115">All code that can access a module, class, or structure can access its `Public` elements.</span></span>  
  
-   <span data-ttu-id="b60c2-116">**Accès par défaut.**</span><span class="sxs-lookup"><span data-stu-id="b60c2-116">**Default Access.**</span></span> <span data-ttu-id="b60c2-117">Variables locales à l’intérieur d’une procédure reviennent par défaut à l’accès public et que vous ne pouvez pas utiliser les modificateurs d’accès sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="b60c2-117">Local variables inside a procedure default to public access, and you cannot use any access modifiers on them.</span></span>  
  
-   <span data-ttu-id="b60c2-118">**Modificateurs d’accès.**</span><span class="sxs-lookup"><span data-stu-id="b60c2-118">**Access Modifiers.**</span></span> <span data-ttu-id="b60c2-119">Les mots clés qui spécifient le niveau d’accès sont appelés *les modificateurs d’accès*.</span><span class="sxs-lookup"><span data-stu-id="b60c2-119">The keywords that specify access level are called *access modifiers*.</span></span> <span data-ttu-id="b60c2-120">Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b60c2-120">For a comparison of the access modifiers, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
 <span data-ttu-id="b60c2-121">Le modificateur `Public` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="b60c2-121">The `Public` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="b60c2-122">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-122">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [<span data-ttu-id="b60c2-123">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-123">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [<span data-ttu-id="b60c2-124">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-124">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="b60c2-125">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-125">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [<span data-ttu-id="b60c2-126">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-126">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="b60c2-127">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-127">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [<span data-ttu-id="b60c2-128">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-128">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="b60c2-129">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-129">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="b60c2-130">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-130">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [<span data-ttu-id="b60c2-131">Module (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-131">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)  
  
 [<span data-ttu-id="b60c2-132">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-132">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [<span data-ttu-id="b60c2-133">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-133">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="b60c2-134">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-134">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [<span data-ttu-id="b60c2-135">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="b60c2-135">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="b60c2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b60c2-136">See Also</span></span>  
 [<span data-ttu-id="b60c2-137">Protected</span><span class="sxs-lookup"><span data-stu-id="b60c2-137">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)  
 [<span data-ttu-id="b60c2-138">Friend</span><span class="sxs-lookup"><span data-stu-id="b60c2-138">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)  
 [<span data-ttu-id="b60c2-139">Private</span><span class="sxs-lookup"><span data-stu-id="b60c2-139">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)  
 <span data-ttu-id="b60c2-140">[Protégé privé](private-protected.md) </span><span class="sxs-lookup"><span data-stu-id="b60c2-140">[Private Protected](private-protected.md) </span></span>  
 <span data-ttu-id="b60c2-141">[Protected Friend](protected-friend.md) </span><span class="sxs-lookup"><span data-stu-id="b60c2-141">[Protected Friend](protected-friend.md) </span></span>  
 [<span data-ttu-id="b60c2-142">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b60c2-142">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)  
 [<span data-ttu-id="b60c2-143">Procédures</span><span class="sxs-lookup"><span data-stu-id="b60c2-143">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
 [<span data-ttu-id="b60c2-144">Structures</span><span class="sxs-lookup"><span data-stu-id="b60c2-144">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
 [<span data-ttu-id="b60c2-145">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="b60c2-145">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
