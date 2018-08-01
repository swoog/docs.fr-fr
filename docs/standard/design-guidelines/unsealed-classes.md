---
title: Classes unsealed
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 672d36c6b888ee9a89a76d5d417a7a7e92dd8f36
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571659"
---
# <a name="unsealed-classes"></a><span data-ttu-id="28517-102">Classes unsealed</span><span class="sxs-lookup"><span data-stu-id="28517-102">Unsealed Classes</span></span>
<span data-ttu-id="28517-103">Classes sealed ne peut pas être héritées, et empêchent d’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="28517-103">Sealed classes cannot be inherited from, and they prevent extensibility.</span></span> <span data-ttu-id="28517-104">En revanche, les classes qui peuvent être héritées sont appelées classes unsealed.</span><span class="sxs-lookup"><span data-stu-id="28517-104">In contrast, classes that can be inherited from are called unsealed classes.</span></span>  
  
 <span data-ttu-id="28517-105">**✓ CONSIDER** à l’aide des classes unsealed sans aucune ajouté des membres virtuels ou protégés comme un excellent moyen de fournir un peu coûteux encore apprécié extensibilité à une infrastructure.</span><span class="sxs-lookup"><span data-stu-id="28517-105">**✓ CONSIDER** using unsealed classes with no added virtual or protected members as a great way to provide inexpensive yet much appreciated extensibility to a framework.</span></span>  
  
 <span data-ttu-id="28517-106">Les développeurs souhaitent souvent héritent des classes unsealed afin d’ajouter des membres de commodité telles que les constructeurs personnalisés, les nouvelles méthodes ou les surcharges de méthode.</span><span class="sxs-lookup"><span data-stu-id="28517-106">Developers often want to inherit from unsealed classes so as to add convenience members such as custom constructors, new methods, or method overloads.</span></span> <span data-ttu-id="28517-107">Par exemple, `System.Messaging.MessageQueue` est non scellé, et permet ainsi aux utilisateurs de créer des files d’attente personnalisées cette valeur par défaut pour un chemin d’accès de la file d’attente particulière ou ajouter des méthodes personnalisées qui simplifient l’API pour des scénarios spécifiques.</span><span class="sxs-lookup"><span data-stu-id="28517-107">For example,  `System.Messaging.MessageQueue` is unsealed and thus allows users to create custom queues that default to a particular queue path or to add custom methods that simplify the API for specific scenarios.</span></span>  
  
 <span data-ttu-id="28517-108">Classes sont non scellés par défaut dans les langages de programmation plus, et c’est également la valeur par défaut recommandée pour la plupart des classes dans les infrastructures.</span><span class="sxs-lookup"><span data-stu-id="28517-108">Classes are unsealed by default in most programming languages, and this is also the recommended default for most classes in frameworks.</span></span> <span data-ttu-id="28517-109">L’extensibilité offerte par les types unsealed est bien appréciés par les utilisateurs de l’infrastructure et relativement peu coûteux fournir des coûts relativement faible de test associées aux types unsealed.</span><span class="sxs-lookup"><span data-stu-id="28517-109">The extensibility afforded by unsealed types is much appreciated by framework users and quite inexpensive to provide because of relatively low test costs associated with unsealed types.</span></span>  
  
 <span data-ttu-id="28517-110">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="28517-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="28517-111">*Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="28517-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28517-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28517-112">See Also</span></span>  
 [<span data-ttu-id="28517-113">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="28517-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
 [<span data-ttu-id="28517-114">Conception en vue de l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="28517-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
 [<span data-ttu-id="28517-115">Scellement</span><span class="sxs-lookup"><span data-stu-id="28517-115">Sealing</span></span>](../../../docs/standard/design-guidelines/sealing.md)
