---
title: Modificateurs d’accès - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- access modifiers [C#]
ms.assetid: 61c3fa51-c00f-48cb-9b49-c805dedd62d7
ms.openlocfilehash: 0fb435a35b928cb78511d8969f1dfce9f94869eb
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53242020"
---
# <a name="access-modifiers-c-reference"></a><span data-ttu-id="f2d03-102">Modificateurs d’accès (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f2d03-102">Access Modifiers (C# Reference)</span></span>
<span data-ttu-id="f2d03-103">Les modificateurs d’accès sont des mots clés utilisés pour spécifier l’accessibilité déclarée d’un membre ou d’un type.</span><span class="sxs-lookup"><span data-stu-id="f2d03-103">Access modifiers are keywords used to specify the declared accessibility of a member or a type.</span></span> <span data-ttu-id="f2d03-104">Cette section présente les quatre modificateurs d’accès :</span><span class="sxs-lookup"><span data-stu-id="f2d03-104">This section introduces the four access modifiers:</span></span>  
  
-   `public`
-   `protected`
-   `internal`
-   `private`
  
 <span data-ttu-id="f2d03-105">Les modificateurs d’accès permettent de spécifier les six niveaux d’accessibilité suivants :</span><span class="sxs-lookup"><span data-stu-id="f2d03-105">The following six accessibility levels can be specified using the access modifiers:</span></span>  
  
- <span data-ttu-id="f2d03-106">[`public`](public.md) : L’accès n’est pas limité.</span><span class="sxs-lookup"><span data-stu-id="f2d03-106">[`public`](public.md): Access is not restricted.</span></span>  
  
- <span data-ttu-id="f2d03-107">[`protected`](protected.md) : L’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="f2d03-107">[`protected`](protected.md): Access is limited to the containing class or types derived from the containing class.</span></span>  
  
- <span data-ttu-id="f2d03-108">[`internal`](internal.md) : L’accès est limité à l’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="f2d03-108">[`internal`](internal.md): Access is limited to the current assembly.</span></span>  
  
- <span data-ttu-id="f2d03-109">[`protected internal`](protected-internal.md) : L’accès est limité à l’assembly actuel ou aux types dérivés de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="f2d03-109">[`protected internal`](protected-internal.md): Access is limited to the current assembly or types derived from the containing class.</span></span>  
  
- <span data-ttu-id="f2d03-110">[`private`](private.md) : L’accès est limité au type conteneur.</span><span class="sxs-lookup"><span data-stu-id="f2d03-110">[`private`](private.md): Access is limited to the containing type.</span></span>  

- <span data-ttu-id="f2d03-111">[`private protected`](private-protected.md) : L’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur dans l’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="f2d03-111">[`private protected`](private-protected.md): Access is limited to the containing class or types derived from the containing class within the current assembly.</span></span>  
  
 <span data-ttu-id="f2d03-112">Cette section introduit également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f2d03-112">This section also introduces the following:</span></span>  
  
-   <span data-ttu-id="f2d03-113">[Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md) : utilisation des quatre modificateurs d’accès pour déclarer six niveaux d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="f2d03-113">[Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md): Using the four access modifiers to declare six levels of accessibility.</span></span>  
  
-   <span data-ttu-id="f2d03-114">[Domaine d’accessibilité](../../../csharp/language-reference/keywords/accessibility-domain.md) : spécifie où, dans les sections du programme, un membre peut être référencé.</span><span class="sxs-lookup"><span data-stu-id="f2d03-114">[Accessibility Domain](../../../csharp/language-reference/keywords/accessibility-domain.md): Specifies where, in the program sections, a member can be referenced.</span></span>  
  
-   <span data-ttu-id="f2d03-115">[Limitations sur l’utilisation des niveaux d’accessibilité](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md) : résumé des restrictions sur l’utilisation des niveaux d’accessibilité déclarés.</span><span class="sxs-lookup"><span data-stu-id="f2d03-115">[Restrictions on Using Accessibility Levels](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md): A summary of the restrictions on using declared accessibility levels.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2d03-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d03-116">See Also</span></span>  
- [<span data-ttu-id="f2d03-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f2d03-117">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="f2d03-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f2d03-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f2d03-119">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="f2d03-119">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="f2d03-120">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="f2d03-120">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
- [<span data-ttu-id="f2d03-121">Mots clés d’accès</span><span class="sxs-lookup"><span data-stu-id="f2d03-121">Access Keywords</span></span>](../../../csharp/language-reference/keywords/access-keywords.md)  
- [<span data-ttu-id="f2d03-122">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="f2d03-122">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)
