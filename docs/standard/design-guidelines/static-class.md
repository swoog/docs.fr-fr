---
title: Conception de classes statiques
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c3a0a51fc6055190f9a0189de2e17d98f88036ea
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46518046"
---
# <a name="static-class-design"></a><span data-ttu-id="2e2ac-102">Conception de classes statiques</span><span class="sxs-lookup"><span data-stu-id="2e2ac-102">Static Class Design</span></span>
<span data-ttu-id="2e2ac-103">Une classe statique est définie comme une classe qui contient uniquement des membres statiques (bien entendu, outre les membres d’instance hérités de <xref:System.Object?displayProperty=nameWithType> et éventuellement un constructeur privé).</span><span class="sxs-lookup"><span data-stu-id="2e2ac-103">A static class is defined as a class that contains only static members (of course besides the instance members inherited from <xref:System.Object?displayProperty=nameWithType> and possibly a private constructor).</span></span> <span data-ttu-id="2e2ac-104">Certains langages fournissent la prise en charge intégrée pour les classes static.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-104">Some languages provide built-in support for static classes.</span></span> <span data-ttu-id="2e2ac-105">Dans c# 2.0 et versions ultérieures, quand une classe est déclarée comme statique, il est scellé, abstract, et aucun membre d’instance peut être remplacée ou déclaré.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-105">In C# 2.0 and later, when a class is declared to be static, it is sealed, abstract, and no instance members can be overridden or declared.</span></span>  
  
 <span data-ttu-id="2e2ac-106">Les classes statiques sont un compromis entre la conception orientée objet et la simplicité.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-106">Static classes are a compromise between pure object-oriented design and simplicity.</span></span> <span data-ttu-id="2e2ac-107">Ils sont couramment utilisés pour fournir des raccourcis vers les autres opérations (telles que <xref:System.IO.File?displayProperty=nameWithType>), les détenteurs de méthodes d’extension ou de fonctionnalités pour lequel un wrapper orienté objet est injustifié (tel que <xref:System.Environment?displayProperty=nameWithType>).</span><span class="sxs-lookup"><span data-stu-id="2e2ac-107">They are commonly used to provide shortcuts to other operations (such as <xref:System.IO.File?displayProperty=nameWithType>), holders of extension methods, or functionality for which a full object-oriented wrapper is unwarranted (such as <xref:System.Environment?displayProperty=nameWithType>).</span></span>  
  
 <span data-ttu-id="2e2ac-108">**✓ DO** utilisent des classes statiques avec parcimonie.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-108">**✓ DO** use static classes sparingly.</span></span>  
  
 <span data-ttu-id="2e2ac-109">Classes static doivent être utilisées uniquement comme prenant en charge de classes pour la core orientée objet du framework.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-109">Static classes should be used only as supporting classes for the object-oriented core of the framework.</span></span>  
  
 <span data-ttu-id="2e2ac-110">**X DO NOT** traiter des classes statiques comme un compartiment divers.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-110">**X DO NOT** treat static classes as a miscellaneous bucket.</span></span>  
  
 <span data-ttu-id="2e2ac-111">**X DO NOT** déclarer ou substituer des membres d’instance dans les classes static.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-111">**X DO NOT** declare or override instance members in static classes.</span></span>  
  
 <span data-ttu-id="2e2ac-112">**✓ DO** déclarer des classes statiques comme sealed, abstract, et ajoutez un constructeur d’instance privée si votre langage de programmation ne dispose pas de prise en charge intégrée pour les classes static.</span><span class="sxs-lookup"><span data-stu-id="2e2ac-112">**✓ DO** declare static classes as sealed, abstract, and add a private instance constructor if your programming language does not have built-in support for static classes.</span></span>  
  
 <span data-ttu-id="2e2ac-113">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="2e2ac-113">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="2e2ac-114">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="2e2ac-114">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e2ac-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2ac-115">See also</span></span>

- [<span data-ttu-id="2e2ac-116">Instructions pour la conception des types</span><span class="sxs-lookup"><span data-stu-id="2e2ac-116">Type Design Guidelines</span></span>](../../../docs/standard/design-guidelines/type.md)  
- [<span data-ttu-id="2e2ac-117">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2e2ac-117">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
