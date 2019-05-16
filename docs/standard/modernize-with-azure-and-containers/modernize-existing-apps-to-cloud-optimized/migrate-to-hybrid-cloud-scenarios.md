---
title: Scénarios de migration vers le cloud hybride
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Migrer vers les scénarios de cloud hybride
ms.date: 04/30/2018
ms.openlocfilehash: 04c618681c61f5584e641e0a4735e1261ab34fa3
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65643719"
---
# <a name="migrate-to-hybrid-cloud-scenarios"></a>Scénarios de migration vers le cloud hybride

Certaines organisations et les entreprises ne peuvent pas migrer certaines de leurs applications à des clouds publics comme Microsoft Azure ou n’importe quel autre cloud public en raison des réglementations ou leurs propres stratégies. Toutefois, il est probable que n’importe quelle organisation peut bénéficier d’avoir certaines de leurs applications dans le cloud public et d’autres applications en local. Mais un environnement mixte peut conduire à l’excès de complexité dans les environnements en raison des différentes plateformes et technologies utilisées dans des clouds publics et les environnements locaux.

Microsoft fournit la meilleure solution de cloud hybride, un dans lequel vous pouvez optimiser vos actifs existants en local et dans le cloud public, alors que vous garantir la cohérence dans un cloud hybride Azure. Vous pouvez optimiser les compétences et bénéficiez d’une approche flexible et unifiée pour la création d’applications pouvant s’exécuter dans le cloud ou sur site, grâce à Azure Stack (local) et Azure (cloud public).

Lorsqu’il s’agit à la sécurité, vous pouvez centraliser la gestion et la sécurité dans votre cloud hybride. Vous pouvez obtenir un contrôle sur toutes les ressources, à partir de votre centre de données dans le cloud, en fournissant l’authentification unique au niveau local et les applications cloud. Vous y parvenir en étendant Active Directory à un cloud hybride et à l’aide de la gestion des identités.

Enfin, vous pouvez distribuer analyser les données en toute transparence, utiliser les mêmes langages de requête pour les ressources cloud et locales et s’appliquent aux analytique et l’apprentissage profond dans Azure pour enrichir vos données, quelle que soit sa source.

## <a name="azure-stack"></a>Azure Stack

Azure Stack est une plateforme de cloud hybride qui vous permet de fournir des services Azure à partir du centre de données de votre organisation. Azure Stack est conçu pour prendre en charge de nouvelles options pour vos applications modernes dans des scénarios clés, telles qu’edge et les environnements non connectés ou les exigences de sécurité et de conformité spécifiques de réunion.

Figure 4-13 montre une vue d’ensemble de la plateforme de cloud hybride true proposées par Microsoft.

![Plateforme de cloud hybride de Microsoft avec Azure Stack et Azure](./media/image13.jpg)

> **Figure 4-13.** Plateforme de cloud hybride de Microsoft avec Azure Stack et Azure

Azure Stack est proposé en deux options de déploiement, à vos besoins :

- Systèmes intégrés Azure Stack

- Kit de développement Azure Stack

### <a name="azure-stack-integrated-systems"></a>Systèmes intégrés Azure Stack

Systèmes intégrés Azure Stack sont proposées grâce à un partenariat de partenaires matériels et de Microsoft. Le partenariat crée une solution qui offre l’innovation cloud-à un rythme qui est équilibrée et simplicité de gestion. Car Azure Stack est proposé comme un système intégré de matériels et logiciels, vous obtenez la quantité exacte de flexibilité et de contrôle, tout en adoptant toujours l’innovation à partir du cloud. Systèmes intégrés Azure Stack taille comprise entre 4 à 12 nœuds et sont pris en charge conjointement par le fournisseur de matériel partenaire et Microsoft. Utiliser des systèmes intégrés Azure Stack pour implémenter les nouveaux scénarios pour vos charges de travail de production.

### <a name="azure-stack-development-kit"></a>Kit de développement Azure Stack

Kit de développement Microsoft Azure Stack est un déploiement à nœud unique d’Azure Stack, que vous pouvez utiliser pour évaluer et d’en savoir plus sur Azure Stack. Vous pouvez également utiliser le Kit de développement Azure Stack comme environnement de développement, où vous pouvez développer à l’aide des API et des outils qui sont compatibles avec Azure. Kit de développement Azure Stack n’est pas destiné à être utilisé comme un environnement de production.

### <a name="additional-resources"></a>Ressources supplémentaires

- **Cloud hybride Azure**

    <https://azure.microsoft.com/overview/hybrid-cloud/>

- **Azure Stack**

    <https://azure.microsoft.com/overview/azure-stack/>

- **Comptes de Service de Active Directory pour les conteneurs Windows**

    <https://docs.microsoft.com/virtualization/windowscontainers/manage-containers/manage-serviceaccounts>

- **Créer un conteneur avec prise en charge d’Active Directory**

    <https://blogs.msdn.microsoft.com/containerstuff/2017/01/30/create-a-container-with-active-directory-support/>

- **Licences Azure Hybrid Benefit**

    <https://azure.microsoft.com/pricing/hybrid-benefit/>

>[!div class="step-by-step"]
>[Précédent](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)
>[Suivant](../walkthroughs-technical-get-started-overview.md)
