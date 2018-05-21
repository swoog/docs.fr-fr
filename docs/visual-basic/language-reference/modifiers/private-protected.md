---
title: Protégé privé (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Private Protected keyword [Visual Basic]
- Private Protected keyword [Visual Basic], syntax
ms.openlocfilehash: 23fd6583182a1fee544d0458dc3fc390aed86b9f
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
---
# <a name="private-protected-visual-basic"></a><span data-ttu-id="18a92-102">Protégé privé (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="18a92-102">Private Protected (Visual Basic)</span></span>

<span data-ttu-id="18a92-103">Le `Private Protected` combinaison de mots clés est un modificateur d’accès du membre.</span><span class="sxs-lookup"><span data-stu-id="18a92-103">The `Private Protected` keyword combination is a member access modifier.</span></span> <span data-ttu-id="18a92-104">A `Private Protected` membre est accessible par tous les membres de sa classe conteneur, ainsi que par les types dérivés de la classe conteneur, mais uniquement si elles se trouvent dans l’assembly qui le contient.</span><span class="sxs-lookup"><span data-stu-id="18a92-104">A `Private Protected` member is accessible by all members in its containing class, as well as by types derived from the containing class, but only if they are found in its containing assembly.</span></span> 

<span data-ttu-id="18a92-105">Vous pouvez spécifier `Private Protected` uniquement sur les membres de classes ; vous ne pouvez pas appliquer `Private Protected` aux membres d’une structure, car les structures ne peuvent pas être héritées.</span><span class="sxs-lookup"><span data-stu-id="18a92-105">You can specify `Private Protected` only on members of classes; you cannot apply `Private Protected` to members of a structure because structures cannot be inherited.</span></span>

<span data-ttu-id="18a92-106">Le `Private Protected` modificateur d’accès est prise en charge par Visual Basic 15.5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="18a92-106">The `Private Protected` access modifier is supported by Visual Basic 15.5 and later.</span></span> <span data-ttu-id="18a92-107">Pour l’utiliser, vous pouvez ajouter l’élément suivant à votre fichier projet (\*.vbproj) de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="18a92-107">To use it, you can add the following element to your Visual Basic project (\*.vbproj) file.</span></span> <span data-ttu-id="18a92-108">En tant que Visual Basic 15.5 ou version ultérieure est installé sur votre système, il vous permet de tirer parti de toutes les fonctionnalités de langage pris en charge par la dernière version du compilateur Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="18a92-108">As long as Visual Basic 15.5 or later is installed on your system, it lets you take advantage of all the language features supported by the latest version of the Visual Basic compiler:</span></span>

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

> [!NOTE]
> <span data-ttu-id="18a92-109">Dans Visual Studio, en sélectionnant la touche F1 sur `private protected` fournit une aide pour soit [privé](private.md) ou [protégé](protected.md).</span><span class="sxs-lookup"><span data-stu-id="18a92-109">In Visual Studio, selecting F1 help on `private protected` provides help for either [private](private.md) or [protected](protected.md).</span></span> <span data-ttu-id="18a92-110">L’IDE choisit le jeton unique sous le curseur plutôt que le mot composé.</span><span class="sxs-lookup"><span data-stu-id="18a92-110">The IDE picks the single token under the cursor rather than the compound word.</span></span>

## <a name="rules"></a><span data-ttu-id="18a92-111">Règles</span><span class="sxs-lookup"><span data-stu-id="18a92-111">Rules</span></span>

- <span data-ttu-id="18a92-112">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="18a92-112">**Declaration Context.**</span></span> <span data-ttu-id="18a92-113">Vous pouvez utiliser `Private Protected` uniquement au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="18a92-113">You can use `Private Protected` only at the class level.</span></span> <span data-ttu-id="18a92-114">Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être un fichier source, espace de noms, interface, un module, structure ou procédure.</span><span class="sxs-lookup"><span data-stu-id="18a92-114">This means the declaration context for a `Protected` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.</span></span>

## <a name="behavior"></a><span data-ttu-id="18a92-115">Comportement</span><span class="sxs-lookup"><span data-stu-id="18a92-115">Behavior</span></span>

- <span data-ttu-id="18a92-116">**Niveau d’accès.**</span><span class="sxs-lookup"><span data-stu-id="18a92-116">**Access Level.**</span></span> <span data-ttu-id="18a92-117">Tout le code dans une classe peut accéder à ses éléments.</span><span class="sxs-lookup"><span data-stu-id="18a92-117">All code in a class can access its elements.</span></span> <span data-ttu-id="18a92-118">Le code dans n’importe quelle classe qui dérive d’une classe de base et qui est contenue dans le même assembly peut accéder à tous les `Private Protected` les éléments de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="18a92-118">Code in any class that derives from a base class and is contained in the same assembly can access all the `Private Protected` elements of the base class.</span></span> <span data-ttu-id="18a92-119">Toutefois, le code dans n’importe quelle classe qui dérive d’une classe de base et qui est contenue dans un autre assembly Impossible d’accéder à la classe de base `Private Protected` éléments.</span><span class="sxs-lookup"><span data-stu-id="18a92-119">However, code in any class that derives from a base class and is contained in a different assembly can't access the base class `Private Protected` elements.</span></span>

- <span data-ttu-id="18a92-120">**Modificateurs d’accès.**</span><span class="sxs-lookup"><span data-stu-id="18a92-120">**Access Modifiers.**</span></span> <span data-ttu-id="18a92-121">Les mots clés qui spécifient le niveau d’accès sont appelés *les modificateurs d’accès*.</span><span class="sxs-lookup"><span data-stu-id="18a92-121">The keywords that specify access level are called *access modifiers*.</span></span> <span data-ttu-id="18a92-122">Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="18a92-122">For a comparison of the access modifiers, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>
  
 <span data-ttu-id="18a92-123">Le modificateur `Private Protected` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="18a92-123">The `Private Protected` modifier can be used in these contexts:</span></span>  
  
 <span data-ttu-id="18a92-124">[La classe](../../../visual-basic/language-reference/statements/class-statement.md) d’une classe imbriquée</span><span class="sxs-lookup"><span data-stu-id="18a92-124">[Class Statement](../../../visual-basic/language-reference/statements/class-statement.md) of a nested class</span></span>  
  
 [<span data-ttu-id="18a92-125">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-125">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [<span data-ttu-id="18a92-126">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-126">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 <span data-ttu-id="18a92-127">[Delegate, instruction](../../../visual-basic/language-reference/statements/delegate-statement.md) d’un délégué imbriqué dans une classe</span><span class="sxs-lookup"><span data-stu-id="18a92-127">[Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) of a delegate nested in a class</span></span>  
  
 [<span data-ttu-id="18a92-128">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-128">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 <span data-ttu-id="18a92-129">[Enum, instruction](../../../visual-basic/language-reference/statements/enum-statement.md) d’une eumeration imbriquée dans une classe</span><span class="sxs-lookup"><span data-stu-id="18a92-129">[Enum Statement](../../../visual-basic/language-reference/statements/enum-statement.md) of an eumeration nested in a class</span></span> 
  
 [<span data-ttu-id="18a92-130">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-130">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="18a92-131">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-131">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 <span data-ttu-id="18a92-132">[Interface, instruction](../../../visual-basic/language-reference/statements/interface-statement.md) d’une interface imbriquée dans une classe</span><span class="sxs-lookup"><span data-stu-id="18a92-132">[Interface Statement](../../../visual-basic/language-reference/statements/interface-statement.md) of an interface nested in a class</span></span> 
  
 [<span data-ttu-id="18a92-133">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-133">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 <span data-ttu-id="18a92-134">[Instruction de la structure](../../../visual-basic/language-reference/statements/structure-statement.md) d’une structure imbriquée dans une classe</span><span class="sxs-lookup"><span data-stu-id="18a92-134">[Structure Statement](../../../visual-basic/language-reference/statements/structure-statement.md) of a structure nested in a class</span></span> 
  
 [<span data-ttu-id="18a92-135">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="18a92-135">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="18a92-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18a92-136">See Also</span></span>

[<span data-ttu-id="18a92-137">Public</span><span class="sxs-lookup"><span data-stu-id="18a92-137">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)  
[<span data-ttu-id="18a92-138">Protected</span><span class="sxs-lookup"><span data-stu-id="18a92-138">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)  
<span data-ttu-id="18a92-139">[Friend](friend.md) </span><span class="sxs-lookup"><span data-stu-id="18a92-139">[Friend](friend.md) </span></span>  
[<span data-ttu-id="18a92-140">Private</span><span class="sxs-lookup"><span data-stu-id="18a92-140">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)  
<span data-ttu-id="18a92-141">[Protected Friend](./protected-friend.md) </span><span class="sxs-lookup"><span data-stu-id="18a92-141">[Protected Friend](./protected-friend.md) </span></span>  
[<span data-ttu-id="18a92-142">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="18a92-142">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)  
[<span data-ttu-id="18a92-143">Procédures</span><span class="sxs-lookup"><span data-stu-id="18a92-143">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
[<span data-ttu-id="18a92-144">Structures</span><span class="sxs-lookup"><span data-stu-id="18a92-144">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
[<span data-ttu-id="18a92-145">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="18a92-145">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
