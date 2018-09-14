---
title: Déploiement d'applications WCF à l'aide de ClickOnce
ms.date: 03/30/2017
ms.assetid: 1a11feee-2a47-4d3e-a28a-ad69d5ff93e0
ms.openlocfilehash: d733c6f523393737418c6394707c1d4e6e9c1710
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45590492"
---
# <a name="deploying-wcf-applications-with-clickonce"></a><span data-ttu-id="dbc56-102">Déploiement d'applications WCF à l'aide de ClickOnce</span><span class="sxs-lookup"><span data-stu-id="dbc56-102">Deploying WCF Applications with ClickOnce</span></span>
<span data-ttu-id="dbc56-103">Les applications clientes à l’aide de Windows Communication Foundation (WCF) peuvent être déployées à l’aide de la technologie ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="dbc56-103">Client applications using Windows Communication Foundation (WCF) may be deployed using ClickOnce technology.</span></span> <span data-ttu-id="dbc56-104">Cette technologie leur permet de tirer parti des protections de sécurité d'exécution fournies par la sécurité d'accès du code, sous réserve qu'elles soient signées numériquement avec un certificat approuvé.</span><span class="sxs-lookup"><span data-stu-id="dbc56-104">This technology allows them to take advantage of the runtime security protections provided by Code Access Security, provided that they are digitally signed with a trusted certificate.</span></span> <span data-ttu-id="dbc56-105">Le certificat utilisé pour signer l'application ClickOnce doit résider dans le magasin d'éditeurs approuvés, et la stratégie de sécurité locale sur l'ordinateur client doit être configurée pour accorder des autorisations Confiance totale aux applications signées avec le certificat de l'éditeur.</span><span class="sxs-lookup"><span data-stu-id="dbc56-105">The certificate used to sign the ClickOnce application must reside in the Trusted Publisher store, and the local security policy on the client machine must be configured to grant Full Trust permissions to applications signed with the publisher's certificate.</span></span>  
  
 <span data-ttu-id="dbc56-106">Pour plus d’informations sur la configuration des applications ClickOnce et éditeurs approuvés, consultez [configuration d’éditeurs approuvés ClickOnce](https://go.microsoft.com/fwlink/?LinkId=94774).</span><span class="sxs-lookup"><span data-stu-id="dbc56-106">For information on configuring ClickOnce applications and trusted publishers, see [Configuring ClickOnce Trusted Publishers](https://go.microsoft.com/fwlink/?LinkId=94774).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbc56-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbc56-107">See Also</span></span>  
 [<span data-ttu-id="dbc56-108">Vue d’ensemble du déploiement d’applications approuvées</span><span class="sxs-lookup"><span data-stu-id="dbc56-108">Trusted Application Deployment Overview</span></span>](https://go.microsoft.com/fwlink/?LinkId=94775)  
 [<span data-ttu-id="dbc56-109">Applications de déploiement ClickOnce pour les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dbc56-109">ClickOnce Deployment for Windows Forms Applications</span></span>](https://go.microsoft.com/fwlink/?LinkId=94776)
