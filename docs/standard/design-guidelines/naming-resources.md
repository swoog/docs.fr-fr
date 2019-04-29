---
title: Attribution d'un nom à des ressources
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], localized resources
- localization, naming guidelines
- resource names
- global applications, naming guidelines
- international applications, naming guidelines
ms.assetid: 8b0e97f3-7877-44fd-bc76-e05d36d5d79c
author: KrzysztofCwalina
ms.openlocfilehash: 44627aafd9ec779625413a0862412a8f6c408109
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756882"
---
# <a name="naming-resources"></a><span data-ttu-id="3a603-102">Attribution d'un nom à des ressources</span><span class="sxs-lookup"><span data-stu-id="3a603-102">Naming Resources</span></span>
<span data-ttu-id="3a603-103">Étant donné que les ressources localisables peuvent être référencés par le biais de certains objets comme s’ils étaient des propriétés, les instructions d’affectation de noms pour les ressources sont similaires aux instructions de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3a603-103">Because localizable resources can be referenced via certain objects as if they were properties, the naming guidelines for resources are similar to property guidelines.</span></span>  
  
 <span data-ttu-id="3a603-104">**✓ DO** utilisent la casse Pascal dans les clés de ressources.</span><span class="sxs-lookup"><span data-stu-id="3a603-104">**✓ DO** use PascalCasing in resource keys.</span></span>  
  
 <span data-ttu-id="3a603-105">**✓ DO** fournir descriptif au lieu d’identificateurs courts.</span><span class="sxs-lookup"><span data-stu-id="3a603-105">**✓ DO** provide descriptive rather than short identifiers.</span></span>  
  
 <span data-ttu-id="3a603-106">**X DO NOT** utiliser des mots clés de langage spécifique langage CLR principal.</span><span class="sxs-lookup"><span data-stu-id="3a603-106">**X DO NOT** use language-specific keywords of the main CLR languages.</span></span>  
  
 <span data-ttu-id="3a603-107">**✓ DO** utiliser uniquement des caractères alphanumériques et des traits de soulignement dans les noms des ressources.</span><span class="sxs-lookup"><span data-stu-id="3a603-107">**✓ DO** use only alphanumeric characters and underscores in naming resources.</span></span>  
  
 <span data-ttu-id="3a603-108">**✓ DO** utilisent la convention d’affectation de noms suivante pour les ressources de message d’exception.</span><span class="sxs-lookup"><span data-stu-id="3a603-108">**✓ DO** use the following naming convention for exception message resources.</span></span>  
  
 <span data-ttu-id="3a603-109">L’identificateur de ressource doit être le nom du type exception ainsi qu’un identificateur court de l’exception :</span><span class="sxs-lookup"><span data-stu-id="3a603-109">The resource identifier should be the exception type name plus a short identifier of the exception:</span></span>  
  
 `ArgumentExceptionIllegalCharacters`  
 `ArgumentExceptionInvalidName`  
 `ArgumentExceptionFileNameIsMalformed`  
  
 <span data-ttu-id="3a603-110">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="3a603-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="3a603-111">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="3a603-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a603-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a603-112">See also</span></span>

- [<span data-ttu-id="3a603-113">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3a603-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
- [<span data-ttu-id="3a603-114">Directives de nommage</span><span class="sxs-lookup"><span data-stu-id="3a603-114">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
