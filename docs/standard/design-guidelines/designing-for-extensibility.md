---
title: Conception en vue de l'extensibilité
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c1690d0cdf1f57eaf0a794d6e71babfa4fa6425
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44710899"
---
# <a name="designing-for-extensibility"></a><span data-ttu-id="ab849-102">Conception en vue de l'extensibilité</span><span class="sxs-lookup"><span data-stu-id="ab849-102">Designing for Extensibility</span></span>
<span data-ttu-id="ab849-103">Un aspect important de la conception d’une infrastructure consiste à s’assurer de que l’extensibilité de l’infrastructure a été examinée avec soin.</span><span class="sxs-lookup"><span data-stu-id="ab849-103">One important aspect of designing a framework is making sure the extensibility of the framework has been carefully considered.</span></span> <span data-ttu-id="ab849-104">Cela nécessite que vous comprenez les coûts et les avantages associés à différents mécanismes d’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="ab849-104">This requires that you understand the costs and benefits associated with various extensibility mechanisms.</span></span> <span data-ttu-id="ab849-105">Ce chapitre vous aide à décider des mécanismes d’extensibilité : sous-classement, les événements, les membres virtuels, les rappels et ainsi de suite, pouvez répondent le mieux aux exigences de votre infrastructure.</span><span class="sxs-lookup"><span data-stu-id="ab849-105">This chapter helps you decide which of the extensibility mechanisms—subclassing, events, virtual members, callbacks, and so on—can best meet the requirements of your framework.</span></span>  
  
 <span data-ttu-id="ab849-106">Il existe de nombreuses façons pour permettre l’extensibilité dans les infrastructures.</span><span class="sxs-lookup"><span data-stu-id="ab849-106">There are many ways to allow extensibility in frameworks.</span></span> <span data-ttu-id="ab849-107">Ils comprise entre moins puissants mais moins coûteux et très puissant, mais il est coûteux.</span><span class="sxs-lookup"><span data-stu-id="ab849-107">They range from less powerful but less costly to very powerful but expensive.</span></span> <span data-ttu-id="ab849-108">Pour les besoins d’extensibilité donné, vous devez choisir le mécanisme d’extensibilité moins coûteux qui répond aux exigences.</span><span class="sxs-lookup"><span data-stu-id="ab849-108">For any given extensibility requirement, you should choose the least costly extensibility mechanism that meets the requirements.</span></span> <span data-ttu-id="ab849-109">N’oubliez pas qu’il est généralement possible d’ajouter plus d’extensibilité ultérieurement, mais jamais emportez-la suite sans introduire de modifications avec rupture.</span><span class="sxs-lookup"><span data-stu-id="ab849-109">Keep in mind that it’s usually possible to add more extensibility later, but you can never take it away without introducing breaking changes.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ab849-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ab849-110">In This Section</span></span>  
 [<span data-ttu-id="ab849-111">Classes unsealed</span><span class="sxs-lookup"><span data-stu-id="ab849-111">Unsealed Classes</span></span>](../../../docs/standard/design-guidelines/unsealed-classes.md)  
 [<span data-ttu-id="ab849-112">Membres protégés</span><span class="sxs-lookup"><span data-stu-id="ab849-112">Protected Members</span></span>](../../../docs/standard/design-guidelines/protected-members.md)  
 [<span data-ttu-id="ab849-113">Événements et rappels</span><span class="sxs-lookup"><span data-stu-id="ab849-113">Events and Callbacks</span></span>](../../../docs/standard/design-guidelines/events-and-callbacks.md)  
 [<span data-ttu-id="ab849-114">Membres virtuels</span><span class="sxs-lookup"><span data-stu-id="ab849-114">Virtual Members</span></span>](../../../docs/standard/design-guidelines/virtual-members.md)  
 [<span data-ttu-id="ab849-115">Abstractions (types et interfaces abstraits)</span><span class="sxs-lookup"><span data-stu-id="ab849-115">Abstractions (Abstract Types and Interfaces)</span></span>](../../../docs/standard/design-guidelines/abstractions-abstract-types-and-interfaces.md)  
 [<span data-ttu-id="ab849-116">Classes de base pour l’implémentation d’abstractions</span><span class="sxs-lookup"><span data-stu-id="ab849-116">Base Classes for Implementing Abstractions</span></span>](../../../docs/standard/design-guidelines/base-classes-for-implementing-abstractions.md)  
 [<span data-ttu-id="ab849-117">Scellement</span><span class="sxs-lookup"><span data-stu-id="ab849-117">Sealing</span></span>](../../../docs/standard/design-guidelines/sealing.md)  
 <span data-ttu-id="ab849-118">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="ab849-118">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="ab849-119">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="ab849-119">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab849-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab849-120">See also</span></span>

- [<span data-ttu-id="ab849-121">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ab849-121">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
