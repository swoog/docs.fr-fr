---
title: Moment de déployer des conteneurs Windows aux ordinateurs virtuels de Azure (IaaS cloud)
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Moment de déployer des conteneurs Windows aux ordinateurs virtuels de Azure (IaaS cloud)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 7472745577f414062b460fd71ab45bae85d7a62e
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
ms.locfileid: "33958019"
---
# <a name="when-to-deploy-windows-containers-to-azure-vms-iaas-cloud"></a>Moment de déployer des conteneurs Windows aux ordinateurs virtuels de Azure (IaaS cloud)

Si votre organisation est à l’aide de machines virtuelles Azure, même si vous utilisez également des conteneurs Windows, vous travaillez toujours avec IaaS. Cela signifie que qui traite des opérations d’infrastructure, des correctifs de système d’exploitation de la machine virtuelle et complexité de l’infrastructure pour les applications hautement évolutives lorsque vous avez besoin déployer sur plusieurs machines virtuelles dans une infrastructure à charge équilibrée. Les principaux scénarios pour l’utilisation de conteneurs Windows dans une machine virtuelle Azure sont :

-   **Environnement de développement/test**: machine virtuelle de A dans le cloud est idéale pour le développement et de test dans le cloud. Vous pouvez rapidement créer ou arrêt de l’environnement en fonction des besoins.

-   **Évolutivité de petite et moyenne taille doit**: dans les scénarios où vous devrez peut-être que quelques exemples d’ordinateurs virtuels pour votre environnement de production, la gestion d’un petit nombre de machines virtuelles peut être économique jusqu'à ce que vous pouvez déplacer vers des environnements PaaS plus avancées, telles qu’orchestrators.

-   **Environnement de production avec les outils de déploiement existants**: vous pouvez déplacer à partir d’un environnement local dans lequel vous avez investi dans les outils pour effectuer des déploiements complexes à des machines virtuelles ou les serveurs de récupération complète (comme Puppet ou outils similaires). Pour déplacer vers le cloud avec des modifications mineures par rapport aux procédures de déploiement environnement de production, vous pourrez continuer à utiliser ces outils pour déployer des machines virtuelles Azure. Toutefois, vous souhaiterez utiliser des conteneurs Windows en tant que l’unité de déploiement pour améliorer l’expérience de déploiement.

>[!div class="step-by-step"]
[Précédent](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
[Suivant](when-to-deploy-windows-containers-to-azure-container-instances-ACI.md)
