---
title: Contrôle d'accès
description: Découvrez comment contrôler l’accès aux éléments de programmation, tels que les types, méthodes et fonctions, dans le F# langage de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: 8db178b26f3beb6ce95bff84ccad9ac9e8c40ce7
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612805"
---
# <a name="access-control"></a><span data-ttu-id="9eeff-103">Contrôle d'accès</span><span class="sxs-lookup"><span data-stu-id="9eeff-103">Access Control</span></span>

<span data-ttu-id="9eeff-104">*Contrôle d’accès* fait référence à la déclaration de clients qui peuvent utiliser certains éléments de programme, tels que les types, méthodes et fonctions.</span><span class="sxs-lookup"><span data-stu-id="9eeff-104">*Access control* refers to declaring which clients can use certain program elements, such as types, methods, and functions.</span></span>

## <a name="basics-of-access-control"></a><span data-ttu-id="9eeff-105">Principes de base du contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="9eeff-105">Basics of Access Control</span></span>

<span data-ttu-id="9eeff-106">Dans F#, les spécificateurs de contrôle d’accès `public`, `internal`, et `private` peuvent être appliquées à des modules, types, méthodes, des définitions de valeur, fonctions, propriétés et champs explicites.</span><span class="sxs-lookup"><span data-stu-id="9eeff-106">In F#, the access control specifiers `public`, `internal`, and `private` can be applied to modules, types, methods, value definitions, functions, properties, and explicit fields.</span></span>

- <span data-ttu-id="9eeff-107">`public` Indique que l’entité est accessible par tous les appelants.</span><span class="sxs-lookup"><span data-stu-id="9eeff-107">`public` indicates that the entity can be accessed by all callers.</span></span>

- <span data-ttu-id="9eeff-108">`internal` Indique que l’entité est accessible uniquement à partir du même assembly.</span><span class="sxs-lookup"><span data-stu-id="9eeff-108">`internal` indicates that the entity can be accessed only from the same assembly.</span></span>

- <span data-ttu-id="9eeff-109">`private` Indique que l’entité est accessible uniquement à partir de type ou un module englobant.</span><span class="sxs-lookup"><span data-stu-id="9eeff-109">`private` indicates that the entity can be accessed only from the enclosing type or module.</span></span>

> [!NOTE]
> <span data-ttu-id="9eeff-110">Le spécificateur d’accès `protected` n’est pas utilisé dans F#, bien qu’il soit acceptable si vous utilisez des types créés dans les langages qui prennent en charge `protected` accès.</span><span class="sxs-lookup"><span data-stu-id="9eeff-110">The access specifier `protected` is not used in F#, although it is acceptable if you are using types authored in languages that do support `protected` access.</span></span> <span data-ttu-id="9eeff-111">Par conséquent, si vous substituez une méthode protégée, votre méthode reste accessible uniquement au sein de la classe et ses descendants.</span><span class="sxs-lookup"><span data-stu-id="9eeff-111">Therefore, if you override a protected method, your method remains accessible only within the class and its descendents.</span></span>

<span data-ttu-id="9eeff-112">En général, le spécificateur est placé devant le nom de l’entité, sauf quand une `mutable` ou `inline` spécificateur est utilisé, qui apparaît après le spécificateur de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9eeff-112">In general, the specifier is put in front of the name of the entity, except when a `mutable` or `inline` specifier is used, which appear after the access control specifier.</span></span>

<span data-ttu-id="9eeff-113">Si aucun spécificateur d’accès n’est utilisé, la valeur par défaut est `public`, à l’exception de `let` liaisons dans un type, qui sont toujours `private` au type.</span><span class="sxs-lookup"><span data-stu-id="9eeff-113">If no access specifier is used, the default is `public`, except for `let` bindings in a type, which are always `private` to the type.</span></span>

<span data-ttu-id="9eeff-114">Signatures dans F# fournissent un autre mécanisme pour contrôler l’accès à F# éléments de programme.</span><span class="sxs-lookup"><span data-stu-id="9eeff-114">Signatures in F# provide another mechanism for controlling access to F# program elements.</span></span> <span data-ttu-id="9eeff-115">Les signatures ne sont pas requises pour le contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9eeff-115">Signatures are not required for access control.</span></span> <span data-ttu-id="9eeff-116">Pour plus d’informations, consultez [Signatures](signatures.md).</span><span class="sxs-lookup"><span data-stu-id="9eeff-116">For more information, see [Signatures](signatures.md).</span></span>

## <a name="rules-for-access-control"></a><span data-ttu-id="9eeff-117">Règles de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="9eeff-117">Rules for Access Control</span></span>

<span data-ttu-id="9eeff-118">Contrôle d’accès est soumis aux règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eeff-118">Access control is subject to the following rules:</span></span>

- <span data-ttu-id="9eeff-119">Déclarations d’héritage (autrement dit, l’utilisation de `inherit` pour spécifier une classe de base pour une classe), déclarations d’interface (c'est-à-dire spécifier qu’une classe implémente une interface) et d’abstraire membres ont toujours la même accessibilité que le type englobant.</span><span class="sxs-lookup"><span data-stu-id="9eeff-119">Inheritance declarations (that is, the use of `inherit` to specify a base class for a class), interface declarations (that is, specifying that a class implements an interface), and abstract members always have the same accessibility as the enclosing type.</span></span> <span data-ttu-id="9eeff-120">Par conséquent, un spécificateur de contrôle d’accès ne peut pas être utilisé sur ces constructions.</span><span class="sxs-lookup"><span data-stu-id="9eeff-120">Therefore, an access control specifier cannot be used on these constructs.</span></span>

- <span data-ttu-id="9eeff-121">Accessibilité pour les cas individuels dans une union discriminée est déterminée par l’accessibilité de l’union discriminée lui-même.</span><span class="sxs-lookup"><span data-stu-id="9eeff-121">Accessibility for individual cases in a discriminated union is determined by the accessibility of the discriminated union itself.</span></span> <span data-ttu-id="9eeff-122">Autrement dit, un cas d’union particulier n’est pas moins accessible que l’union elle-même.</span><span class="sxs-lookup"><span data-stu-id="9eeff-122">That is, a particular union case is no less accessible than the union itself.</span></span>

- <span data-ttu-id="9eeff-123">Accessibilité pour les champs individuels d’un type d’enregistrement ne peut pas est déterminée par l’accessibilité de l’enregistrement lui-même.</span><span class="sxs-lookup"><span data-stu-id="9eeff-123">Accessibility for individual fields of a record type cannot is determined by the accessibility of the record itself.</span></span> <span data-ttu-id="9eeff-124">Autrement dit, une étiquette d’enregistrement particulier n’est pas moins accessible que l’enregistrement lui-même.</span><span class="sxs-lookup"><span data-stu-id="9eeff-124">That is, a particular record label is no less accessible than the record itself.</span></span>

## <a name="example"></a><span data-ttu-id="9eeff-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="9eeff-125">Example</span></span>

<span data-ttu-id="9eeff-126">Le code suivant illustre l’utilisation de spécificateurs de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="9eeff-126">The following code illustrates the use of access control specifiers.</span></span> <span data-ttu-id="9eeff-127">Il existe deux fichiers dans le projet, `Module1.fs` et `Module2.fs`.</span><span class="sxs-lookup"><span data-stu-id="9eeff-127">There are two files in the project, `Module1.fs` and `Module2.fs`.</span></span> <span data-ttu-id="9eeff-128">Chaque fichier est implicitement un module.</span><span class="sxs-lookup"><span data-stu-id="9eeff-128">Each file is implicitly a module.</span></span> <span data-ttu-id="9eeff-129">Par conséquent, il existe deux modules, `Module1` et `Module2`.</span><span class="sxs-lookup"><span data-stu-id="9eeff-129">Therefore, there are two modules, `Module1` and `Module2`.</span></span> <span data-ttu-id="9eeff-130">Un type privé et un type interne sont définis dans `Module1`.</span><span class="sxs-lookup"><span data-stu-id="9eeff-130">A private type and an internal type are defined in `Module1`.</span></span> <span data-ttu-id="9eeff-131">Le type privé n’est pas accessible à partir de `Module2`, mais le type interne.</span><span class="sxs-lookup"><span data-stu-id="9eeff-131">The private type cannot be accessed from `Module2`, but the internal type can.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/access-control/snippet1.fs)]

<span data-ttu-id="9eeff-132">Le code suivant teste l’accessibilité des types créés dans `Module1.fs`.</span><span class="sxs-lookup"><span data-stu-id="9eeff-132">The following code tests the accessibility of the types created in `Module1.fs`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/access-control/snippet2.fs)]

## <a name="see-also"></a><span data-ttu-id="9eeff-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eeff-133">See also</span></span>

- [<span data-ttu-id="9eeff-134">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="9eeff-134">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="9eeff-135">Signatures</span><span class="sxs-lookup"><span data-stu-id="9eeff-135">Signatures</span></span>](signatures.md)