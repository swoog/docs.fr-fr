---
title: Conception d'interfaces
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- interfaces [.NET Framework], design guidelines
- type design guidelines, interfaces
- class library design guidelines [.NET Framework], interfaces
ms.assetid: a016bd18-6710-4358-9438-9f190a295392
author: KrzysztofCwalina
ms.openlocfilehash: a017b34ab410824e3ddac4365e5711840fb50031
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148728"
---
# <a name="interface-design"></a><span data-ttu-id="230f5-102">Conception d'interfaces</span><span class="sxs-lookup"><span data-stu-id="230f5-102">Interface Design</span></span>
<span data-ttu-id="230f5-103">Bien que la plupart des API sont mieux modélisées au moyen des classes et structs, il existe des cas dans lequel les interfaces sont plus appropriées ou sont la seule option.</span><span class="sxs-lookup"><span data-stu-id="230f5-103">Although most APIs are best modeled using classes and structs, there are cases in which interfaces are more appropriate or are the only option.</span></span>  
  
 <span data-ttu-id="230f5-104">Le CLR ne prend pas en charge l’héritage multiple (par exemple, les classes CLR ne peut pas hériter plusieurs classes de base), mais il n’autorise pas les types d’implémenter une ou plusieurs interfaces en plus de l’héritage d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="230f5-104">The CLR does not support multiple inheritance (i.e., CLR classes cannot inherit from more than one base class), but it does allow types to implement one or more interfaces in addition to inheriting from a base class.</span></span> <span data-ttu-id="230f5-105">Par conséquent, les interfaces sont souvent utilisées pour obtenir l’effet de l’héritage multiple.</span><span class="sxs-lookup"><span data-stu-id="230f5-105">Therefore, interfaces are often used to achieve the effect of multiple inheritance.</span></span> <span data-ttu-id="230f5-106">Par exemple, <xref:System.IDisposable> est une interface qui permet aux types prendre en charge disposability indépendant de toute autre hiérarchie d’héritage dans lequel ils souhaitent participer.</span><span class="sxs-lookup"><span data-stu-id="230f5-106">For example, <xref:System.IDisposable> is an interface that allows types to support disposability independent of any other inheritance hierarchy in which they want to participate.</span></span>  
  
 <span data-ttu-id="230f5-107">L’autre situation en les définissant une interface est appropriée est dans la création d’une interface commune pouvant être pris en charge par plusieurs types, y compris certains types de valeur.</span><span class="sxs-lookup"><span data-stu-id="230f5-107">The other situation in which defining an interface is appropriate is in creating a common interface that can be supported by several types, including some value types.</span></span> <span data-ttu-id="230f5-108">Types valeur ne peut pas hériter de types autres que <xref:System.ValueType>, mais ils peuvent implémenter des interfaces, par conséquent, à l’aide d’une interface est la seule option afin de fournir un type de base commun.</span><span class="sxs-lookup"><span data-stu-id="230f5-108">Value types cannot inherit from types other than <xref:System.ValueType>, but they can implement interfaces, so using an interface is the only option in order to provide a common base type.</span></span>  
  
 <span data-ttu-id="230f5-109">**✓ DO** définir une interface si vous avez besoin de certaines API courantes pour être pris en charge par un ensemble de types qui inclut les types de valeur.</span><span class="sxs-lookup"><span data-stu-id="230f5-109">**✓ DO** define an interface if you need some common API to be supported by a set of types that includes value types.</span></span>  
  
 <span data-ttu-id="230f5-110">**✓ CONSIDER** définissant une interface si vous avez besoin prendre en charge ses fonctionnalités sur les types qui héritent déjà d’un autre type.</span><span class="sxs-lookup"><span data-stu-id="230f5-110">**✓ CONSIDER** defining an interface if you need to support its functionality on types that already inherit from some other type.</span></span>  
  
 <span data-ttu-id="230f5-111">**X AVOID** à l’aide des interfaces de marqueur (interfaces sans membres).</span><span class="sxs-lookup"><span data-stu-id="230f5-111">**X AVOID** using marker interfaces (interfaces with no members).</span></span>  
  
 <span data-ttu-id="230f5-112">Si vous avez besoin marquer une classe comme ayant une caractéristique spécifique (marqueur), utilisez en général, un attribut personnalisé plutôt que d’une interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-112">If you need to mark a class as having a specific characteristic (marker), in general, use a custom attribute rather than an interface.</span></span>  
  
 <span data-ttu-id="230f5-113">**✓ DO** fournir au moins un type qui est une implémentation d’une interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-113">**✓ DO** provide at least one type that is an implementation of an interface.</span></span>  
  
 <span data-ttu-id="230f5-114">Ceci permet de valider la conception de l’interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-114">Doing this helps to validate the design of the interface.</span></span> <span data-ttu-id="230f5-115">Par exemple, <xref:System.Collections.Generic.List%601> est une implémentation de la <xref:System.Collections.Generic.IList%601> interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-115">For example, <xref:System.Collections.Generic.List%601> is an implementation of the <xref:System.Collections.Generic.IList%601> interface.</span></span>  
  
 <span data-ttu-id="230f5-116">**✓ DO** fournissent au moins une API qui consomme chaque interface que vous définissez (une méthode qui prend l’interface comme paramètre ou une propriété de type interface).</span><span class="sxs-lookup"><span data-stu-id="230f5-116">**✓ DO** provide at least one API that consumes each interface you define (a method taking the interface as a parameter or a property typed as the interface).</span></span>  
  
 <span data-ttu-id="230f5-117">Ceci permet de valider la conception de l’interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-117">Doing this helps to validate the interface design.</span></span> <span data-ttu-id="230f5-118">Par exemple, <xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> consomme la <xref:System.Collections.Generic.IComparer%601?displayProperty=nameWithType> interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-118">For example, <xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> consumes the <xref:System.Collections.Generic.IComparer%601?displayProperty=nameWithType> interface.</span></span>  
  
 <span data-ttu-id="230f5-119">**X DO NOT** ajouter des membres à une interface qui existait précédemment.</span><span class="sxs-lookup"><span data-stu-id="230f5-119">**X DO NOT** add members to an interface that has previously shipped.</span></span>  
  
 <span data-ttu-id="230f5-120">Cela compromettrait les implémentations de l’interface.</span><span class="sxs-lookup"><span data-stu-id="230f5-120">Doing so would break implementations of the interface.</span></span> <span data-ttu-id="230f5-121">Vous devez créer une nouvelle interface afin d’éviter les problèmes de versioning.</span><span class="sxs-lookup"><span data-stu-id="230f5-121">You should create a new interface in order to avoid versioning problems.</span></span>  
  
 <span data-ttu-id="230f5-122">À l’exception des situations décrites dans ces instructions, vous devez, en général, choisir les classes plutôt que des interfaces dans la conception de bibliothèques réutilisables de code managé.</span><span class="sxs-lookup"><span data-stu-id="230f5-122">Except for the situations described in these guidelines, you should, in general, choose classes rather than interfaces in designing managed code reusable libraries.</span></span>  
  
 <span data-ttu-id="230f5-123">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="230f5-123">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="230f5-124">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="230f5-124">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="230f5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="230f5-125">See also</span></span>

- [<span data-ttu-id="230f5-126">Instructions pour la conception des types</span><span class="sxs-lookup"><span data-stu-id="230f5-126">Type Design Guidelines</span></span>](../../../docs/standard/design-guidelines/type.md)  
- [<span data-ttu-id="230f5-127">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="230f5-127">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
