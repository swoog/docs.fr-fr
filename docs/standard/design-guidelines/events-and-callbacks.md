---
title: Événements et rappels
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 90cc40024de627f151a4d0df879a65e5900004b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33573631"
---
# <a name="events-and-callbacks"></a><span data-ttu-id="dd0fe-102">Événements et rappels</span><span class="sxs-lookup"><span data-stu-id="dd0fe-102">Events and Callbacks</span></span>
<span data-ttu-id="dd0fe-103">Les rappels sont des points d’extensibilité qui autorisent une infrastructure rappeler dans le code de l’utilisateur via un délégué.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-103">Callbacks are extensibility points that allow a framework to call back into user code through a delegate.</span></span> <span data-ttu-id="dd0fe-104">Ces délégués sont généralement transmis à l’infrastructure via un paramètre d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-104">These delegates are usually passed to the framework through a parameter of a method.</span></span>  
  
 <span data-ttu-id="dd0fe-105">Les événements sont un cas spécial de rappels qui prend en charge la syntaxe pratique et cohérente pour fournir le délégué (un gestionnaire d’événements).</span><span class="sxs-lookup"><span data-stu-id="dd0fe-105">Events are a special case of callbacks that supports convenient and consistent syntax for supplying the delegate (an event handler).</span></span> <span data-ttu-id="dd0fe-106">En outre, saisie semi-automatique des instructions et les concepteurs de Visual Studio fournissent de l’aide à l’aide d’API basées sur des événements.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-106">In addition, Visual Studio’s statement completion and designers provide help in using event-based APIs.</span></span> <span data-ttu-id="dd0fe-107">(Consultez [événement conception](../../../docs/standard/design-guidelines/event.md).)</span><span class="sxs-lookup"><span data-stu-id="dd0fe-107">(See [Event Design](../../../docs/standard/design-guidelines/event.md).)</span></span>  
  
 <span data-ttu-id="dd0fe-108">**✓ CONSIDER** à l’aide des rappels pour permettre aux utilisateurs de fournir un code personnalisé doit être exécuté par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-108">**✓ CONSIDER** using callbacks to allow users to provide custom code to be executed by the framework.</span></span>  
  
 <span data-ttu-id="dd0fe-109">**✓ CONSIDER** à l’aide d’événements pour permettre aux utilisateurs de personnaliser le comportement d’une infrastructure sans avoir besoin pour comprendre la conception orientée objet.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-109">**✓ CONSIDER** using events to allow users to customize the behavior of a framework without the need for understanding object-oriented design.</span></span>  
  
 <span data-ttu-id="dd0fe-110">**✓ DO** de préférence des événements via des rappels ordinaires, car ils sont plus facile pour un grand nombre de développeurs et sont intégrés à la fin de l’instruction Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-110">**✓ DO** prefer events over plain callbacks, because they are more familiar to a broader range of developers and are integrated with Visual Studio statement completion.</span></span>  
  
 <span data-ttu-id="dd0fe-111">**X AVOID** à l’aide de rappels dans les API sensibles aux performances.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-111">**X AVOID** using callbacks in performance-sensitive APIs.</span></span>  
  
 <span data-ttu-id="dd0fe-112">**✓ DO** utiliser la nouvelle `Func<...>`, `Action<...>`, ou `Expression<...>` types à la place des délégués personnalisés lors de la définition d’API avec des rappels.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-112">**✓ DO** use the new `Func<...>`, `Action<...>`, or `Expression<...>` types instead of custom delegates, when defining APIs with callbacks.</span></span>  
  
 <span data-ttu-id="dd0fe-113">`Func<...>` et `Action<...>` représentent des délégués génériques.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-113">`Func<...>` and `Action<...>` represent generic delegates.</span></span> <span data-ttu-id="dd0fe-114">`Expression<...>` représente les définitions de fonction qui peuvent être compilées et appelées par la suite lors de l’exécution, mais peut également être sérialisées et passées à des processus à distance.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-114">`Expression<...>` represents function definitions that can be compiled and subsequently invoked at runtime but can also be serialized and passed to remote processes.</span></span>  
  
 <span data-ttu-id="dd0fe-115">**✓ DO** mesurer et comprendre les implications en matière de performances de l’utilisation de `Expression<...>`, au lieu d’utiliser `Func<...>` et `Action<...>` délégués.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-115">**✓ DO** measure and understand performance implications of using `Expression<...>`, instead of using `Func<...>` and `Action<...>` delegates.</span></span>  
  
 <span data-ttu-id="dd0fe-116">`Expression<...>` les types sont dans la plupart des cas logiquement équivalente à `Func<...>` et `Action<...>` délégués.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-116">`Expression<...>` types are in most cases logically equivalent to `Func<...>` and `Action<...>` delegates.</span></span> <span data-ttu-id="dd0fe-117">La principale différence est que les délégués sont destinées à être utilisée dans des scénarios de processus locale. les expressions sont destinées aux cas où il est bénéfique et permet d’évaluer l’expression dans un processus distant ou un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-117">The main difference between them is that the delegates are intended to be used in local process scenarios; expressions are intended for cases where it’s beneficial and possible to evaluate the expression in a remote process or machine.</span></span>  
  
 <span data-ttu-id="dd0fe-118">**✓ DO** comprendre que par l’appel d’un délégué, vous exécutez du code arbitraire et qui pourraient avoir des répercussions de sécurité, d’exactitude et de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="dd0fe-118">**✓ DO** understand that by calling a delegate, you are executing arbitrary code and that could have security, correctness, and compatibility repercussions.</span></span>  
  
 <span data-ttu-id="dd0fe-119">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="dd0fe-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="dd0fe-120">*Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="dd0fe-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd0fe-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd0fe-121">See Also</span></span>  
 [<span data-ttu-id="dd0fe-122">Conception en vue de l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="dd0fe-122">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
 [<span data-ttu-id="dd0fe-123">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="dd0fe-123">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
