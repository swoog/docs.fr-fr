---
title: Instructions de conception des membres
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines [.NET Framework], about member design guidelines
- members [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], members
- member design guidelines [.NET Framework]
ms.assetid: 0ce93180-1d7b-4f8c-9306-f828b2d66b8f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1c04b431224a1d4f03e85397b854a52856e114e6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571395"
---
# <a name="member-design-guidelines"></a><span data-ttu-id="df994-102">Instructions de conception des membres</span><span class="sxs-lookup"><span data-stu-id="df994-102">Member Design Guidelines</span></span>
<span data-ttu-id="df994-103">Méthodes, propriétés, événements, constructeurs et les champs sont collectivement en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="df994-103">Methods, properties, events, constructors, and fields are collectively referred to as members.</span></span> <span data-ttu-id="df994-104">Les membres sont finalement les moyens par lesquels les fonctionnalités de framework sont exposées aux utilisateurs finaux d’une infrastructure.</span><span class="sxs-lookup"><span data-stu-id="df994-104">Members are ultimately the means by which framework functionality is exposed to the end users of a framework.</span></span>  
  
 <span data-ttu-id="df994-105">Les membres peuvent être virtuel ou non virtuelle, concret ou abstrait, statique ou instance et peuvent avoir plusieurs étendues différentes d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="df994-105">Members can be virtual or nonvirtual, concrete or abstract, static or instance, and can have several different scopes of accessibility.</span></span> <span data-ttu-id="df994-106">Tous les différents fournit incroyable simplicité, mais en même temps requiert soins par le Concepteur de framework.</span><span class="sxs-lookup"><span data-stu-id="df994-106">All this variety provides incredible expressiveness but at the same time requires care on the part of the framework designer.</span></span>  
  
 <span data-ttu-id="df994-107">Ce chapitre propose des conseils de base qui doivent être suivies lors de la conception des membres de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="df994-107">This chapter offers basic guidelines that should be followed when designing members of any type.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="df994-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="df994-108">In This Section</span></span>  
 [<span data-ttu-id="df994-109">Surcharge de membre</span><span class="sxs-lookup"><span data-stu-id="df994-109">Member Overloading</span></span>](../../../docs/standard/design-guidelines/member-overloading.md)  
 [<span data-ttu-id="df994-110">Conception des propriétés</span><span class="sxs-lookup"><span data-stu-id="df994-110">Property Design</span></span>](../../../docs/standard/design-guidelines/property.md)  
 [<span data-ttu-id="df994-111">Conception de constructeurs</span><span class="sxs-lookup"><span data-stu-id="df994-111">Constructor Design</span></span>](../../../docs/standard/design-guidelines/constructor.md)  
 [<span data-ttu-id="df994-112">Conception d’événements</span><span class="sxs-lookup"><span data-stu-id="df994-112">Event Design</span></span>](../../../docs/standard/design-guidelines/event.md)  
 [<span data-ttu-id="df994-113">Conception de champs</span><span class="sxs-lookup"><span data-stu-id="df994-113">Field Design</span></span>](../../../docs/standard/design-guidelines/field.md)  
 [<span data-ttu-id="df994-114">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="df994-114">Extension Methods</span></span>](../../../docs/standard/design-guidelines/extension-methods.md)  
 [<span data-ttu-id="df994-115">Surcharges d’opérateurs</span><span class="sxs-lookup"><span data-stu-id="df994-115">Operator Overloads</span></span>](../../../docs/standard/design-guidelines/operator-overloads.md)  
 [<span data-ttu-id="df994-116">Conception de paramètres</span><span class="sxs-lookup"><span data-stu-id="df994-116">Parameter Design</span></span>](../../../docs/standard/design-guidelines/parameter-design.md)  
 <span data-ttu-id="df994-117">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="df994-117">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="df994-118">*Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="df994-118">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df994-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df994-119">See Also</span></span>  
 [<span data-ttu-id="df994-120">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="df994-120">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
