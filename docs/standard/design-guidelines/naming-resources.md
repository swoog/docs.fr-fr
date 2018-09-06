---
title: Attribution d'un nom à des ressources
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], localized resources
- localization, naming guidelines
- resource names
- global applications, naming guidelines
- international applications, naming guidelines
ms.assetid: 8b0e97f3-7877-44fd-bc76-e05d36d5d79c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5b53fc383e6fc9a5f056bab4eabde9979cd734b
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43875107"
---
# <a name="naming-resources"></a><span data-ttu-id="fa46f-102">Attribution d'un nom à des ressources</span><span class="sxs-lookup"><span data-stu-id="fa46f-102">Naming Resources</span></span>
<span data-ttu-id="fa46f-103">Étant donné que les ressources localisables peuvent être référencés par le biais de certains objets comme s’ils étaient des propriétés, les instructions d’affectation de noms pour les ressources sont similaires aux instructions de la propriété.</span><span class="sxs-lookup"><span data-stu-id="fa46f-103">Because localizable resources can be referenced via certain objects as if they were properties, the naming guidelines for resources are similar to property guidelines.</span></span>  
  
 <span data-ttu-id="fa46f-104">**✓ DO** utilisent la casse Pascal dans les clés de ressources.</span><span class="sxs-lookup"><span data-stu-id="fa46f-104">**✓ DO** use PascalCasing in resource keys.</span></span>  
  
 <span data-ttu-id="fa46f-105">**✓ DO** fournir descriptif au lieu d’identificateurs courts.</span><span class="sxs-lookup"><span data-stu-id="fa46f-105">**✓ DO** provide descriptive rather than short identifiers.</span></span>  
  
 <span data-ttu-id="fa46f-106">**X DO NOT** utiliser des mots clés de langage spécifique langage CLR principal.</span><span class="sxs-lookup"><span data-stu-id="fa46f-106">**X DO NOT** use language-specific keywords of the main CLR languages.</span></span>  
  
 <span data-ttu-id="fa46f-107">**✓ DO** utiliser uniquement des caractères alphanumériques et des traits de soulignement dans les noms des ressources.</span><span class="sxs-lookup"><span data-stu-id="fa46f-107">**✓ DO** use only alphanumeric characters and underscores in naming resources.</span></span>  
  
 <span data-ttu-id="fa46f-108">**✓ DO** utilisent la convention d’affectation de noms suivante pour les ressources de message d’exception.</span><span class="sxs-lookup"><span data-stu-id="fa46f-108">**✓ DO** use the following naming convention for exception message resources.</span></span>  
  
 <span data-ttu-id="fa46f-109">L’identificateur de ressource doit être le nom du type exception ainsi qu’un identificateur court de l’exception :</span><span class="sxs-lookup"><span data-stu-id="fa46f-109">The resource identifier should be the exception type name plus a short identifier of the exception:</span></span>  
  
 `ArgumentExceptionIllegalCharacters`  
 `ArgumentExceptionInvalidName`  
 `ArgumentExceptionFileNameIsMalformed`  
  
 <span data-ttu-id="fa46f-110">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="fa46f-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="fa46f-111">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="fa46f-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa46f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa46f-112">See also</span></span>

- [<span data-ttu-id="fa46f-113">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="fa46f-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="fa46f-114">Directives de nommage</span><span class="sxs-lookup"><span data-stu-id="fa46f-114">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
