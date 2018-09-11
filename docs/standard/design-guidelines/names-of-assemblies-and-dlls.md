---
title: Noms d'assemblys et de DLL
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], DLLs
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
- DLLs, names
ms.assetid: e800b610-31b4-4949-9c14-cb60e9f254be
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97bd152cff53fb1c2edb107b6d6b34bd91ca1c49
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44366945"
---
# <a name="names-of-assemblies-and-dlls"></a><span data-ttu-id="ec80c-102">Noms d'assemblys et de DLL</span><span class="sxs-lookup"><span data-stu-id="ec80c-102">Names of Assemblies and DLLs</span></span>
<span data-ttu-id="ec80c-103">Un assembly est l’unité de déploiement et d’identité pour les programmes de code managé.</span><span class="sxs-lookup"><span data-stu-id="ec80c-103">An assembly is the unit of deployment and identity for managed code programs.</span></span> <span data-ttu-id="ec80c-104">Bien que les assemblys peuvent s’étendre sur un ou plusieurs fichiers, en général, un assembly effectue un mappage avec une DLL.</span><span class="sxs-lookup"><span data-stu-id="ec80c-104">Although assemblies can span one or more files, typically an assembly maps one-to-one with a DLL.</span></span> <span data-ttu-id="ec80c-105">Par conséquent, cette section décrit les conventions d’affectation de noms de seul DLL peuvent alors être mappées aux conventions d’affectation de noms d’assembly.</span><span class="sxs-lookup"><span data-stu-id="ec80c-105">Therefore, this section describes only DLL naming conventions, which then can be mapped to assembly naming conventions.</span></span>  
  
 <span data-ttu-id="ec80c-106">**✓ DO** choisissez des noms pour vos DLL d’assembly qui suggèrent des grands segments de fonctionnalités, telles que System.Data.</span><span class="sxs-lookup"><span data-stu-id="ec80c-106">**✓ DO** choose names for your assembly DLLs that suggest large chunks of functionality, such as System.Data.</span></span>  
  
 <span data-ttu-id="ec80c-107">Noms d’assembly et les DLL n’êtes pas obligé de correspondent aux noms d’espace de noms, mais il est raisonnable de suivre le nom de l’espace de noms lorsque vous nommez des assemblys.</span><span class="sxs-lookup"><span data-stu-id="ec80c-107">Assembly and DLL names don’t have to correspond to namespace names, but it is reasonable to follow the namespace name when naming assemblies.</span></span> <span data-ttu-id="ec80c-108">Une règle empirique consiste à nommer la DLL basée sur le préfixe commun des espaces de noms contenus dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ec80c-108">A good rule of thumb is to name the DLL based on the common prefix of the namespaces contained in the assembly.</span></span> <span data-ttu-id="ec80c-109">Par exemple, un assembly avec deux espaces de noms, `MyCompany.MyTechnology.FirstFeature` et `MyCompany.MyTechnology.SecondFeature`, peut être appelée `MyCompany.MyTechnology.dll`.</span><span class="sxs-lookup"><span data-stu-id="ec80c-109">For example, an assembly with two namespaces, `MyCompany.MyTechnology.FirstFeature` and `MyCompany.MyTechnology.SecondFeature`, could be called `MyCompany.MyTechnology.dll`.</span></span>  
  
 <span data-ttu-id="ec80c-110">**✓ CONSIDER** nommer les DLL selon le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="ec80c-110">**✓ CONSIDER** naming DLLs according to the following pattern:</span></span>  
  
 `<Company>.<Component>.dll`  
  
 <span data-ttu-id="ec80c-111">où `<Component>` contient une ou plusieurs clauses séparés par des points.</span><span class="sxs-lookup"><span data-stu-id="ec80c-111">where `<Component>` contains one or more dot-separated clauses.</span></span> <span data-ttu-id="ec80c-112">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ec80c-112">For example:</span></span>  
  
 <span data-ttu-id="ec80c-113">`Litware.Controls.dll`.</span><span class="sxs-lookup"><span data-stu-id="ec80c-113">`Litware.Controls.dll`.</span></span>  
  
 <span data-ttu-id="ec80c-114">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="ec80c-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="ec80c-115">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="ec80c-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec80c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec80c-116">See also</span></span>

- [<span data-ttu-id="ec80c-117">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ec80c-117">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="ec80c-118">Directives de nommage</span><span class="sxs-lookup"><span data-stu-id="ec80c-118">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
