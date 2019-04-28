---
title: Quand ne pas déployer sur des conteneurs Windows
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Quand ne pas déployer sur des conteneurs Windows
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: c5d8f50c7b9967eba0ec01c9e864a02b6a3b201a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012007"
---
# <a name="when-not-to-deploy-to-windows-containers"></a><span data-ttu-id="f7655-103">Quand ne pas déployer sur des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="f7655-103">When not to deploy to Windows Containers</span></span>

<span data-ttu-id="f7655-104">Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="f7655-104">Some Windows technologies are not supported by Windows Containers.</span></span> <span data-ttu-id="f7655-105">Dans ce cas, vous devez toujours migrer vers les machines virtuelles aux normes, généralement avec simplement Windows et IIS.</span><span class="sxs-lookup"><span data-stu-id="f7655-105">In those cases, you still need to migrate to standards VMs, usually with just Windows and IIS.</span></span>

<span data-ttu-id="f7655-106">Cas non pris en charge dans des conteneurs Windows, à compter de mai 2018 :</span><span class="sxs-lookup"><span data-stu-id="f7655-106">Cases not supported in Windows Containers, as of May 2018:</span></span>

- <span data-ttu-id="f7655-107">Microsoft Message Queuing (MSMQ) est actuellement uniquement disponible dans les conteneurs Windows basés sur la version de Windows Server v1803, mais pas dans toutes les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="f7655-107">Microsoft Message Queuing (MSMQ) currently is only available in Windows Containers based on Windows Server v1803 release, but not in any other prior releases.</span></span>

  - [<span data-ttu-id="f7655-108">Forum de demande de UserVoice</span><span class="sxs-lookup"><span data-stu-id="f7655-108">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

  - [<span data-ttu-id="f7655-109">Forum de discussion</span><span class="sxs-lookup"><span data-stu-id="f7655-109">Discussion forum</span></span>](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

- <span data-ttu-id="f7655-110">Microsoft Distributed Transaction Coordinator (MSDTC) actuellement n’est pas pris en charge dans les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="f7655-110">Microsoft Distributed Transaction Coordinator (MSDTC) currently is not supported in Windows Containers.</span></span>

  - [<span data-ttu-id="f7655-111">Problème GitHub</span><span class="sxs-lookup"><span data-stu-id="f7655-111">GitHub issue</span></span>](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

- <span data-ttu-id="f7655-112">Microsoft Office ne prend actuellement pas en charge les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="f7655-112">Microsoft Office currently does not support containers.</span></span>

  - [<span data-ttu-id="f7655-113">Forum de demande de UserVoice</span><span class="sxs-lookup"><span data-stu-id="f7655-113">UserVoice request forum</span></span>](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

- <span data-ttu-id="f7655-114">Applications d’interface utilisateur (applications clientes avec une interface utilisateur visuelle) ne sont pas prises en charge de scénarios.</span><span class="sxs-lookup"><span data-stu-id="f7655-114">UI apps (client apps with a visual user interface) are not supported scenarios.</span></span>

- <span data-ttu-id="f7655-115">Rôles d’infrastructure Windows (DNS, DHCP, DC, NTP, impression, serveur de fichiers, etc. IAM) ne sont pas des scénarios pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f7655-115">Windows infrastructure roles (DNS, DHCP, DC, NTP, PRINT, File server, IAM etc.) are not supported scenarios.</span></span>

<span data-ttu-id="f7655-116">Pour des scénarios supplémentaires non prise en charge et les demandes à partir de la Communauté, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.</span><span class="sxs-lookup"><span data-stu-id="f7655-116">For additional not-supported scenarios and requests from the community, see the UserVoice forum for Windows Containers: <https://windowsserver.uservoice.com/forums/304624-containers>.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f7655-117">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f7655-117">Additional resources</span></span>

- <span data-ttu-id="f7655-118">**Machines virtuelles et conteneurs dans Azure**</span><span class="sxs-lookup"><span data-stu-id="f7655-118">**Virtual machines and containers in Azure**</span></span>

    <https://azure.microsoft.com/overview/containers/>

> [!div class="step-by-step"]
> <span data-ttu-id="f7655-119">[Précédent](deploy-existing-net-apps-as-windows-containers.md)
> [Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span><span class="sxs-lookup"><span data-stu-id="f7655-119">[Previous](deploy-existing-net-apps-as-windows-containers.md)
[Next](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)</span></span>
