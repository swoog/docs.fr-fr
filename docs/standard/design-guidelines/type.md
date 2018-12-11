---
title: Instructions de conception de types
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
author: KrzysztofCwalina
ms.openlocfilehash: 16f2a095f461a406eedbd2b34b0c91d3ac43bbe5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53145226"
---
# <a name="type-design-guidelines"></a><span data-ttu-id="de2a3-102">Instructions de conception de types</span><span class="sxs-lookup"><span data-stu-id="de2a3-102">Type Design Guidelines</span></span>
<span data-ttu-id="de2a3-103">À partir de la perspective du CLR, il existe uniquement deux catégories de types : types référence et les types valeur, mais à des fins une discussion sur la conception d’infrastructure, nous divisons types en groupes logiques de plus, chacun avec ses propres règles de conception spécifiques.</span><span class="sxs-lookup"><span data-stu-id="de2a3-103">From the CLR perspective, there are only two categories of types—reference types and value types—but for the purpose of a discussion about framework design, we divide types into more logical groups, each with its own specific design rules.</span></span>  
  
 <span data-ttu-id="de2a3-104">Les classes sont des types référence générale.</span><span class="sxs-lookup"><span data-stu-id="de2a3-104">Classes are the general case of reference types.</span></span> <span data-ttu-id="de2a3-105">Ils constituent la majeure partie des types dans la plupart des infrastructures.</span><span class="sxs-lookup"><span data-stu-id="de2a3-105">They make up the bulk of types in the majority of frameworks.</span></span> <span data-ttu-id="de2a3-106">Classes à régler leur popularité pour la riche ensemble de fonctionnalités orientées objet, qu'ils prennent en charge et leur applicabilité générale.</span><span class="sxs-lookup"><span data-stu-id="de2a3-106">Classes owe their popularity to the rich set of object-oriented features they support and to their general applicability.</span></span> <span data-ttu-id="de2a3-107">Classes de base et des classes abstraites sont des groupes logiques spéciales relatives à l’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="de2a3-107">Base classes and abstract classes are special logical groups related to extensibility.</span></span>  
  
 <span data-ttu-id="de2a3-108">Les interfaces sont des types qui peuvent être implémentées par les types référence et les types valeur.</span><span class="sxs-lookup"><span data-stu-id="de2a3-108">Interfaces are types that can be implemented by both reference types and value types.</span></span> <span data-ttu-id="de2a3-109">Elles peuvent donc servir racines des hiérarchies polymorphes des types référence et les types valeur.</span><span class="sxs-lookup"><span data-stu-id="de2a3-109">They can thus serve as roots of polymorphic hierarchies of reference types and value types.</span></span> <span data-ttu-id="de2a3-110">En outre, les interfaces peuvent être utilisées pour simuler l’héritage multiple, ce qui n’est pas pris en charge en mode natif par le CLR.</span><span class="sxs-lookup"><span data-stu-id="de2a3-110">In addition, interfaces can be used to simulate multiple inheritance, which is not natively supported by the CLR.</span></span>  
  
 <span data-ttu-id="de2a3-111">Les structs sont générale des types valeur et doit être réservés pour les types simples, similaires aux primitives de langage.</span><span class="sxs-lookup"><span data-stu-id="de2a3-111">Structs are the general case of value types and should be reserved for small, simple types, similar to language primitives.</span></span>  
  
 <span data-ttu-id="de2a3-112">Les enums sont un cas spécial de types valeur utilisés pour définir des ensembles courts de valeurs, telles que les jours de la semaine, les couleurs de console et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="de2a3-112">Enums are a special case of value types used to define short sets of values, such as days of the week, console colors, and so on.</span></span>  
  
 <span data-ttu-id="de2a3-113">Les classes statiques sont destinées à être des conteneurs pour les membres statiques de types.</span><span class="sxs-lookup"><span data-stu-id="de2a3-113">Static classes are types intended to be containers for static members.</span></span> <span data-ttu-id="de2a3-114">Ils sont souvent utilisés pour fournir des raccourcis vers les autres opérations.</span><span class="sxs-lookup"><span data-stu-id="de2a3-114">They are commonly used to provide shortcuts to other operations.</span></span>  
  
 <span data-ttu-id="de2a3-115">Délégués, les exceptions, les attributs, les tableaux et les collections sont tous les cas spéciaux de types de référence destinées à des utilisations spécifiques, et les instructions pour leur conception et leur utilisation sont étudiées ailleurs dans ce livre.</span><span class="sxs-lookup"><span data-stu-id="de2a3-115">Delegates, exceptions, attributes, arrays, and collections are all special cases of reference types intended for specific uses, and guidelines for their design and usage are discussed elsewhere in this book.</span></span>  
  
 <span data-ttu-id="de2a3-116">**✓ DO** Vérifiez que chaque type est un ensemble bien défini de membres associés, pas seulement une collection aléatoire des fonctionnalités non liées.</span><span class="sxs-lookup"><span data-stu-id="de2a3-116">**✓ DO** ensure that each type is a well-defined set of related members, not just a random collection of unrelated functionality.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="de2a3-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="de2a3-117">In This Section</span></span>  
 [<span data-ttu-id="de2a3-118">Choix entre classe et structure</span><span class="sxs-lookup"><span data-stu-id="de2a3-118">Choosing Between Class and Struct</span></span>](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)  
 [<span data-ttu-id="de2a3-119">Conception de classes abstraites</span><span class="sxs-lookup"><span data-stu-id="de2a3-119">Abstract Class Design</span></span>](../../../docs/standard/design-guidelines/abstract-class.md)  
 [<span data-ttu-id="de2a3-120">Conception de classes statiques</span><span class="sxs-lookup"><span data-stu-id="de2a3-120">Static Class Design</span></span>](../../../docs/standard/design-guidelines/static-class.md)  
 [<span data-ttu-id="de2a3-121">Conception d’interfaces</span><span class="sxs-lookup"><span data-stu-id="de2a3-121">Interface Design</span></span>](../../../docs/standard/design-guidelines/interface.md)  
 [<span data-ttu-id="de2a3-122">Conception de structures</span><span class="sxs-lookup"><span data-stu-id="de2a3-122">Struct Design</span></span>](../../../docs/standard/design-guidelines/struct.md)  
 [<span data-ttu-id="de2a3-123">Conception d’énumérations</span><span class="sxs-lookup"><span data-stu-id="de2a3-123">Enum Design</span></span>](../../../docs/standard/design-guidelines/enum.md)  
 [<span data-ttu-id="de2a3-124">Types imbriqués</span><span class="sxs-lookup"><span data-stu-id="de2a3-124">Nested Types</span></span>](../../../docs/standard/design-guidelines/nested-types.md)  
 <span data-ttu-id="de2a3-125">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="de2a3-125">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="de2a3-126">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="de2a3-126">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de2a3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de2a3-127">See also</span></span>

- [<span data-ttu-id="de2a3-128">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="de2a3-128">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
