---
title: Programmation à l'aide de domaines d'application et d'assemblys
ms.date: 03/30/2017
helpviewer_keywords:
- assemblies [.NET Framework], programming
- programming assemblies
- application domains, programming
- programming application domains
ms.assetid: 96d3b8e3-bef8-4da0-9a81-9841e23a94e9
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7124b6b234601e3afc27109ac318f47e3fe40c35
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675349"
---
# <a name="programming-with-application-domains-and-assemblies"></a><span data-ttu-id="69499-102">Programmation à l'aide de domaines d'application et d'assemblys</span><span class="sxs-lookup"><span data-stu-id="69499-102">Programming with Application Domains and Assemblies</span></span>
<span data-ttu-id="69499-103">Les ordinateurs hôtes tels que Microsoft Internet Explorer, ASP.NET et le shell Windows chargent le Common Language Runtime dans un processus, créent un [domaine d’application](../../../docs/framework/app-domains/application-domains.md) dans ce processus, puis chargent et exécutent le code utilisateur dans ce domaine d’application lors de l’exécution d’une application .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="69499-103">Hosts such as Microsoft Internet Explorer, ASP.NET, and the Windows shell load the common language runtime into a process, create an [application domain](../../../docs/framework/app-domains/application-domains.md) in that process, and then load and execute user code in that application domain when running a .NET Framework application.</span></span> <span data-ttu-id="69499-104">Dans la plupart des cas, vous n’avez pas à vous soucier de la création des domaines d’application et du chargement des assemblys dans ces domaines car l’hôte runtime effectue ces tâches.</span><span class="sxs-lookup"><span data-stu-id="69499-104">In most cases, you do not have to worry about creating application domains and loading assemblies into them because the runtime host performs those tasks.</span></span>  
  
 <span data-ttu-id="69499-105">Toutefois, si vous créez une application qui hébergera le Common Language Runtime, créez des outils ou un code que vous souhaitez décharger par programmation, ou créez des composants enfichables pouvant être déchargés et rechargés à la volée, vous allez créer vos propres domaines d’application.</span><span class="sxs-lookup"><span data-stu-id="69499-105">However, if you are creating an application that will host the common language runtime, creating tools or code you want to unload programmatically, or creating pluggable components that can be unloaded and reloaded on the fly, you will be creating your own application domains.</span></span> <span data-ttu-id="69499-106">Même si vous ne créez aucun hôte de runtime, cette section fournit des informations importantes sur l’utilisation des domaines d’application et assemblys chargés dans ces domaines d’application.</span><span class="sxs-lookup"><span data-stu-id="69499-106">Even if you are not creating a runtime host, this section provides important information on how to work with application domains and assemblies loaded in these application domains.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="69499-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="69499-107">In This Section</span></span>  
 [<span data-ttu-id="69499-108">Rubriques Guide pratique relatives aux domaines d'application et aux assemblys</span><span class="sxs-lookup"><span data-stu-id="69499-108">Application Domains and Assemblies How-to Topics</span></span>](../../../docs/framework/app-domains/application-domains-and-assemblies-how-to-topics.md)  
 <span data-ttu-id="69499-109">Fournit des liens vers toutes les rubriques Guide pratique de la documentation conceptuelle pour la programmation avec des domaines d’application et des assemblys.</span><span class="sxs-lookup"><span data-stu-id="69499-109">Provides links to all How-to topics found in the conceptual documentation for programming with application domains and assemblies.</span></span>  
  
 [<span data-ttu-id="69499-110">Utilisation des domaines d’application</span><span class="sxs-lookup"><span data-stu-id="69499-110">Using Application Domains</span></span>](../../../docs/framework/app-domains/use.md)  
 <span data-ttu-id="69499-111">Fournit des exemples de création, de configuration et d’utilisation des domaines d’application.</span><span class="sxs-lookup"><span data-stu-id="69499-111">Provides examples of creating, configuring, and using application domains.</span></span>  
  
 [<span data-ttu-id="69499-112">Programmation à l’aide d’assemblys</span><span class="sxs-lookup"><span data-stu-id="69499-112">Programming with Assemblies</span></span>](../../../docs/framework/app-domains/programming-with-assemblies.md)  
 <span data-ttu-id="69499-113">Décrit comment créer, signer et définir des attributs sur des assemblys.</span><span class="sxs-lookup"><span data-stu-id="69499-113">Describes how to create, sign, and set attributes on assemblies.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="69499-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69499-114">Related Sections</span></span>  
 [<span data-ttu-id="69499-115">Émission d’assemblys et de méthodes dynamiques</span><span class="sxs-lookup"><span data-stu-id="69499-115">Emitting Dynamic Methods and Assemblies</span></span>](../../../docs/framework/reflection-and-codedom/emitting-dynamic-methods-and-assemblies.md)  
 <span data-ttu-id="69499-116">Décrit comment créer des assemblys dynamiques.</span><span class="sxs-lookup"><span data-stu-id="69499-116">Describes how to create dynamic assemblies.</span></span>  
  
 [<span data-ttu-id="69499-117">Assemblys dans le Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="69499-117">Assemblies in the Common Language Runtime</span></span>](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)  
 <span data-ttu-id="69499-118">Fournit une vue d'ensemble conceptuelle des assemblys.</span><span class="sxs-lookup"><span data-stu-id="69499-118">Provides a conceptual overview of assemblies.</span></span>  
  
 [<span data-ttu-id="69499-119">Domaines d’application</span><span class="sxs-lookup"><span data-stu-id="69499-119">Application Domains</span></span>](../../../docs/framework/app-domains/application-domains.md)  
 <span data-ttu-id="69499-120">Fournit une vue d'ensemble conceptuelle des domaines d'application.</span><span class="sxs-lookup"><span data-stu-id="69499-120">Provides a conceptual overview of application domains.</span></span>  
  
 [<span data-ttu-id="69499-121">Vue d’ensemble de la réflexion</span><span class="sxs-lookup"><span data-stu-id="69499-121">Reflection Overview</span></span>](../../../docs/framework/reflection-and-codedom/reflection.md)  
 <span data-ttu-id="69499-122">Explique comment utiliser la classe **Reflection** pour obtenir des informations sur un assembly.</span><span class="sxs-lookup"><span data-stu-id="69499-122">Describes how to use the **Reflection** class to obtain information about an assembly.</span></span>
