---
title: Private protégé (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Private Protected keyword [Visual Basic]
- Private Protected keyword [Visual Basic], syntax
ms.openlocfilehash: fea43558ac0fe8181f2786b69f2621346d446b2e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61920495"
---
# <a name="private-protected-visual-basic"></a><span data-ttu-id="28dde-102">Private protégé (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="28dde-102">Private Protected (Visual Basic)</span></span>

<span data-ttu-id="28dde-103">La combinaison de mots clés `Private Protected` est un modificateur d’accès de membre.</span><span class="sxs-lookup"><span data-stu-id="28dde-103">The `Private Protected` keyword combination is a member access modifier.</span></span> <span data-ttu-id="28dde-104">Un `Private Protected` membre est accessible par tous les membres de sa classe conteneur, ainsi que par les types dérivés de la classe conteneur, mais uniquement si elles sont trouvent dans son assembly conteneur.</span><span class="sxs-lookup"><span data-stu-id="28dde-104">A `Private Protected` member is accessible by all members in its containing class, as well as by types derived from the containing class, but only if they are found in its containing assembly.</span></span>

<span data-ttu-id="28dde-105">Vous pouvez spécifier `Private Protected` uniquement sur les membres de classes ; vous ne pouvez pas appliquer `Private Protected` aux membres d’une structure, car les structures ne peuvent pas être héritées.</span><span class="sxs-lookup"><span data-stu-id="28dde-105">You can specify `Private Protected` only on members of classes; you cannot apply `Private Protected` to members of a structure because structures cannot be inherited.</span></span>

<span data-ttu-id="28dde-106">Le `Private Protected` modificateur d’accès est pris en charge par Visual Basic 15.5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="28dde-106">The `Private Protected` access modifier is supported by Visual Basic 15.5 and later.</span></span> <span data-ttu-id="28dde-107">Pour l’utiliser, vous pouvez ajouter l’élément suivant à votre projet Visual Basic (\*.vbproj) fichier.</span><span class="sxs-lookup"><span data-stu-id="28dde-107">To use it, you can add the following element to your Visual Basic project (\*.vbproj) file.</span></span> <span data-ttu-id="28dde-108">Comme tant que Visual Basic 15.5 ou version ultérieure est installé sur votre système, il vous permet de tirer parti de toutes les fonctionnalités de langage pris en charge par la dernière version du compilateur Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="28dde-108">As long as Visual Basic 15.5 or later is installed on your system, it lets you take advantage of all the language features supported by the latest version of the Visual Basic compiler:</span></span>

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="28dde-109">Pour plus d’informations, consultez [définition de la version de langage Visual Basic](../../language-reference/configure-language-version.md).</span><span class="sxs-lookup"><span data-stu-id="28dde-109">For more information see [setting the Visual Basic language version](../../language-reference/configure-language-version.md).</span></span>

> [!NOTE]
> <span data-ttu-id="28dde-110">Dans Visual Studio, en sélectionnant la touche F1 sur `private protected` fournit une aide pour soit [privé](private.md) ou [protégé](protected.md).</span><span class="sxs-lookup"><span data-stu-id="28dde-110">In Visual Studio, selecting F1 help on `private protected` provides help for either [private](private.md) or [protected](protected.md).</span></span> <span data-ttu-id="28dde-111">L’IDE choisit le jeton unique sous le curseur plutôt que le mot composé.</span><span class="sxs-lookup"><span data-stu-id="28dde-111">The IDE picks the single token under the cursor rather than the compound word.</span></span>

## <a name="rules"></a><span data-ttu-id="28dde-112">Règles</span><span class="sxs-lookup"><span data-stu-id="28dde-112">Rules</span></span>

- <span data-ttu-id="28dde-113">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="28dde-113">**Declaration Context.**</span></span> <span data-ttu-id="28dde-114">Vous pouvez utiliser `Private Protected` uniquement au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="28dde-114">You can use `Private Protected` only at the class level.</span></span> <span data-ttu-id="28dde-115">Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être une fichier source, un espace de noms, un module, une structure ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="28dde-115">This means the declaration context for a `Protected` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.</span></span>

## <a name="behavior"></a><span data-ttu-id="28dde-116">Comportement</span><span class="sxs-lookup"><span data-stu-id="28dde-116">Behavior</span></span>

- <span data-ttu-id="28dde-117">**Niveau d’accès.**</span><span class="sxs-lookup"><span data-stu-id="28dde-117">**Access Level.**</span></span> <span data-ttu-id="28dde-118">Tout le code dans une classe peut accéder à ses éléments.</span><span class="sxs-lookup"><span data-stu-id="28dde-118">All code in a class can access its elements.</span></span> <span data-ttu-id="28dde-119">Code dans toute classe qui dérive d’une classe de base et est contenue dans le même assembly peut accéder à tous les `Private Protected` éléments de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="28dde-119">Code in any class that derives from a base class and is contained in the same assembly can access all the `Private Protected` elements of the base class.</span></span> <span data-ttu-id="28dde-120">Toutefois, le code dans toute classe qui dérive d’une classe de base et est contenue dans un autre assembly ne peut pas accéder à la classe de base `Private Protected` éléments.</span><span class="sxs-lookup"><span data-stu-id="28dde-120">However, code in any class that derives from a base class and is contained in a different assembly can't access the base class `Private Protected` elements.</span></span>

- <span data-ttu-id="28dde-121">**Modificateurs d’accès.**</span><span class="sxs-lookup"><span data-stu-id="28dde-121">**Access Modifiers.**</span></span> <span data-ttu-id="28dde-122">Les mots clés qui spécifient le niveau d’accès sont appelés *modificateurs d’accès*.</span><span class="sxs-lookup"><span data-stu-id="28dde-122">The keywords that specify access level are called *access modifiers*.</span></span> <span data-ttu-id="28dde-123">Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="28dde-123">For a comparison of the access modifiers, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>

<span data-ttu-id="28dde-124">Le modificateur `Private Protected` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="28dde-124">The `Private Protected` modifier can be used in these contexts:</span></span>

- <span data-ttu-id="28dde-125">[Class, instruction](../../../visual-basic/language-reference/statements/class-statement.md) d’une classe imbriquée</span><span class="sxs-lookup"><span data-stu-id="28dde-125">[Class Statement](../../../visual-basic/language-reference/statements/class-statement.md) of a nested class</span></span>

- [<span data-ttu-id="28dde-126">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-126">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)

- [<span data-ttu-id="28dde-127">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-127">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)

- <span data-ttu-id="28dde-128">[Delegate, instruction](../../../visual-basic/language-reference/statements/delegate-statement.md) d’un délégué imbriqué dans une classe</span><span class="sxs-lookup"><span data-stu-id="28dde-128">[Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) of a delegate nested in a class</span></span>

- [<span data-ttu-id="28dde-129">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-129">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)

- <span data-ttu-id="28dde-130">[Enum, instruction](../../../visual-basic/language-reference/statements/enum-statement.md) d’une énumération imbriquée dans une classe</span><span class="sxs-lookup"><span data-stu-id="28dde-130">[Enum Statement](../../../visual-basic/language-reference/statements/enum-statement.md) of an enumeration nested in a class</span></span>

- [<span data-ttu-id="28dde-131">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-131">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)

- [<span data-ttu-id="28dde-132">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-132">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)

- <span data-ttu-id="28dde-133">[Interface, instruction](../../../visual-basic/language-reference/statements/interface-statement.md) d’une interface imbriquée dans une classe</span><span class="sxs-lookup"><span data-stu-id="28dde-133">[Interface Statement](../../../visual-basic/language-reference/statements/interface-statement.md) of an interface nested in a class</span></span>

- [<span data-ttu-id="28dde-134">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-134">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)

- <span data-ttu-id="28dde-135">[Structure instruction](../../../visual-basic/language-reference/statements/structure-statement.md) d’une structure imbriquée dans une classe</span><span class="sxs-lookup"><span data-stu-id="28dde-135">[Structure Statement](../../../visual-basic/language-reference/statements/structure-statement.md) of a structure nested in a class</span></span>

- [<span data-ttu-id="28dde-136">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="28dde-136">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)

## <a name="see-also"></a><span data-ttu-id="28dde-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28dde-137">See also</span></span>

- [<span data-ttu-id="28dde-138">Public</span><span class="sxs-lookup"><span data-stu-id="28dde-138">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="28dde-139">Protected</span><span class="sxs-lookup"><span data-stu-id="28dde-139">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)
- [<span data-ttu-id="28dde-140">Friend</span><span class="sxs-lookup"><span data-stu-id="28dde-140">Friend</span></span>](friend.md)
- [<span data-ttu-id="28dde-141">Private</span><span class="sxs-lookup"><span data-stu-id="28dde-141">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)
- [<span data-ttu-id="28dde-142">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="28dde-142">Protected Friend</span></span>](./protected-friend.md)
- [<span data-ttu-id="28dde-143">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="28dde-143">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="28dde-144">Procédures</span><span class="sxs-lookup"><span data-stu-id="28dde-144">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="28dde-145">Structures</span><span class="sxs-lookup"><span data-stu-id="28dde-145">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="28dde-146">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="28dde-146">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
