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
---
# <a name="when-not-to-deploy-to-windows-containers"></a>Quand ne pas déployer des conteneurs Windows

Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows. Dans ce cas, vous devrez migrer vers les machines virtuelles aux normes, généralement avec Windows et de IIS.

Cas non pris en charge dans les conteneurs Windows, à compter de mai 2018 : 

-   Microsoft Message Queuing (MSMQ) actuellement est disponible uniquement dans les conteneurs Windows basé sur la version de Windows Server v1803, mais pas dans toutes les autres versions antérieures. 

    -   [Forum sur la demande UserVoice](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

    -   [Forum de discussion](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

-   Microsoft Distributed Transaction Coordinator (MSDTC) actuellement n’est pas pris en charge dans les conteneurs Windows.

    -   [Problème GitHub](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

-   Microsoft Office ne prend actuellement pas en charge les conteneurs.

    -   [Forum sur la demande UserVoice](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

-   Applications de l’interface utilisateur (applications clientes avec une interface utilisateur) ne sont pas des scénarios pris en charge.

-   Rôles d’infrastructure Windows (DNS, DHCP, DC, NTP, impression, serveur de fichiers, etc. de la page IAM) ne sont pas des scénarios pris en charge.


Pour les requêtes à partir de la Communauté et d’autres scénarios non pris en charge, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Machines virtuelles et les conteneurs dans Azure**

    [https://docs.microsoft.com/azure/virtual-machines/windows/containers](https://docs.microsoft.com/azure/virtual-machines/windows/containers)

>[!div class="step-by-step"]
[Précédent](deploy-existing-net-apps-as-windows-containers.md)
[Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
