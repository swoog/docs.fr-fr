---
title: "Quand ne pas déployer des conteneurs Windows"
description: "Architecture de Microservices .NET pour les Applications .NET en conteneur | Quand ne pas déployer des conteneurs Windows"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/26/2017
ms.prod: .net
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: cb671ec88da7ff1aa5c960c210e0da5e9d753280
ms.sourcegitcommit: d3cfda0943364aaf6ccd574f55f584576c8a4fee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2018
---
# <a name="when-not-to-deploy-to-windows-containers"></a><span data-ttu-id="1933a-103">Quand ne pas déployer des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="1933a-103">When not to deploy to Windows Containers</span></span>

<span data-ttu-id="1933a-104">Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="1933a-104">Some Windows technologies are not supported by Windows Containers.</span></span> <span data-ttu-id="1933a-105">Dans ce cas, vous devrez migrer vers les machines virtuelles aux normes, généralement avec Windows et de IIS.</span><span class="sxs-lookup"><span data-stu-id="1933a-105">In those cases, you still need to migrate to standards VMs, usually with just Windows and IIS.</span></span>

<span data-ttu-id="1933a-106">Cas non pris en charge dans les conteneurs Windows, à compter de mid 2017 :</span><span class="sxs-lookup"><span data-stu-id="1933a-106">Cases not supported in Windows Containers, as of mid-2017:</span></span>

-   <span data-ttu-id="1933a-107">Microsoft Message Queuing (MSMQ) actuellement n’est pas pris en charge dans les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="1933a-107">Microsoft Message Queuing (MSMQ) currently is not supported in Windows Containers.</span></span>

    -   [<span data-ttu-id="1933a-108">Forum sur la demande UserVoice</span><span class="sxs-lookup"><span data-stu-id="1933a-108">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

    -   [<span data-ttu-id="1933a-109">Forum de discussion</span><span class="sxs-lookup"><span data-stu-id="1933a-109">Discussion forum</span></span>](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

-   <span data-ttu-id="1933a-110">Microsoft Distributed Transaction Coordinator (MSDTC) en n'est pas pris en charge dans les conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="1933a-110">Microsoft Distributed Transaction Coordinator (MSDTC) currently is not supported in Windows Containers</span></span>

    -   [<span data-ttu-id="1933a-111">Problème GitHub</span><span class="sxs-lookup"><span data-stu-id="1933a-111">GitHub issue</span></span>](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

-   <span data-ttu-id="1933a-112">Microsoft Office ne prend actuellement pas en charge les conteneurs</span><span class="sxs-lookup"><span data-stu-id="1933a-112">Microsoft Office currently does not support containers</span></span>

    -   [<span data-ttu-id="1933a-113">Forum sur la demande UserVoice</span><span class="sxs-lookup"><span data-stu-id="1933a-113">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

<span data-ttu-id="1933a-114">Pour les requêtes à partir de la Communauté et d’autres scénarios non pris en charge, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.</span><span class="sxs-lookup"><span data-stu-id="1933a-114">For additional not-supported scenarios and requests from the community, see the UserVoice forum for Windows Containers: <https://windowsserver.uservoice.com/forums/304624-containers>.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="1933a-115">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="1933a-115">Additional resources</span></span>

-   <span data-ttu-id="1933a-116">**Machines virtuelles et les conteneurs dans Azure**</span><span class="sxs-lookup"><span data-stu-id="1933a-116">**Virtual machines and containers in Azure**</span></span>

    [<span data-ttu-id="1933a-117">https://docs.microsoft.com/azure/virtual-machines/windows/containers</span><span class="sxs-lookup"><span data-stu-id="1933a-117">https://docs.microsoft.com/azure/virtual-machines/windows/containers</span></span>](https://docs.microsoft.com/azure/virtual-machines/windows/containers)

>[!div class="step-by-step"]
<span data-ttu-id="1933a-118">[Précédent](deploy-existing-net-apps-as-windows-containers.md)
[Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span><span class="sxs-lookup"><span data-stu-id="1933a-118">[Previous](deploy-existing-net-apps-as-windows-containers.md)
[Next](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span></span>
