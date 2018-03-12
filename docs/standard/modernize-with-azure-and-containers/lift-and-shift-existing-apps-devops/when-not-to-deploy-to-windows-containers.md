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
# <a name="when-not-to-deploy-to-windows-containers"></a>Quand ne pas déployer des conteneurs Windows

Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows. Dans ce cas, vous devrez migrer vers les machines virtuelles aux normes, généralement avec Windows et de IIS.

Cas non pris en charge dans les conteneurs Windows, à compter de mid 2017 :

-   Microsoft Message Queuing (MSMQ) actuellement n’est pas pris en charge dans les conteneurs Windows.

    -   [Forum sur la demande UserVoice](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

    -   [Forum de discussion](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

-   Microsoft Distributed Transaction Coordinator (MSDTC) en n'est pas pris en charge dans les conteneurs Windows

    -   [Problème GitHub](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

-   Microsoft Office ne prend actuellement pas en charge les conteneurs

    -   [Forum sur la demande UserVoice](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

Pour les requêtes à partir de la Communauté et d’autres scénarios non pris en charge, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Machines virtuelles et les conteneurs dans Azure**

    [https://docs.microsoft.com/azure/virtual-machines/windows/containers](https://docs.microsoft.com/azure/virtual-machines/windows/containers)

>[!div class="step-by-step"]
[Précédent](deploy-existing-net-apps-as-windows-containers.md)
[Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
