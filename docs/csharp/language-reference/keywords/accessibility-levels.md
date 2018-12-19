---
title: Niveaux d’accessibilité - Référence C#
ms.custom: seodec18
ms.date: 12/06/2017
helpviewer_keywords:
- access modifiers [C#], accessibility levels
- accessibility levels
ms.assetid: dc083921-0073-413e-8936-a613e8bb7df4
ms.openlocfilehash: 1bd4c063afe175b5585e5f732ebddbe1a271c8b3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243775"
---
# <a name="accessibility-levels-c-reference"></a><span data-ttu-id="9e256-102">Niveaux d’accessibilité (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9e256-102">Accessibility Levels (C# Reference)</span></span>

<span data-ttu-id="9e256-103">Utilisez les modificateurs d’accès `public`, `protected`, `internal` ou `private` pour spécifier l’un des niveaux d’accessibilité déclarés ci-dessous pour les membres.</span><span class="sxs-lookup"><span data-stu-id="9e256-103">Use the access modifiers, `public`, `protected`, `internal`, or `private`, to specify one of the following declared accessibility levels for members.</span></span>  
  
|<span data-ttu-id="9e256-104">Accessibilité déclarée</span><span class="sxs-lookup"><span data-stu-id="9e256-104">Declared accessibility</span></span>|<span data-ttu-id="9e256-105">Signification</span><span class="sxs-lookup"><span data-stu-id="9e256-105">Meaning</span></span>|  
|----------------------------|-------------|  
|[`public`](public.md)|<span data-ttu-id="9e256-106">L’accès n’est pas limité.</span><span class="sxs-lookup"><span data-stu-id="9e256-106">Access is not restricted.</span></span>|  
|[`protected`](protected.md)|<span data-ttu-id="9e256-107">L’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="9e256-107">Access is limited to the containing class or types derived from the containing class.</span></span>|  
|[`internal`](internal.md)|<span data-ttu-id="9e256-108">L’accès est limité à l’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="9e256-108">Access is limited to the current assembly.</span></span>|  
|[`protected internal`](protected-internal.md)|<span data-ttu-id="9e256-109">L’accès est limité à l’assembly actuel ou aux types dérivés de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="9e256-109">Access is limited to the current assembly or types derived from the containing class.</span></span>|  
|[`private`](private.md)|<span data-ttu-id="9e256-110">L’accès est limité au type conteneur.</span><span class="sxs-lookup"><span data-stu-id="9e256-110">Access is limited to the containing type.</span></span>|  
|[`private protected`](private-protected.md)|<span data-ttu-id="9e256-111">L’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur dans l’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="9e256-111">Access is limited to the containing class or types derived from the containing class within the current assembly.</span></span> <span data-ttu-id="9e256-112">Disponible depuis C# 7.2.</span><span class="sxs-lookup"><span data-stu-id="9e256-112">Available since C# 7.2.</span></span> |  
  
 <span data-ttu-id="9e256-113">Vous ne pouvez spécifier qu’un seul modificateur d’accès pour un membre ou un type, sauf si vous utilisez les combinaisons `protected internal` ou `private protected`.</span><span class="sxs-lookup"><span data-stu-id="9e256-113">Only one access modifier is allowed for a member or type, except when you use the `protected internal` or `private protected` combinations.</span></span>  
  
 <span data-ttu-id="9e256-114">Les modificateurs d’accès ne sont pas autorisés sur les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="9e256-114">Access modifiers are not allowed on namespaces.</span></span> <span data-ttu-id="9e256-115">Les espaces de noms ne présentent aucune limitation d’accès.</span><span class="sxs-lookup"><span data-stu-id="9e256-115">Namespaces have no access restrictions.</span></span>  
  
 <span data-ttu-id="9e256-116">Selon le contexte dans lequel une déclaration de membre est effectuée, seules certaines accessibilités déclarées sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="9e256-116">Depending on the context in which a member declaration occurs, only certain declared accessibilities are permitted.</span></span> <span data-ttu-id="9e256-117">Si aucun modificateur d’accès n’est spécifié dans une déclaration de membre, une accessibilité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9e256-117">If no access modifier is specified in a member declaration, a default accessibility is used.</span></span>  
  
 <span data-ttu-id="9e256-118">Les types de premier niveau, qui ne sont pas imbriqués dans d’autres types, peuvent uniquement avoir une accessibilité `internal` ou `public`.</span><span class="sxs-lookup"><span data-stu-id="9e256-118">Top-level types, which are not nested in other types, can only have `internal` or `public` accessibility.</span></span> <span data-ttu-id="9e256-119">L’accessibilité par défaut de ces types est `internal`.</span><span class="sxs-lookup"><span data-stu-id="9e256-119">The default accessibility for these types is `internal`.</span></span>  
  
 <span data-ttu-id="9e256-120">Les types imbriqués, qui sont membres d’autres types, peuvent avoir les accessibilités déclarées indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9e256-120">Nested types, which are members of other types, can have declared accessibilities as indicated in the following table.</span></span>  
  
|<span data-ttu-id="9e256-121">Membres de</span><span class="sxs-lookup"><span data-stu-id="9e256-121">Members of</span></span>|<span data-ttu-id="9e256-122">Accessibilité par défaut du membre</span><span class="sxs-lookup"><span data-stu-id="9e256-122">Default member accessibility</span></span>|<span data-ttu-id="9e256-123">Accessibilité déclarée du membre autorisée</span><span class="sxs-lookup"><span data-stu-id="9e256-123">Allowed declared accessibility of the member</span></span>|  
|----------------|----------------------------------|--------------------------------------------------|  
|`enum`|`public`|<span data-ttu-id="9e256-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9e256-124">None</span></span>|  
|`class`|`private`|`public`<br /><br /> `protected`<br /><br /> `internal`<br /><br /> `private`<br /><br /> `protected internal` <br /><br />`private protected`|  
|`interface`|`public`|<span data-ttu-id="9e256-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9e256-125">None</span></span>|  
|`struct`|`private`|`public`<br /><br /> `internal`<br /><br /> `private`|  
  
 <span data-ttu-id="9e256-126">L’accessibilité d’un type imbriqué dépend de son [domaine d’accessibilité](../../../csharp/language-reference/keywords/accessibility-domain.md), qui est déterminé à la fois par l’accessibilité déclarée du membre et par le domaine d’accessibilité du type conteneur immédiat.</span><span class="sxs-lookup"><span data-stu-id="9e256-126">The accessibility of a nested type depends on its [accessibility domain](../../../csharp/language-reference/keywords/accessibility-domain.md), which is determined by both the declared accessibility of the member and the accessibility domain of the immediately containing type.</span></span> <span data-ttu-id="9e256-127">Toutefois, le domaine d'accessibilité d'un type imbriqué ne peut pas dépasser celui du type conteneur.</span><span class="sxs-lookup"><span data-stu-id="9e256-127">However, the accessibility domain of a nested type cannot exceed that of the containing type.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="9e256-128">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9e256-128">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9e256-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e256-129">See Also</span></span>  
- [<span data-ttu-id="9e256-130">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9e256-130">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="9e256-131">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9e256-131">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9e256-132">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="9e256-132">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="9e256-133">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="9e256-133">Access Modifiers</span></span>](../../../csharp/language-reference/keywords/access-modifiers.md)  
- [<span data-ttu-id="9e256-134">Domaine d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="9e256-134">Accessibility Domain</span></span>](../../../csharp/language-reference/keywords/accessibility-domain.md)  
- [<span data-ttu-id="9e256-135">Limitations sur l’utilisation des niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="9e256-135">Restrictions on Using Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md)  
- [<span data-ttu-id="9e256-136">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="9e256-136">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
- [<span data-ttu-id="9e256-137">public</span><span class="sxs-lookup"><span data-stu-id="9e256-137">public</span></span>](../../../csharp/language-reference/keywords/public.md)  
- [<span data-ttu-id="9e256-138">private</span><span class="sxs-lookup"><span data-stu-id="9e256-138">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
- [<span data-ttu-id="9e256-139">protected</span><span class="sxs-lookup"><span data-stu-id="9e256-139">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)  
- [<span data-ttu-id="9e256-140">internal</span><span class="sxs-lookup"><span data-stu-id="9e256-140">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)
