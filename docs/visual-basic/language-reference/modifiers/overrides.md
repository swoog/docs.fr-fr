---
title: Overrides (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- Overrides
- vb.Overrides
helpviewer_keywords:
- properties [Visual Basic], redefining
- procedures [Visual Basic], overriding
- procedures [Visual Basic], redefining
- overriding
- Overrides keyword [Visual Basic]
- overriding, Overrides keyword
- properties [Visual Basic], overriding
ms.assetid: 9f5e6144-ce10-465e-842b-1a8f8760af90
ms.openlocfilehash: 7fff91d993743574d13030aa3d5cc1e462e76838
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64751027"
---
# <a name="overrides-visual-basic"></a><span data-ttu-id="b9596-102">Overrides (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b9596-102">Overrides (Visual Basic)</span></span>

<span data-ttu-id="b9596-103">Spécifie qu'une propriété ou procédure substitue une propriété ou procédure ayant un nom identique et ayant été héritée d'une classe de base.</span><span class="sxs-lookup"><span data-stu-id="b9596-103">Specifies that a property or procedure overrides an identically named property or procedure inherited from a base class.</span></span>

## <a name="rules"></a><span data-ttu-id="b9596-104">Règles</span><span class="sxs-lookup"><span data-stu-id="b9596-104">Rules</span></span>

- <span data-ttu-id="b9596-105">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="b9596-105">**Declaration Context.**</span></span> <span data-ttu-id="b9596-106">Vous pouvez utiliser `Overrides` uniquement dans une instruction de déclaration de propriété ou de procédure.</span><span class="sxs-lookup"><span data-stu-id="b9596-106">You can use `Overrides` only in a property or procedure declaration statement.</span></span>

- <span data-ttu-id="b9596-107">**Modificateurs combinés.**</span><span class="sxs-lookup"><span data-stu-id="b9596-107">**Combined Modifiers.**</span></span> <span data-ttu-id="b9596-108">Vous ne pouvez pas spécifier `Overrides` avec `Shadows` ou `Shared` dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="b9596-108">You cannot specify `Overrides` together with `Shadows` or `Shared` in the same declaration.</span></span> <span data-ttu-id="b9596-109">Comme un élément de substitution est implicitement substituable, vous ne pouvez pas combiner `Overridable` avec `Overrides`.</span><span class="sxs-lookup"><span data-stu-id="b9596-109">Because an overriding element is implicitly overridable, you cannot combine `Overridable` with `Overrides`.</span></span>

- <span data-ttu-id="b9596-110">**Faire correspondre les Signatures.**</span><span class="sxs-lookup"><span data-stu-id="b9596-110">**Matching Signatures.**</span></span> <span data-ttu-id="b9596-111">La signature de cette déclaration doit correspondre exactement à la *signature* de la propriété ou procédure qu’elle substitue.</span><span class="sxs-lookup"><span data-stu-id="b9596-111">The signature of this declaration must exactly match the *signature* of the property or procedure that it overrides.</span></span> <span data-ttu-id="b9596-112">Cela signifie que les listes de paramètres doivent avoir le même nombre de paramètres, dans le même ordre, avec les mêmes types de données.</span><span class="sxs-lookup"><span data-stu-id="b9596-112">This means the parameter lists must have the same number of parameters, in the same order, with the same data types.</span></span>

  <span data-ttu-id="b9596-113">Outre la signature, la déclaration de substitution doit également correspondre exactement à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b9596-113">In addition to the signature, the overriding declaration must also exactly match the following:</span></span>

  - <span data-ttu-id="b9596-114">Niveau d'accès</span><span class="sxs-lookup"><span data-stu-id="b9596-114">The access level</span></span>

  - <span data-ttu-id="b9596-115">Type de retour, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="b9596-115">The return type, if any</span></span>

- <span data-ttu-id="b9596-116">**Signatures génériques.**</span><span class="sxs-lookup"><span data-stu-id="b9596-116">**Generic Signatures.**</span></span> <span data-ttu-id="b9596-117">Pour une procédure générique, la signature inclut le nombre de paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="b9596-117">For a generic procedure, the signature includes the number of type parameters.</span></span> <span data-ttu-id="b9596-118">Par conséquent, la déclaration de substitution doit correspondre à la version de la classe de base également selon ce critère.</span><span class="sxs-lookup"><span data-stu-id="b9596-118">Therefore, the overriding declaration must match the base class version in that respect as well.</span></span>

- <span data-ttu-id="b9596-119">**Correspondance supplémentaire.**</span><span class="sxs-lookup"><span data-stu-id="b9596-119">**Additional Matching.**</span></span> <span data-ttu-id="b9596-120">Cette déclaration doit non seulement correspondre à la signature de la version de la classe de base, mais aussi lui correspondre selon les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="b9596-120">In addition to matching the signature of the base class version, this declaration must also match it in the following respects:</span></span>

  - <span data-ttu-id="b9596-121">Modificateur de niveau d’accès (tel que [Public](../../../visual-basic/language-reference/modifiers/public.md))</span><span class="sxs-lookup"><span data-stu-id="b9596-121">Access-level modifier (such as [Public](../../../visual-basic/language-reference/modifiers/public.md))</span></span>

  - <span data-ttu-id="b9596-122">Mécanisme de passage de chaque paramètre ([ByVal](../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../visual-basic/language-reference/modifiers/byref.md))</span><span class="sxs-lookup"><span data-stu-id="b9596-122">Passing mechanism of each parameter ([ByVal](../../../visual-basic/language-reference/modifiers/byval.md) or [ByRef](../../../visual-basic/language-reference/modifiers/byref.md))</span></span>

  - <span data-ttu-id="b9596-123">Listes de contraintes pour chaque paramètre de type d'une procédure générique</span><span class="sxs-lookup"><span data-stu-id="b9596-123">Constraint lists on each type parameter of a generic procedure</span></span>

- <span data-ttu-id="b9596-124">**Occultation et substitution.**</span><span class="sxs-lookup"><span data-stu-id="b9596-124">**Shadowing and Overriding.**</span></span> <span data-ttu-id="b9596-125">L'occultation et la substitution redéfinissent toutes les deux un élément hérité, mais il existe des différences importantes entre ces deux approches.</span><span class="sxs-lookup"><span data-stu-id="b9596-125">Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches.</span></span> <span data-ttu-id="b9596-126">Pour plus d’informations, consultez [occultation dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md).</span><span class="sxs-lookup"><span data-stu-id="b9596-126">For more information, see [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md).</span></span>

<span data-ttu-id="b9596-127">Si vous utilisez `Overrides`, le compilateur ajoute implicitement `Overloads` afin que vos API de bibliothèque fonctionnent plus facilement avec C#.</span><span class="sxs-lookup"><span data-stu-id="b9596-127">If you use `Overrides`, the compiler implicitly adds `Overloads` so that your library APIs work with C# more easily.</span></span>

<span data-ttu-id="b9596-128">Le modificateur `Overrides` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="b9596-128">The `Overrides` modifier can be used in these contexts:</span></span>

- [<span data-ttu-id="b9596-129">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="b9596-129">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)

- [<span data-ttu-id="b9596-130">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="b9596-130">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)

- [<span data-ttu-id="b9596-131">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="b9596-131">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)

## <a name="see-also"></a><span data-ttu-id="b9596-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9596-132">See also</span></span>

- [<span data-ttu-id="b9596-133">MustOverride</span><span class="sxs-lookup"><span data-stu-id="b9596-133">MustOverride</span></span>](../../../visual-basic/language-reference/modifiers/mustoverride.md)
- [<span data-ttu-id="b9596-134">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="b9596-134">NotOverridable</span></span>](../../../visual-basic/language-reference/modifiers/notoverridable.md)
- [<span data-ttu-id="b9596-135">Overridable</span><span class="sxs-lookup"><span data-stu-id="b9596-135">Overridable</span></span>](../../../visual-basic/language-reference/modifiers/overridable.md)
- [<span data-ttu-id="b9596-136">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9596-136">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="b9596-137">Occultation dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9596-137">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
- [<span data-ttu-id="b9596-138">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9596-138">Generic Types in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="b9596-139">Liste de types</span><span class="sxs-lookup"><span data-stu-id="b9596-139">Type List</span></span>](../../../visual-basic/language-reference/statements/type-list.md)
