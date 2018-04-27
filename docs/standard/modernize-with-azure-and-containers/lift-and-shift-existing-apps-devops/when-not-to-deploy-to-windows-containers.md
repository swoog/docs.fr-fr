---
title: Quand ne pas déployer des conteneurs Windows
description: Architecture de Microservices .NET pour les Applications .NET en conteneur | Quand ne pas déployer des conteneurs Windows
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/26/2017
ms.prod: .net
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: b8fb31a17d1f9d91fe053596685b7560a7fa1ee1
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="when-not-to-deploy-to-windows-containers"></a><span data-ttu-id="af9cb-103">Quand ne pas déployer des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="af9cb-103">When not to deploy to Windows Containers</span></span>

<span data-ttu-id="af9cb-104">Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="af9cb-104">Some Windows technologies are not supported by Windows Containers.</span></span> <span data-ttu-id="af9cb-105">Dans ce cas, vous devrez migrer vers les machines virtuelles aux normes, généralement avec Windows et de IIS.</span><span class="sxs-lookup"><span data-stu-id="af9cb-105">In those cases, you still need to migrate to standards VMs, usually with just Windows and IIS.</span></span>

<span data-ttu-id="af9cb-106">Cas non pris en charge dans les conteneurs Windows, à compter de mid 2017 :</span><span class="sxs-lookup"><span data-stu-id="af9cb-106">Cases not supported in Windows Containers, as of mid-2017:</span></span>

-   <span data-ttu-id="af9cb-107">Microsoft Message Queuing (MSMQ) actuellement n’est pas pris en charge dans les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="af9cb-107">Microsoft Message Queuing (MSMQ) currently is not supported in Windows Containers.</span></span>

    -   [<span data-ttu-id="af9cb-108">Forum sur la demande UserVoice</span><span class="sxs-lookup"><span data-stu-id="af9cb-108">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

    -   [<span data-ttu-id="af9cb-109">Forum de discussion</span><span class="sxs-lookup"><span data-stu-id="af9cb-109">Discussion forum</span></span>](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

-   <span data-ttu-id="af9cb-110">Microsoft Distributed Transaction Coordinator (MSDTC) en n'est pas pris en charge dans les conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="af9cb-110">Microsoft Distributed Transaction Coordinator (MSDTC) currently is not supported in Windows Containers</span></span>

    -   [<span data-ttu-id="af9cb-111">Problème GitHub</span><span class="sxs-lookup"><span data-stu-id="af9cb-111">GitHub issue</span></span>](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

-   <span data-ttu-id="af9cb-112">Microsoft Office ne prend actuellement pas en charge les conteneurs</span><span class="sxs-lookup"><span data-stu-id="af9cb-112">Microsoft Office currently does not support containers</span></span>

    -   [<span data-ttu-id="af9cb-113">Forum sur la demande UserVoice</span><span class="sxs-lookup"><span data-stu-id="af9cb-113">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

<span data-ttu-id="af9cb-114">Pour les requêtes à partir de la Communauté et d’autres scénarios non pris en charge, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.</span><span class="sxs-lookup"><span data-stu-id="af9cb-114">For additional not-supported scenarios and requests from the community, see the UserVoice forum for Windows Containers: <https://windowsserver.uservoice.com/forums/304624-containers>.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="af9cb-115">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="af9cb-115">Additional resources</span></span>

-   <span data-ttu-id="af9cb-116">**Machines virtuelles et les conteneurs dans Azure**</span><span class="sxs-lookup"><span data-stu-id="af9cb-116">**Virtual machines and containers in Azure**</span></span>

    [https://docs.microsoft.com/azure/virtual-machines/windows/containers](https://docs.microsoft.com/azure/virtual-machines/windows/containers)

>[!div class="step-by-step"]
<span data-ttu-id="af9cb-117">[Précédent](deploy-existing-net-apps-as-windows-containers.md)
[Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span><span class="sxs-lookup"><span data-stu-id="af9cb-117">[Previous](deploy-existing-net-apps-as-windows-containers.md)
[Next](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span></span>
