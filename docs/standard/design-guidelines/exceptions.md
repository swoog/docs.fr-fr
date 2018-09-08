---
title: Instructions de conception pour les exceptions
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- exceptions [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], exceptions
- errors [.NET Framework], exceptions
- reporting errors
ms.assetid: bc177b2f-7528-4ae4-83db-aacfb04b86d0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51cc5296a7b3f6d75b5e56d6bbc74330fa147848
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44140955"
---
# <a name="design-guidelines-for-exceptions"></a><span data-ttu-id="237fa-102">Instructions de conception pour les exceptions</span><span class="sxs-lookup"><span data-stu-id="237fa-102">Design Guidelines for Exceptions</span></span>
<span data-ttu-id="237fa-103">Gestion des exceptions présente de nombreux avantages sur le rapport d’erreurs basée sur la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="237fa-103">Exception handling has many advantages over return-value-based error reporting.</span></span> <span data-ttu-id="237fa-104">Conception de bonne infrastructure permet le développeur d’applications de tirer parti d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="237fa-104">Good framework design helps the application developer realize the benefits of exceptions.</span></span> <span data-ttu-id="237fa-105">Cette section décrit les avantages des exceptions et présente des recommandations pour les utiliser efficacement.</span><span class="sxs-lookup"><span data-stu-id="237fa-105">This section discusses the benefits of exceptions and presents guidelines for using them effectively.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="237fa-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="237fa-106">In This Section</span></span>  
 [<span data-ttu-id="237fa-107">Levée d’exceptions</span><span class="sxs-lookup"><span data-stu-id="237fa-107">Exception Throwing</span></span>](../../../docs/standard/design-guidelines/exception-throwing.md)  
 [<span data-ttu-id="237fa-108">Utilisation de types d’exceptions standard</span><span class="sxs-lookup"><span data-stu-id="237fa-108">Using Standard Exception Types</span></span>](../../../docs/standard/design-guidelines/using-standard-exception-types.md)  
 [<span data-ttu-id="237fa-109">Exceptions et performances</span><span class="sxs-lookup"><span data-stu-id="237fa-109">Exceptions and Performance</span></span>](../../../docs/standard/design-guidelines/exceptions-and-performance.md)  
 <span data-ttu-id="237fa-110">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="237fa-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="237fa-111">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="237fa-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="237fa-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="237fa-112">See also</span></span>

- [<span data-ttu-id="237fa-113">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="237fa-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
