---
title: Quand ne pas déployer sur des conteneurs Windows
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Quand ne pas déployer sur des conteneurs Windows
ms.date: 04/28/2018
ms.openlocfilehash: 65e793b846b495e9a1be6db9ddfa38bbf0d49445
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65638895"
---
# <a name="when-not-to-deploy-to-windows-containers"></a>Quand ne pas déployer sur des conteneurs Windows

Certaines technologies de Windows ne sont pas pris en charge par les conteneurs Windows. Dans ce cas, vous devez toujours migrer vers les machines virtuelles aux normes, généralement avec simplement Windows et IIS.

Cas non pris en charge dans des conteneurs Windows, à compter de mai 2018 :

- Microsoft Message Queuing (MSMQ) est actuellement uniquement disponible dans les conteneurs Windows basés sur la version de Windows Server v1803, mais pas dans toutes les versions antérieures.

  - [Forum de demande de UserVoice](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/15719031-create-base-container-image-with-msmq-server)

  - [Forum de discussion](https://social.msdn.microsoft.com/Forums/bce99a7d-aa60-44fa-a348-450855650810/msmqserver-is-it-supported?forum=windowscontainers)

- Microsoft Distributed Transaction Coordinator (MSDTC) actuellement n’est pas pris en charge dans les conteneurs Windows.

  - [Problème GitHub](https://github.com/MicrosoftDocs/Virtualization-Documentation/issues/494)

- Microsoft Office ne prend actuellement pas en charge les conteneurs.

  - [Forum de demande de UserVoice](https://windowsserver.uservoice.com/forums/304624-containers/suggestions/19686220-provide-office-support-for-containers)

- Applications d’interface utilisateur (applications clientes avec une interface utilisateur visuelle) ne sont pas prises en charge de scénarios.

- Rôles d’infrastructure Windows (DNS, DHCP, DC, NTP, impression, serveur de fichiers, etc. IAM) ne sont pas des scénarios pris en charge.

Pour des scénarios supplémentaires non prise en charge et les demandes à partir de la Communauté, consultez le forum UserVoice pour les conteneurs Windows : <https://windowsserver.uservoice.com/forums/304624-containers>.

### <a name="additional-resources"></a>Ressources supplémentaires

- **Machines virtuelles et conteneurs dans Azure**

    <https://azure.microsoft.com/overview/containers/>

> [!div class="step-by-step"]
> [Précédent](deploy-existing-net-apps-as-windows-containers.md)
> [Suivant](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
