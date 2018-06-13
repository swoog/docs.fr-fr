---
title: Quand ne pas déployer des conteneurs Windows
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Quand ne pas déployer des conteneurs Windows
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 819f32955ff019414bef8820d17d272eddc11bf8
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
ms.locfileid: "33957959"
---
# <a name="when-not-to-deploy-to-windows-containers"></a><span data-ttu-id="e9332-103">Quand ne pas déployer des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="e9332-103">When not to deploy to Windows Containers</span></span>

<span data-ttu-id="e9332-104">Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="e9332-104">Some Windows technologies are not supported by Windows Containers.</span></span> <span data-ttu-id="e9332-105">Dans ce cas, vous devrez migrer vers les machines virtuelles aux normes, généralement avec Windows et de IIS.</span><span class="sxs-lookup"><span data-stu-id="e9332-105">In those cases, you still need to migrate to standards VMs, usually with just Windows and IIS.</span></span>

<span data-ttu-id="e9332-106">Cas non pris en charge dans les conteneurs Windows, à compter de mai 2018 :</span><span class="sxs-lookup"><span data-stu-id="e9332-106">Cases not supported in Windows Containers, as of May 2018:</span></span> 

-   <span data-ttu-id="e9332-107">Microsoft Message Queuing (MSMQ) actuellement est disponible uniquement dans les conteneurs Windows basé sur la version de Windows Server v1803, mais pas dans toutes les autres versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="e9332-107">Microsoft Message Queuing (MSMQ) currently is only available in Windows Containers based on Windows Server v1803 release, but not in any other prior releases.</span></span> 

    -   [<span data-ttu-id="e9332-108">Forum sur la demande UserVoice</span><span class="sxs-lookup"><span data-stu-id="e9332-108">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

    -   [<span data-ttu-id="e9332-109">Forum de discussion</span><span class="sxs-lookup"><span data-stu-id="e9332-109">Discussion forum</span></span>](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

-   <span data-ttu-id="e9332-110">Microsoft Distributed Transaction Coordinator (MSDTC) actuellement n’est pas pris en charge dans les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="e9332-110">Microsoft Distributed Transaction Coordinator (MSDTC) currently is not supported in Windows Containers.</span></span>

    -   [<span data-ttu-id="e9332-111">Problème GitHub</span><span class="sxs-lookup"><span data-stu-id="e9332-111">GitHub issue</span></span>](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

-   <span data-ttu-id="e9332-112">Microsoft Office ne prend actuellement pas en charge les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="e9332-112">Microsoft Office currently does not support containers.</span></span>

    -   [<span data-ttu-id="e9332-113">Forum sur la demande UserVoice</span><span class="sxs-lookup"><span data-stu-id="e9332-113">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

-   <span data-ttu-id="e9332-114">Applications de l’interface utilisateur (applications clientes avec une interface utilisateur) ne sont pas des scénarios pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e9332-114">UI apps (client apps with a visual user interface) are not supported scenarios.</span></span>

-   <span data-ttu-id="e9332-115">Rôles d’infrastructure Windows (DNS, DHCP, DC, NTP, impression, serveur de fichiers, etc. de la page IAM) ne sont pas des scénarios pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e9332-115">Windows infrastructure roles (DNS, DHCP, DC, NTP, PRINT, File server, IAM etc.) are not supported scenarios.</span></span>


<span data-ttu-id="e9332-116">Pour les requêtes à partir de la Communauté et d’autres scénarios non pris en charge, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.</span><span class="sxs-lookup"><span data-stu-id="e9332-116">For additional not-supported scenarios and requests from the community, see the UserVoice forum for Windows Containers: <https://windowsserver.uservoice.com/forums/304624-containers>.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e9332-117">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e9332-117">Additional resources</span></span>

-   <span data-ttu-id="e9332-118">**Machines virtuelles et les conteneurs dans Azure**</span><span class="sxs-lookup"><span data-stu-id="e9332-118">**Virtual machines and containers in Azure**</span></span>

    [https://docs.microsoft.com/azure/virtual-machines/windows/containers](https://docs.microsoft.com/azure/virtual-machines/windows/containers)

>[!div class="step-by-step"]
<span data-ttu-id="e9332-119">[Précédent](deploy-existing-net-apps-as-windows-containers.md)
[Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span><span class="sxs-lookup"><span data-stu-id="e9332-119">[Previous](deploy-existing-net-apps-as-windows-containers.md)
[Next](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span></span>
