---
title: Modificateurs d’accès (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- access modifiers [C#]
ms.assetid: 61c3fa51-c00f-48cb-9b49-c805dedd62d7
ms.openlocfilehash: ff313df9683dbc76bab684ff484b746ad05e065a
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935559"
---
# <a name="access-modifiers-c-reference"></a><span data-ttu-id="8c046-102">Modificateurs d’accès (référence C#)</span><span class="sxs-lookup"><span data-stu-id="8c046-102">Access Modifiers (C# Reference)</span></span>
<span data-ttu-id="8c046-103">Les modificateurs d’accès sont des mots clés utilisés pour spécifier l’accessibilité déclarée d’un membre ou d’un type.</span><span class="sxs-lookup"><span data-stu-id="8c046-103">Access modifiers are keywords used to specify the declared accessibility of a member or a type.</span></span> <span data-ttu-id="8c046-104">Cette section présente les quatre modificateurs d’accès :</span><span class="sxs-lookup"><span data-stu-id="8c046-104">This section introduces the four access modifiers:</span></span>  
  
-   `public`
-   `protected`
-   `internal`
-   `private`
  
 <span data-ttu-id="8c046-105">Les modificateurs d’accès permettent de spécifier les six niveaux d’accessibilité suivants :</span><span class="sxs-lookup"><span data-stu-id="8c046-105">The following six accessibility levels can be specified using the access modifiers:</span></span>  
  
- <span data-ttu-id="8c046-106">[`public`](public.md) : l’accès n’est pas limité.</span><span class="sxs-lookup"><span data-stu-id="8c046-106">[`public`](public.md): Access is not restricted.</span></span>  
  
- <span data-ttu-id="8c046-107">[`protected`](protected.md) : l’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="8c046-107">[`protected`](protected.md): Access is limited to the containing class or types derived from the containing class.</span></span>  
  
- <span data-ttu-id="8c046-108">[`internal`](internal.md) : l’accès est limité à l’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="8c046-108">[`internal`](internal.md): Access is limited to the current assembly.</span></span>  
  
- <span data-ttu-id="8c046-109">[`protected internal`](protected-internal.md) : l’accès est limité à l’assembly actuel ou aux types dérivés de la classe conteneur.</span><span class="sxs-lookup"><span data-stu-id="8c046-109">[`protected internal`](protected-internal.md): Access is limited to the current assembly or types derived from the containing class.</span></span>  
  
- <span data-ttu-id="8c046-110">[`private`](private.md) : l’accès est limité au type conteneur.</span><span class="sxs-lookup"><span data-stu-id="8c046-110">[`private`](private.md): Access is limited to the containing type.</span></span>  

- <span data-ttu-id="8c046-111">[`private protected`](private-protected.md) : l’accès est limité à la classe conteneur ou aux types dérivés de la classe conteneur dans l’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="8c046-111">[`private protected`](private-protected.md): Access is limited to the containing class or types derived from the containing class within the current assembly.</span></span>  
  
 <span data-ttu-id="8c046-112">Cette section introduit également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8c046-112">This section also introduces the following:</span></span>  
  
-   <span data-ttu-id="8c046-113">[Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md) : utilisation des quatre modificateurs d’accès pour déclarer six niveaux d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="8c046-113">[Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md): Using the four access modifiers to declare six levels of accessibility.</span></span>  
  
-   <span data-ttu-id="8c046-114">[Domaine d’accessibilité](../../../csharp/language-reference/keywords/accessibility-domain.md) : spécifie où, dans les sections du programme, un membre peut être référencé.</span><span class="sxs-lookup"><span data-stu-id="8c046-114">[Accessibility Domain](../../../csharp/language-reference/keywords/accessibility-domain.md): Specifies where, in the program sections, a member can be referenced.</span></span>  
  
-   <span data-ttu-id="8c046-115">[Limitations sur l’utilisation des niveaux d’accessibilité](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md) : résumé des restrictions sur l’utilisation des niveaux d’accessibilité déclarés.</span><span class="sxs-lookup"><span data-stu-id="8c046-115">[Restrictions on Using Accessibility Levels](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md): A summary of the restrictions on using declared accessibility levels.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c046-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c046-116">See Also</span></span>  
- [<span data-ttu-id="8c046-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="8c046-117">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="8c046-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8c046-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="8c046-119">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="8c046-119">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="8c046-120">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="8c046-120">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
- [<span data-ttu-id="8c046-121">Mots clés d’accès</span><span class="sxs-lookup"><span data-stu-id="8c046-121">Access Keywords</span></span>](../../../csharp/language-reference/keywords/access-keywords.md)  
- [<span data-ttu-id="8c046-122">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="8c046-122">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)
