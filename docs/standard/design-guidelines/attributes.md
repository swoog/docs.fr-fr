---
title: Attributes1
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- attributes [.NET Framework], about
- class library design guidelines [.NET Framework], attributes
ms.assetid: ee0038ef-b247-4747-a650-3c5c5cd58d8b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51aa91b1acbae9f1a15ac12441090dd4c1c2dcb1
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43869141"
---
# <a name="attributes"></a><span data-ttu-id="e27a8-102">Attributs</span><span class="sxs-lookup"><span data-stu-id="e27a8-102">Attributes</span></span>
<span data-ttu-id="e27a8-103"><xref:System.Attribute?displayProperty=nameWithType> une classe de base permet de définir des attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e27a8-103"><xref:System.Attribute?displayProperty=nameWithType> is a base class used to define custom attributes.</span></span>  
  
 <span data-ttu-id="e27a8-104">Les attributs sont des annotations qui peuvent être ajoutées aux éléments de programmation tels que les assemblys, types, membres et paramètres.</span><span class="sxs-lookup"><span data-stu-id="e27a8-104">Attributes are annotations that can be added to programming elements such as assemblies, types, members, and parameters.</span></span> <span data-ttu-id="e27a8-105">Ils sont stockés dans les métadonnées de l’assembly et sont accessibles lors de l’exécution à l’aide de l’API de réflexion.</span><span class="sxs-lookup"><span data-stu-id="e27a8-105">They are stored in the metadata of the assembly and can be accessed at runtime using the reflection APIs.</span></span> <span data-ttu-id="e27a8-106">Par exemple, le Framework définit le <xref:System.ObsoleteAttribute>, qui peut être appliqué à un type ou un membre pour indiquer que le type ou membre a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e27a8-106">For example, the Framework defines the <xref:System.ObsoleteAttribute>, which can be applied to a type or a member to indicate that the type or member has been deprecated.</span></span>  
  
 <span data-ttu-id="e27a8-107">Attributs peuvent avoir une ou plusieurs propriétés qui transmettent des données supplémentaires relatives à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e27a8-107">Attributes can have one or more properties that carry additional data related to the attribute.</span></span> <span data-ttu-id="e27a8-108">Par exemple, `ObsoleteAttribute` peut comporter des informations complémentaires sur la version dans lequel un type ou un membre a été déconseillé et la description des nouvelles API en remplaçant l’API obsolète.</span><span class="sxs-lookup"><span data-stu-id="e27a8-108">For example, `ObsoleteAttribute` could carry additional information about the release in which a type or a member got deprecated and the description of the new APIs replacing the obsolete API.</span></span>  
  
 <span data-ttu-id="e27a8-109">Certaines propriétés d’un attribut doivent être spécifiées lorsque l’attribut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="e27a8-109">Some properties of an attribute must be specified when the attribute is applied.</span></span> <span data-ttu-id="e27a8-110">Ceux-ci sont appelés les propriétés requises ou les arguments requis, car ils sont représentés en tant que paramètres de constructeur positionnel.</span><span class="sxs-lookup"><span data-stu-id="e27a8-110">These are referred to as the required properties or required arguments, because they are represented as positional constructor parameters.</span></span> <span data-ttu-id="e27a8-111">Par exemple, le <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> propriété de la <xref:System.Diagnostics.ConditionalAttribute> est une propriété obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e27a8-111">For example, the <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> property of the <xref:System.Diagnostics.ConditionalAttribute> is a required property.</span></span>  
  
 <span data-ttu-id="e27a8-112">Les propriétés qui n’ont pas nécessairement être spécifié lorsque l’attribut est appliqué sont appelées propriétés facultatives (ou les arguments facultatifs).</span><span class="sxs-lookup"><span data-stu-id="e27a8-112">Properties that do not necessarily have to be specified when the attribute is applied are called optional properties (or optional arguments).</span></span> <span data-ttu-id="e27a8-113">Ils sont représentés par les propriétés définissables.</span><span class="sxs-lookup"><span data-stu-id="e27a8-113">They are represented by settable properties.</span></span> <span data-ttu-id="e27a8-114">Les compilateurs fournissent une syntaxe spéciale pour définir ces propriétés lorsqu’un attribut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="e27a8-114">Compilers provide special syntax to set these properties when an attribute is applied.</span></span> <span data-ttu-id="e27a8-115">Par exemple, le <xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> propriété représente un argument facultatif.</span><span class="sxs-lookup"><span data-stu-id="e27a8-115">For example, the <xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> property represents an optional argument.</span></span>  
  
 <span data-ttu-id="e27a8-116">**✓ DO** nommez des classes d’attributs personnalisés avec le suffixe « Attribut ».</span><span class="sxs-lookup"><span data-stu-id="e27a8-116">**✓ DO** name custom attribute classes with the suffix "Attribute."</span></span>  
  
 <span data-ttu-id="e27a8-117">**✓ DO** appliquer le <xref:System.AttributeUsageAttribute> à des attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e27a8-117">**✓ DO** apply the <xref:System.AttributeUsageAttribute> to custom attributes.</span></span>  
  
 <span data-ttu-id="e27a8-118">**✓ DO** fournir les propriétés définissables pour les arguments facultatifs.</span><span class="sxs-lookup"><span data-stu-id="e27a8-118">**✓ DO** provide settable properties for optional arguments.</span></span>  
  
 <span data-ttu-id="e27a8-119">**✓ DO** fournissent des propriétés get uniquement pour les arguments requis.</span><span class="sxs-lookup"><span data-stu-id="e27a8-119">**✓ DO** provide get-only properties for required arguments.</span></span>  
  
 <span data-ttu-id="e27a8-120">**✓ DO** fournissent des paramètres du constructeur pour initialiser les propriétés qui correspondent aux arguments requis.</span><span class="sxs-lookup"><span data-stu-id="e27a8-120">**✓ DO** provide constructor parameters to initialize properties corresponding to required arguments.</span></span> <span data-ttu-id="e27a8-121">Chaque paramètre doit avoir le même nom (mais avec une casse différente) en tant que la propriété correspondante.</span><span class="sxs-lookup"><span data-stu-id="e27a8-121">Each parameter should have the same name (although with different casing) as the corresponding property.</span></span>  
  
 <span data-ttu-id="e27a8-122">**X AVOID** fournissant les paramètres du constructeur pour initialiser les propriétés qui correspondent aux arguments facultatifs.</span><span class="sxs-lookup"><span data-stu-id="e27a8-122">**X AVOID** providing constructor parameters to initialize properties corresponding to the optional arguments.</span></span>  
  
 <span data-ttu-id="e27a8-123">En d’autres termes, n’ont pas de propriétés qui peuvent être définies avec un constructeur et un accesseur Set.</span><span class="sxs-lookup"><span data-stu-id="e27a8-123">In other words, do not have properties that can be set with both a constructor and a setter.</span></span> <span data-ttu-id="e27a8-124">Cette recommandation rend très explicite les arguments sont facultatifs et qui sont nécessaire et évite d’avoir deux façons de faire la même chose.</span><span class="sxs-lookup"><span data-stu-id="e27a8-124">This guideline makes very explicit which arguments are optional and which are required, and avoids having two ways of doing the same thing.</span></span>  
  
 <span data-ttu-id="e27a8-125">**X AVOID** surcharge des constructeurs d’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e27a8-125">**X AVOID** overloading custom attribute constructors.</span></span>  
  
 <span data-ttu-id="e27a8-126">Avoir un seul constructeur communique clairement à l’utilisateur quels sont les arguments requis et facultatifs.</span><span class="sxs-lookup"><span data-stu-id="e27a8-126">Having only one constructor clearly communicates to the user which arguments are required and which are optional.</span></span>  
  
 <span data-ttu-id="e27a8-127">**✓ DO** sceller des classes d’attributs personnalisés, si possible.</span><span class="sxs-lookup"><span data-stu-id="e27a8-127">**✓ DO** seal custom attribute classes, if possible.</span></span> <span data-ttu-id="e27a8-128">Cela accélère la recherche de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e27a8-128">This makes the look-up for the attribute faster.</span></span>  
  
 <span data-ttu-id="e27a8-129">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="e27a8-129">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="e27a8-130">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="e27a8-130">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e27a8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e27a8-131">See also</span></span>

- [<span data-ttu-id="e27a8-132">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e27a8-132">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="e27a8-133">Indications relatives à l’utilisation</span><span class="sxs-lookup"><span data-stu-id="e27a8-133">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)
