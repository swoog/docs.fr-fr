---
title: Déploiement de services
ms.date: 03/30/2017
ms.assetid: ac361bfb-017d-4da9-a2d7-fc0fb72d65bb
ms.openlocfilehash: 17773dc7a6bbed1b88c9324d27a937166e0d9f6b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678978"
---
# <a name="deploying-services"></a><span data-ttu-id="5f869-102">Déploiement de services</span><span class="sxs-lookup"><span data-stu-id="5f869-102">Deploying Services</span></span>
<span data-ttu-id="5f869-103">Cette rubrique décrit comment vous pouvez déployer une application Windows Communication Foundation (WCF) à un environnement d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5f869-103">This topic describes how you can deploy a Windows Communication Foundation (WCF) application to a run-time environment.</span></span>  
  
## <a name="choosing-the-hosting-environment-for-your-application"></a><span data-ttu-id="5f869-104">Choix de l'environnement d'hébergement de votre application</span><span class="sxs-lookup"><span data-stu-id="5f869-104">Choosing the Hosting Environment for Your Application</span></span>  
 <span data-ttu-id="5f869-105">Les services WCF sont conçus pour s’exécuter dans n’importe quel processus Windows qui prend en charge le code managé.</span><span class="sxs-lookup"><span data-stu-id="5f869-105">WCF services are designed to run in any Windows process that supports managed code.</span></span> <span data-ttu-id="5f869-106">Pour devenir actif, un service doit être hébergé dans un environnement d'exécution qui le crée et contrôle son contexte et sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="5f869-106">To become active, a service must be hosted within a run-time environment that creates it and controls its context and lifetime.</span></span> <span data-ttu-id="5f869-107">Les options d'hébergement vont de l'exécution à l'intérieur de l'application console la plus simple à une exécution dans des environnements serveur comme un service Windows et les services Internet (IIS) ou dans un processus de travail géré par WAS (Windows Activation Services).</span><span class="sxs-lookup"><span data-stu-id="5f869-107">Hosting options range from running inside the simplest console application to server environments like a Windows service, Internet Information Services (IIS), or within a worker process managed by the Windows Activation Service (WAS).</span></span> <span data-ttu-id="5f869-108">Pour passer en revue les différentes options d’hébergement pour votre application WCF, consultez [Services d’hébergement](../../../../docs/framework/wcf/hosting-services.md).</span><span class="sxs-lookup"><span data-stu-id="5f869-108">To review the different hosting options for your WCF application, see [Hosting Services](../../../../docs/framework/wcf/hosting-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f869-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f869-109">See also</span></span>
- [<span data-ttu-id="5f869-110">Hébergement</span><span class="sxs-lookup"><span data-stu-id="5f869-110">Hosting</span></span>](../../../../docs/framework/wcf/feature-details/hosting.md)
- [<span data-ttu-id="5f869-111">Hébergement de services</span><span class="sxs-lookup"><span data-stu-id="5f869-111">Hosting Services</span></span>](../../../../docs/framework/wcf/hosting-services.md)
