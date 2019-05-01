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
ms.openlocfilehash: 0c85564503f3c83e436044cd92ee3014945f1ef3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051869"
---
# <a name="public-visual-basic"></a><span data-ttu-id="cab90-102">Public (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cab90-102">Public (Visual Basic)</span></span>
<span data-ttu-id="cab90-103">Spécifie ne qu’aucune restriction d’accès à un ou plusieurs éléments de programmation déclarés.</span><span class="sxs-lookup"><span data-stu-id="cab90-103">Specifies that one or more declared programming elements have no access restrictions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cab90-104">Notes</span><span class="sxs-lookup"><span data-stu-id="cab90-104">Remarks</span></span>  
 <span data-ttu-id="cab90-105">Si vous publiez un composant ou un ensemble de composants, tels qu’une bibliothèque de classes, vous souhaitez généralement les éléments de programmation accessibles par tout code qui interagit avec votre assembly.</span><span class="sxs-lookup"><span data-stu-id="cab90-105">If you are publishing a component or set of components, such as a class library, you usually want the programming elements to be accessible by any code that interoperates with your assembly.</span></span> <span data-ttu-id="cab90-106">Pour octroyer cet accès illimité sur un élément, vous pouvez le déclarer avec `Public`.</span><span class="sxs-lookup"><span data-stu-id="cab90-106">To confer such unlimited access on an element, you can declare it with `Public`.</span></span>  
  
 <span data-ttu-id="cab90-107">L’accès public est le niveau normal pour un élément de programmation lorsque vous n’avez pas besoin de restreindre l’accès.</span><span class="sxs-lookup"><span data-stu-id="cab90-107">Public access is the normal level for a programming element when you do not need to limit access to it.</span></span> <span data-ttu-id="cab90-108">Notez que le niveau d’accès d’un élément déclaré dans une interface, un module, une classe ou une structure par défaut est `Public` si vous ne déclarez pas une dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cab90-108">Note that the access level of an element declared within an interface, module, class, or structure defaults to `Public` if you do not declare it otherwise.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="cab90-109">Règles</span><span class="sxs-lookup"><span data-stu-id="cab90-109">Rules</span></span>  
  
- <span data-ttu-id="cab90-110">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="cab90-110">**Declaration Context.**</span></span> <span data-ttu-id="cab90-111">Vous pouvez utiliser `Public` uniquement au niveau du module, interface ou espace de noms.</span><span class="sxs-lookup"><span data-stu-id="cab90-111">You can use `Public` only at module, interface, or namespace level.</span></span> <span data-ttu-id="cab90-112">Cela signifie que le contexte de déclaration pour un `Public` élément doit être un fichier source, un espace de noms, un module, une classe ou une structure et ne peut pas être une procédure.</span><span class="sxs-lookup"><span data-stu-id="cab90-112">This means the declaration context for a `Public` element must be a source file, namespace, interface, module, class, or structure, and cannot be a procedure.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="cab90-113">Comportement</span><span class="sxs-lookup"><span data-stu-id="cab90-113">Behavior</span></span>  
  
- <span data-ttu-id="cab90-114">**Niveau d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cab90-114">**Access Level.**</span></span> <span data-ttu-id="cab90-115">Tout le code qui peut accéder à un module, une classe ou une structure peut accéder à ses `Public` éléments.</span><span class="sxs-lookup"><span data-stu-id="cab90-115">All code that can access a module, class, or structure can access its `Public` elements.</span></span>  
  
- <span data-ttu-id="cab90-116">**Accès par défaut.**</span><span class="sxs-lookup"><span data-stu-id="cab90-116">**Default Access.**</span></span> <span data-ttu-id="cab90-117">Les variables locales à l’intérieur d’une procédure reviennent par défaut pour l’accès public et vous ne pouvez pas utiliser n’importe quel modificateur d’accès sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="cab90-117">Local variables inside a procedure default to public access, and you cannot use any access modifiers on them.</span></span>  
  
- <span data-ttu-id="cab90-118">**Modificateurs d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cab90-118">**Access Modifiers.**</span></span> <span data-ttu-id="cab90-119">Les mots clés qui spécifient le niveau d’accès sont appelés *modificateurs d’accès*.</span><span class="sxs-lookup"><span data-stu-id="cab90-119">The keywords that specify access level are called *access modifiers*.</span></span> <span data-ttu-id="cab90-120">Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cab90-120">For a comparison of the access modifiers, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
 <span data-ttu-id="cab90-121">Le modificateur `Public` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="cab90-121">The `Public` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="cab90-122">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-122">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [<span data-ttu-id="cab90-123">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-123">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [<span data-ttu-id="cab90-124">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-124">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="cab90-125">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-125">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [<span data-ttu-id="cab90-126">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-126">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="cab90-127">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-127">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [<span data-ttu-id="cab90-128">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-128">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="cab90-129">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-129">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="cab90-130">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-130">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [<span data-ttu-id="cab90-131">Module (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-131">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)  
  
 [<span data-ttu-id="cab90-132">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-132">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [<span data-ttu-id="cab90-133">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-133">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="cab90-134">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-134">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [<span data-ttu-id="cab90-135">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="cab90-135">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="cab90-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cab90-136">See also</span></span>

- [<span data-ttu-id="cab90-137">Protected</span><span class="sxs-lookup"><span data-stu-id="cab90-137">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)
- [<span data-ttu-id="cab90-138">Friend</span><span class="sxs-lookup"><span data-stu-id="cab90-138">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)
- [<span data-ttu-id="cab90-139">Private</span><span class="sxs-lookup"><span data-stu-id="cab90-139">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)
- [<span data-ttu-id="cab90-140">Private Protected</span><span class="sxs-lookup"><span data-stu-id="cab90-140">Private Protected</span></span>](private-protected.md)
- [<span data-ttu-id="cab90-141">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="cab90-141">Protected Friend</span></span>](protected-friend.md)
- [<span data-ttu-id="cab90-142">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cab90-142">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="cab90-143">Procédures</span><span class="sxs-lookup"><span data-stu-id="cab90-143">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="cab90-144">Structures</span><span class="sxs-lookup"><span data-stu-id="cab90-144">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="cab90-145">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="cab90-145">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
