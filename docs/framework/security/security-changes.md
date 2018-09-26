---
title: Modifications de sécurité dans le .NET Framework
ms.date: 03/30/2017
helpviewer_keywords:
- Allow Partially Trusted Callers attribute
- .NET Framework 4, security changes
- .NET Framework security
- security-transparent code
- security-critical code
- code access security, changes
ms.assetid: 5e87881c-9c13-4b52-8ad1-e34bb46e8aaa
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c62a469b3e31283e5790c747092a8fe504ef8c2a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47107907"
---
# <a name="security-changes-in-the-net-framework"></a><span data-ttu-id="3eaa8-102">Modifications de sécurité dans le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3eaa8-102">Security Changes in the .NET Framework</span></span>
<span data-ttu-id="3eaa8-103">L'évolution la plus importante sur le plan de la sécurité dans le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] est l'utilisation de noms forts.</span><span class="sxs-lookup"><span data-stu-id="3eaa8-103">The most important change to security in the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] is in strong naming.</span></span> <span data-ttu-id="3eaa8-104">Pour obtenir une description de ces modifications, consultez [Enhanced Strong Naming](../../../docs/framework/app-domains/enhanced-strong-naming.md) .</span><span class="sxs-lookup"><span data-stu-id="3eaa8-104">See [Enhanced Strong Naming](../../../docs/framework/app-domains/enhanced-strong-naming.md) for a description of those changes.</span></span>  
  
 <span data-ttu-id="3eaa8-105">Le .NET Framework fournit un modèle de sécurité à deux niveaux pour les applications managées.</span><span class="sxs-lookup"><span data-stu-id="3eaa8-105">The .NET Framework provides a two-tier security model for managed applications.</span></span> <span data-ttu-id="3eaa8-106">Les applications[!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] s'exécutent dans un conteneur de sécurité Windows qui limite l'accès aux ressources.</span><span class="sxs-lookup"><span data-stu-id="3eaa8-106">[!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] apps run in a Windows security container that limits access to resources.</span></span> <span data-ttu-id="3eaa8-107">Dans ce conteneur, les applications managées s'exécutent en mode confiance totale.</span><span class="sxs-lookup"><span data-stu-id="3eaa8-107">Within that container, managed applications run fully trusted.</span></span> <span data-ttu-id="3eaa8-108">Du point de vue de la sécurité d'accès du code (CAS), un développeur ne peut rien faire pour élever les privilèges.</span><span class="sxs-lookup"><span data-stu-id="3eaa8-108">From a code access security (CAS) perspective, there is nothing a developer can do to elevate privileges.</span></span> <span data-ttu-id="3eaa8-109">Pour plus d’informations sur les privilèges octroyés par Windows, consultez [Déclarations des fonctionnalités d’application (applications du Windows Store)](https://go.microsoft.com/fwlink/?LinkId=230436) dans le centre de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="3eaa8-109">For information about the privileges granted by Windows, see [App capability declarations (Windows Store apps)](https://go.microsoft.com/fwlink/?LinkId=230436) in the Windows Dev Center.</span></span> <span data-ttu-id="3eaa8-110">Pour plus d’informations sur la création d’une application [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] , consultez [Créer votre première application Windows Runtime en C# ou Visual Basic](https://go.microsoft.com/fwlink/?LinkId=230461).</span><span class="sxs-lookup"><span data-stu-id="3eaa8-110">For information about creating a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app, see [Create your first Windows Store app using C# or Visual Basic](https://go.microsoft.com/fwlink/?LinkId=230461).</span></span>
