---
title: Moderniser des conteneurs Windows et les Applications .NET existant avec Azure Cloud (2nd edition)
description: Apprenez à de courbes d’élévation et MAJ et moderniser des applications existantes vers le cloud Azure et les conteneurs avec ce livre électronique.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 4/28/2018
ms.openlocfilehash: 10af3a8ce1b9f501d7b646c8d49fcecab29af821
ms.sourcegitcommit: c217b067985905cb21eafc5dd9a83568d7ff4e45
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36314797"
---
# <a name="modernize-existing-net-applications-with-azure-cloud-and-windows-containers-2nd-edition"></a>Moderniser des applications .NET existantes avec Azure cloud et les conteneurs Windows (2nd edition)

![image de couverture](./media/cover.png)

PUBLIÉ PAR  
Microsoft Press et Microsoft DevDiv  
Divisions de Microsoft Corporation  
One Microsoft Way  
Redmond, Washington 98052-6399  

Copyright © 2018 Microsoft Corporation  

Tous droits réservés. Aucune partie du contenu de ce document ne peut être reproduite sous quelque forme ou par quelque moyen que ce soit sans l’autorisation écrite de l’éditeur.

Cet ouvrage est disponible gratuitement sous la forme d’un livre électronique (livre électronique) disponible via plusieurs canaux chez Microsoft, tels que http://dot.net/architecture.

Si vous avez des questions liées à cet ouvrage, envoyez un e-mail à [dotnet-architecture-ebooks-feedback@service.microsoft.com](mailto:dotnet-architecture-ebooks-feedback@service.microsoft.com?subject=Feedback%20for%20.NET%20Container%20&%20Microservices%20Architecture%20book)

Ce document est fourni « en l’état » et exprime les points de vue et les opinions de son auteur. Les vues, les avis et les informations exprimées dans ce livre, y compris les URL et autres références de site Web Internet, peuvent changer sans préavis.

Certains exemples décrits dans ce document ne sont fournis qu’à titre d’illustration et sont purement fictifs. Toute ressemblance ou tout lien avec le monde réel sont purement fortuits et involontaires.

Microsoft et les marques à http://www.microsoft.com sur la page Web « Marques » sont des marques du groupe de sociétés Microsoft. Toutes les autres marques sont la propriété de leurs propriétaires respectifs.

Auteur :
> **Cesar de la Torre**, chef de projet sénior, équipe produit .NET, Microsoft Corp.

Participants et réviseurs :
> **Scott Hunter**, chef de projet directeur partenaire, équipe .NET, Microsoft  
> **Paul Yuknewicz**, chef de projet responsable principal, équipe Visual Studio Tools, Microsoft  
> **Lisa Guthrie**, chef de projet sénior, équipe Visual Studio Tools, Microsoft  
> **Ankit Asthana**, responsable principal de la gestion de projets, équipe .NET, Microsoft  
> **Unai Zorrilla**, développeur en chef, Plain Concepts  
> **Javier Valero**, chef des opérations chez Grupo Solutio  

## <a name="introduction"></a>Introduction

Lorsque vous décidez de moderniser vos applications web ou les services et les déplacer vers le cloud, vous ne sont pas nécessairement de remanier complètement de vos applications. Remaniement d’une application à l’aide d’une approche avancée comme microservices n’est pas toujours une option en raison de restrictions de coût et le temps. Selon le type d’application, remaniement une application également peut-être pas nécessaire. Pour optimiser la rentabilité de la stratégie de migration vers le cloud de votre organisation, il est important de prendre en compte les besoins de votre activité et les exigences de vos applications. Vous devez déterminer :

- Les applications qui requièrent une transformation ou remaniement.

- Les applications qui doivent être modernisées seulement en partie.

- Les applications pouvant faire l’objet d’un lift-and-shift directement dans le cloud.

## <a name="about-this-guide"></a>À propos de ce guide

Ce guide se concentre essentiellement sur modernisation initiale du site web de Microsoft .NET Framework existant ou des applications orientées service, ce qui signifie que l’action de déplacement d’une charge de travail dans un environnement plus récente ou plus modern sans modifier de manière significative le code de l’application et l’architecture de base. 

Ce guide présente également les avantages de la transition de vos applications vers le nuage et partiellement rénovation des applications à l’aide d’un ensemble spécifique de nouvelles technologies et les approches, telles que les conteneurs Windows et les plates-formes de calcul connexes dans Azure prenant en charge des conteneurs Windows.

## <a name="path-to-the-cloud-for-existing-net-applications"></a>Déplacement vers le cloud des applications .NET existantes

En règle générale, les organisations choisissent de passer au cloud pour apporter souplesse et rapidité à leurs applications. Vous pouvez configurer des milliers de serveurs (des machines virtuelles) dans le cloud en quelques minutes, en comparaison aux semaines généralement nécessaires pour configurer des serveurs locaux.

Il n’existe pas de stratégie unique et universelle pour migrer des applications dans le cloud. La bonne stratégie de migration pour vous dépend des besoins et des priorités de votre organisation, ainsi que du type des applications que vous migrez. Les applications ne justifient pas toutes l’investissement nécessaire pour passer à un modèle Paas ([plateforme en tant que service](https://azure.microsoft.com/overview/what-is-paas/)) ou pour développer un modèle d’application [natif pour le cloud](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications). Dans de nombreux cas, vous pouvez adopter une approche progressive ou incrémentielle quand vous investissez dans le déplacement de vos ressources sur le cloud, en fonction des besoins de votre entreprise.

Pour les applications modernes avec la valeur de l’organisation et la souplesse mieux à long terme, vous pouvez bénéficier à partir de l’acquisition de *natif cloud* architectures d’application. Toutefois, pour les applications qui existent ou les composants hérités, la clé est de passer un minimum de temps et de l’argent (aucune modification de code ou de remaniement) lors de leur déplacement vers le cloud, pour profiter des avantages significatifs.

La figure 1-1 montre les voies possibles utilisables quand vous faites passer progressivement des applications .NET existantes dans le cloud.

 ![Voies de modernisation pour les applications et les services .NET existants](./media/image1-1.png)

> **Figure 1-1**. Voies de modernisation pour les applications et les services .NET existants

Chaque approche de la migration présente des avantages différents et est utilisée pour des raisons différentes. Vous pouvez choisir une même approche quand vous migrez des applications vers le cloud, ou choisir certains composants provenant de plusieurs approches. Les applications individuelles ne sont pas limitées à une seule approche ou à un seul état de maturité. Par exemple, une approche hybride courante consiste à avoir certains des composants en local et d’autres composants dans le cloud.

La définition et une brève explication pour chaque niveau de maturité d’application sont les suivants :

**Niveau 1 : Infrastructure de Cloud-prêt** applications : dans cette approche de la migration, vous pouvez simplement migrer ou hébergez vos applications locales actuelles vers une infrastructure en tant que service ([IaaS](https://azure.microsoft.com/overview/what-is-iaas/)) plateforme. Vos applications ont pratiquement la même composition qu’avant, mais vous les déployez désormais sur des machines virtuelles dans le cloud.
Ce type simple de migration est généralement connu dans l’industrie, comme « De courbes d’élévation & Décaler ».

**Niveau 2 : Cloud optimisé** applications : À ce niveau et toujours sans remaniement ou de la modification du code significatif, vous pouvez bénéficier des avantages supplémentaires à partir de votre application en cours d’exécution dans le cloud avec des technologies modernes comme des conteneurs et supplémentaires services gérés par le cloud. Vous améliorez l’agilité de vos applications pour les livrer plus rapidement, en affinant les processus de fonctionnement du développement (DevOps) dans votre entreprise. Pour parvenir à l’aide de technologies telles que les conteneurs Windows, qui est basé sur le moteur Docker. Conteneurs de supprimer la friction provoquée par les dépendances d’application lorsque vous déployez en plusieurs étapes. Dans ce modèle de maturité, vous pouvez déployer des conteneurs sur IaaS ou PaaS lors de l’utilisation des services gérés par le cloud liées aux bases de données, mettre en cache comme un service, la surveillance et le déploiement de l’intégration continue/continue des pipelines de (l’élément de configuration/CD).

Le troisième niveau de maturité est l’objectif ultime dans le cloud, mais il est facultatif pour de nombreuses applications et ne constitue pas l’objet principal de ce guide :

**Niveau 3 : Cloud natif** applications : cette approche de la migration est généralement pilotée par les besoins professionnels et les cibles rénovation vos applications critiques. À ce niveau, vous utilisez des services PaaS pour passer vos applications sur des plateformes informatiques PaaS. Vous implémentez des applications et une architecture de microservices [natives pour le cloud](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) pour faire évoluer les applications avec une agilité à long terme et pour les adapter à de nouvelles limites. Ce type de modernisation nécessite généralement une architecture spécifique pour le cloud. Du nouveau code doit souvent être écrit, en particulier quand vous passez à des modèles d’application natifs pour le cloud et basés sur des microservices. Cette approche peut vous aider à profiter d’avantages difficiles à obtenir dans votre environnement applicatif monolithique et local.

Le tableau 1-1 décrit les principaux avantages et les raisons de choisir chaque approche de migration ou de modernisation.

| **Prêt pour l’infrastructure cloud** <br /> *Lift-and-shift* | **Optimisée pour le cloud** <br /> *Moderniser* | **Cloud en mode natif** <br /> *Moderniser, remanier et réécrire* |
|---|---|---|
| **Cible informatique de l’application** |
| Applications déployées sur des machines virtuelles dans Azure | Monolithiques ou des applications multicouches déployées dans Azure App Service, Instance de conteneur Azure (ACI), machines virtuelles avec les conteneurs, Azure Service Fabric ou AKS (Service de Kubernetes Azure) | Microservices en conteneur sur Azure Kubernetes Service (AKS), Service Fabric et/ou microservices sans serveur basé sur les fonctions d’Azure. |
| **Cible de données** |
| SQL ou n’importe quelle base de données relationnelle sur une machine virtuelle | L’Instance gérée de la base de données Azure SQL ou une autre base de données managé dans le cloud. | Bases de données de granularité une amende par microservice, en fonction de la base de données SQL Azure, Azure Cosmos DB ou une autre base de données managé dans le cloud |
| **Avantages**|
| <li>Aucun code remaniement, aucune nouvelle <li> Moins de travail pour une migration rapide <li> Plus petit dénominateur commun pris en charge dans Azure <li> Garanties de disponibilité de base <li> Après être passé au cloud, il est plus facile de moderniser encore plus | <li> Aucun remaniement <li> Modifications de code/configuration minimale <li> Déploiement amélioré et meilleure agilité de DevOps pour la production de nouvelles versions grâce aux conteneurs <li> Densité accrue et coûts de déploiement inférieurs <li> Portabilité des applications et des dépendances <li> Flexibilité des cibles de l’ordinateur hôte : PaaS approches ou IaaS | <li> Architecte pour le cloud, vous obtenez les avantages du cloud mais le nouveau code est nécessaire. <li> Approches natives pour le cloud avec des microservices <li> Applications modernes critiques, résilientes de cloud hyper évolutive <li> Services entièrement gérés <li> Optimisé pour la mise à l’échelle <li> Optimisé pour une agilité autonome par sous-système <li> S’appuyant sur le déploiement et sur DevOps |
| **Difficultés éventuelles** |
| <li> Valeur cloud inférieure, autre que la variation des dépenses d’exploitation ou la fermeture de centres de données <li> Peu est géré : aucun système d’exploitation ou la mise à jour corrective d’intergiciel (middleware) ; peut utiliser des solutions d’infrastructure, tels que Terraform, Spinnaker ou Puppet | <li> Containerizing est une étape supplémentaire dans la courbe d’apprentissage pour les développeurs et des opérations informatiques <li> DevOps et l’élément de configuration/CD pipelines est généralement « doit » de cette approche. Si ce n’est pas actuellement présent dans la culture de l’organisation, il peut être un défi supplémentaire| <li> Architecture de cloud des applications natives et les architectures de microservice et généralement requiert significatif code de refactorisation ou réécriture lorsque rénovation (temps accrue et budget) <li> DevOps et l’élément de configuration/CD pipelines est généralement « doit » de cette approche. Si ce n’est pas actuellement présent dans la culture de l’organisation, il peut être un défi supplémentaire|
> **Tableau 1-1.** Avantages et difficultés éventuelles des parcours de modernisation pour les applications et les services .NET existants

### <a name="key-technologies-and-architectures-by-maturity-level"></a>Technologies et architectures principales par niveau de maturité

Au départ, les applications .NET Framework démarraient avec le .NET Framework version 1.0, qui a été publié fin 2001. Ensuite, les entreprises sont passées à des versions plus récentes (comme 2.0, 3.5 et .NET 4.x). La plupart de ces applications exécuté sur Windows Server et Internet Information Server (IIS) et utilisé une base de données relationnel, telles que SQL Server, Oracle, MySQL ou n’importe quel autre SGBDR.

La plupart des applications .NET existantes sont probablement basées sur le .NET Framework 4.x, ou même sur le .NET Framework 3.5, et elles utilisent des frameworks web, comme ASP.NET MVC, ASP.NET Web Forms, ASP.NET Web API, WCF (Windows Communication Foundation), ASP.NET SignalR et ASP.NET Web Pages. Ces technologies .NET Framework répandues dépendent de Windows. Cette dépendance est importante à prendre en compte si vous effectuez simplement une migration d’applications héritées et que vous voulez apporter le moins de modifications possible à votre infrastructure d’application.

La figure 1-2 montre les technologies et les styles d’architecture principaux utilisés pour chacun des trois niveaux de maturité cloud :

![Technologies principales pour chaque niveau de maturité pour la modernisation d’applications web .NET existantes](./media/image1-2.png)

> **Figure 1-2.** Technologies principales pour chaque niveau de maturité pour la modernisation d’applications web .NET existantes

La figure 1-2 met en évidence les scénarios les plus courants, mais de nombreuses variations hybrides et mixtes sont possibles concernant l’architecture. Par exemple, les modèles de maturité s’appliquent non seulement aux architectures monolithiques dans les applications web existantes, mais aussi à l’orientation service, au multiniveau et à d’autres variations du style d’architecture. Du focus ou pourcentage sur le type d’un ou une autre architecture et les technologies connexes plus élevée détermine le niveau de maturité global de vos applications.

Chaque niveau de maturité du processus de modernisation est associé aux technologies et aux approches principales suivantes :

- **Prêt à l’Infrastructure de cloud computing** (réhébergement ou basic de courbes d’élévation & Décaler) : dans un premier temps, de nombreuses organisations souhaitent simplement exécuter rapidement une stratégie de migration de cloud. Dans ce cas, les applications sont réhébergées. La plus grande partie du réhébergement peut être automatisée avec [Azure Migrate](https://aka.ms/azuremigrate), service qui fournit de l’aide, des insights et les mécanismes nécessaires pour vous aider à migrer vers Azure, basé sur des outils cloud comme [Azure Site Recovery](https://azure.microsoft.com/services/site-recovery/) et [Azure Database Migration Service](https://azure.microsoft.com/campaigns/database-migration/). Vous pouvez également configurer manuellement le réhébergement, ce qui vous permet de découvrir des détails d’infrastructure sur vos ressources quand vous déplacez des applications héritées dans le cloud. Par exemple, vous pouvez déplacer vos applications pour ordinateurs virtuels dans Azure avec peu de modification probablement avec uniquement les modifications de configuration mineures. La mise en réseau est dans ce cas similaire à un environnement local, en particulier si vous créez des réseaux virtuels dans Azure.

- **Optimisée pour le cloud** (Services de gestion et les conteneurs Windows) : ce modèle est sur l’établissement de certaines optimisations importantes pour le déploiement d’obtenir certains des avantages significatifs à partir du cloud, sans modifier l’architecture de l’application. Le principal est ici d’ajouter la prise en charge des [conteneurs Windows](https://docs.microsoft.com/virtualization/windowscontainers/about/) à vos applications .NET Framework existantes. Cette étape importante (CONTENEURISATION des données) ne requiert pas toucher au code, afin de l’effort de courbes d’élévation et MAJ global est faible. Vous pouvez utiliser des outils comme [Image2Docker](https://github.com/docker/communitytools-image2docker-win) ou Visual Studio, avec ses outils pour [Docker](https://www.docker.com/). Visual Studio choisit automatiquement des valeurs par défaut adaptées pour les applications ASP.NET et les images de conteneurs Windows. Ces outils permettent à la fois une boucle interne rapide et une voie rapide pour placer les conteneurs dans Azure. Votre agilité est améliorée quand vous déployez sur plusieurs environnements. Déplacement de la production, vous pouvez ensuite déployer vos conteneurs Windows à [l’application Web Azure pour les conteneurs](https://azure.microsoft.com/en-us/services/app-service/containers/), [Azure conteneur Instances (ACI) et les machines virtuelles de Azure avec Windows Server 2016 et les conteneurs si vous préférez une approche IaaS. Pour les applications de conteneur multi légèrement plus complexes, en orchestrators comme [Azure Service Fabric](https://azure.microsoft.com/services/service-fabric/) ou [Azure Kubernetes Service (AKS/ACS)](https://azure.microsoft.com/en-us/services/container-service/). Au cours de cette modernisation initiale, vous pouvez également ajouter des ressources provenant du cloud, comme la surveillance avec des outils comme [Azure Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview), des pipelines d’intégration continue/de déploiement continu pour les cycles de vie de votre application avec [Visual Studio Team Services](https://visualstudio.microsoft.com/team-services/), et de nombreux autres services de ressources de données qui sont disponibles dans Azure. Par exemple, vous pouvez modifier une application web monolithique qui a été développée à l’origine avec les composants classiques [ASP.NET Web Forms](https://www.asp.net/web-forms) ou [ASP.NET MVC](https://www.asp.net/mvc), mais vous la déployez maintenant en utilisant des conteneurs Windows. Quand vous utilisez des conteneurs Windows, vous devez également migrer vos données vers une base de données qui se trouve dans [Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/), le tout sans modifier l’architecture principale de votre application.

- **Cloud natif**: introduit, vous devez tenir compte architecture [natif cloud](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) lorsque vous ciblez des applications volumineuses et complexes avec plusieurs équipes de développement indépendants travaillant sur les applications microservices différents qui peuvent être développés et déployés de façon autonome. En outre, en raison d’une évolutivité granularized et indépendante par microservice. Ces approches architecturales sont confrontés à des défis très importants et la complexité, mais peuvent être considérablement simplifiés à l’aide de cloud PaaS et orchestrators comme [Azure Kubernetes Service (AKS/ACS)](https://azure.microsoft.com/en-us/services/container-service/) (géré Kubernetes), [Service Azure L’infrastructure, et [Azure fonctions](https://azure.microsoft.com/services/functions/) une approche sans serveur. Toutes ces approches (comme microservices et sans serveur) requièrent en général l’architecture pour le cloud et d’écrire un nouveau code, code qui est adapté aux plateformes PaaS spécifiques ou le code qui s’aligne avec des architectures spécifiques, telles que microservices.

La figure 1-3 montre les technologies internes que vous pouvez utiliser pour chaque niveau de maturité :

![Technologies internes pour chaque niveau de maturité de modernisation](./media/image1-3.png)

> **Figure 1-3.** Technologies internes pour chaque niveau de maturité de modernisation

## <a name="lift-and-shift-scenario"></a>Scénario de courbes d’élévation et MAJ.

Pour les migrations de type lift-and-shift, gardez à l’esprit que vous pouvez utiliser de nombreuses variations de lift-and-shift différentes dans vos scénarios d’application. Si vous réhébergez seulement votre application, vous pouvez avoir un scénario semblable à celui illustré dans la Figure 1-4, où vous utilisez des machines virtuelles dans le cloud seulement pour votre application et pour votre serveur de base de données.

![Exemple de scénario IaaS pur dans le cloud](./media/image1-4.png)

> **Figure 1-4**. Exemple de scénario IaaS pur dans le cloud

## <a name="modernization-scenarios"></a>Scénarios de modernisation

Pour les scénarios de modernisation, vous pouvez avoir une application d’optimisée pour le Cloud pure qui utilise des éléments uniquement à partir de ce niveau de maturité. Ou bien, vous pouvez avoir une application état intermédiaire avec des éléments d’Infrastructure prête pour le Cloud et d’autres éléments à partir des tables optimisées en nuage (un « choisir » ou un modèle mixte), comme dans la Figure 1-5.

![Exemple de scénario « par sélection », avec une base de données sur IaaS, DevOps et des ressources de mise en conteneur](./media/image1-5.png)

> **Figure 1-5.** Exemple de scénario « par sélection », avec une base de données sur IaaS, DevOps et des ressources de mise en conteneur

Ensuite, si le scénario idéal pour de nombreuses applications .NET Framework existantes à migrer, vous pouvez migrer vers une application optimisée pour le Cloud, pour bénéficier des avantages significatifs en peu de travail. Cette approche définit également pour le Cloud en mode natif comme une évolution ultérieure possible. La figure 1-6 en montre un exemple.

![Exemple de scénario optimisée pour le Cloud des applications, avec les conteneurs Windows et de services gérés](./media/image1-6.png)

> **Figure 1-6.** Exemple de scénario optimisée pour le Cloud des applications, avec les conteneurs Windows et de services gérés

Va encore plus loin, vous pouviez étendre votre application existante optimisée pour le Cloud en ajoutant quelques microservices pour des scénarios spécifiques. Cela serait vous déplacer partiellement au niveau du modèle de Cloud en mode natif, ce qui n’est pas l’objectif principal du présent guide.


## <a name="what-this-guide-does-not-cover"></a>Sujets non abordés dans ce guide

Ce guide couvre un sous-ensemble spécifique des exemples de scénarios, comme le montre la figure 1-7. Ce guide se concentre uniquement sur les scénarios de courbes d’élévation et MAJ et enfin, sur le modèle optimisée pour le Cloud. Dans le modèle optimisée pour le Cloud, une application .NET Framework est modernisée à l’aide de conteneurs Windows, ainsi que des composants supplémentaires telles que la surveillance et l’élément de configuration/CD de pipelines. Chaque composant est fondamental pour permettre un déploiement plus rapide et agile des applications dans le cloud.

![Cloud en mode natif n’est pas abordé dans ce guide](./media/image1-7.png)

> **Figure 1-7.** Cloud en mode natif n’est pas abordé dans ce guide

L’objet principal de ce guide est spécifique. Il vous indique le chemin d’accès que vous pouvez prendre pour atteindre un MAJ de vos applications .NET existantes et de courbes d’élévation remaniement et sans aucune modification de code. Pour finir, il vous montre comment rendre votre application optimisée pour le Cloud.

Ce guide ne vous montrent comment créer des applications de Cloud en mode natif, par exemple, l’évolution vers une architecture microservices. De remanier vos applications ou pour créer des applications nouvelles qui sont basées sur microservices, consultez le livre électronique [.NET Microservices : Architecture pour les applications .NET en conteneur](https://aka.ms/microservicesebook).

### <a name="additional-resources"></a>Ressources supplémentaires

- **Placées dans des conteneurs Docker cycle de vie application avec la plate-forme Microsoft et les outils** (livre électronique téléchargeable) : [*https://aka.ms/dockerlifecycleebook*](https://aka.ms/dockerlifecycleebook)

- **.NET Microservices : Architecture pour les applications .NET en conteneur** (livre électronique téléchargeable) : [*https://aka.ms/microservicesebook*](https://aka.ms/microservicesebook)

- **Architecture des applications web avec ASP.NET Core et Azure** (livre électronique téléchargeable) : [*https://aka.ms/webappebook*](https://aka.ms/webappebook)

## <a name="who-should-use-this-guide"></a>Public visé par ce guide

Ce guide a été écrit pour les développeurs et aux architectes de solutions qui souhaitent de moderniser des applications web ASP.NET existantes ou les services WCF qui sont basées sur le .NET Framework, pour une plus grande souplesse dans la copie et la libération des applications.

Ce guide peut être utile également si vous êtes décideur informatique, par exemple architecte d’entreprise ou responsable du développement, et souhaitez seulement une vue d’ensemble des bénéfices que vous pouvez obtenir en utilisant des conteneurs Windows et en déployant sur le cloud si vous utilisez Microsoft Azure.

## <a name="how-to-use-this-guide"></a>Comment utiliser ce guide

Ce guide répond à la question « pourquoi » : pourquoi il peut être souhaitable de moderniser vos applications existantes. Il explique aussi quels sont les bénéfices procurés par l’utilisation des conteneurs Windows quand vous déplacez vos applications dans le cloud. Le contenu des premiers chapitres du guide est conçu pour les architectes et les décideurs informatiques qui veulent une vue d’ensemble, mais qui n’ont pas besoin d’informations techniques détaillées sur le processus d’implémentation.

Le dernier chapitre de ce guide contient plusieurs procédures pas à pas centrées sur des scénarios de déploiement spécifiques. Ce guide propose des versions plus courtes des procédures pas à pas, pour résumer les scénarios et de mettre en évidence leurs avantages. Les procédures pas à pas complètes détaillent la configuration et l’implémentation. Elles sont publiées sous la forme d’un ensemble de [billets wiki](https://github.com/dotnet-architecture/eShopModernizing/wiki) dans le [dépôt GitHub](https://github.com/dotnet-architecture/eShopModernizing) où vous trouvez aussi des exemples d’applications associées (présentées dans la section suivante). Le dernier chapitre et les procédures pas à pas du wiki sur GitHub sont plus intéressants pour les développeurs et les architectes qui veulent connaître les détails d’implémentation.

## <a name="sample-apps-for-modernizing-legacy-apps-eshopmodernizing"></a>Exemples d’applications pour la modernisation d’applications héritées : eShopModernizing

Le dépôt [eShopModernizing](https://github.com/dotnet-architecture/eShopModernizing) sur GitHub contient deux exemples d’applications qui simulent des applications web monolithiques héritées. Une application web est développée à l’aide d’ASP.NET MVC ; la deuxième application web est développée à l’aide de Web Forms ASP.NET et l’application de tiers est une application multicouche avec une application de bureau client WinForms consomme un principal de service WCF. Toutes ces applications sont basées sur le .NET Framework traditionnelles. Ces exemples d’applications n’utilisent pas .NET Core ou ASP.NET Core, car elles sont supposées être des applications .NET Framework existantes/héritées à moderniser.

Ces exemples d’applications ont une deuxième version, avec le code et modernisé, et qui sont assez simple. La différence la plus importante entre les versions des applications est que leur seconde version utilise les conteneurs Windows comme choix de déploiement. Quelques ajouts ont été apportés aux secondes versions, comme des objets blob Stockage Azure pour la gestion des images, Azure Active Directory pour la gestion de la sécurité et Azure Application Insights pour la surveillance et l’audit des applications.

## <a name="send-your-feedback"></a>Envoyez vos commentaires

Ce guide a été écrit pour vous aider à comprendre les options d’amélioration et de rénovation des applications web .NET existantes. Le guide et les exemples d’applications associés sont en constante évolution. Vos commentaires sont Bienvenue ! Si vous avez des commentaires à formuler sur la façon dont ce guide peut être amélioré, envoyez-les à l’adresse : [dotnet-architecture-ebooks-feedback@service.microsoft.com](mailto:dotnet-architecture-ebooks-feedback@service.microsoft.com?subject=Feedback%20for%20.NET%20Container%20&%20Microservices%20Architecture%20book).

>[!div class="step-by-step"]
[Next](lift-and-shift-existing-apps-azure-iaas.md)
