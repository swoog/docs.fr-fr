---
title: Migration des services Web ASP.NET vers WCF
ms.date: 03/30/2017
ms.assetid: 1adbb931-f0b1-47f3-9caf-169e4edc9907
ms.openlocfilehash: 7d43c66952d17a91e38ae1b086478b9416321b8a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="migrating-aspnet-web-services-to-wcf"></a>Migration des services Web ASP.NET vers WCF
ASP.NET fournit des bibliothèques de classes .NET Framework et des outils permettant de générer des services Web, ainsi que des fonctionnalités d'hébergement des services dans les services IIS (Internet Information Services). Windows Communication Foundation (WCF) fournit des bibliothèques de classes .NET Framework, les outils et les services d’hébergement pour l’activation des entités logicielles pour communiquer à l’aide de tous les protocoles, y compris ceux utilisés par les services Web.  Migration des Services Web ASP.NET vers WCF permet à vos applications tirer parti des nouvelles fonctionnalités et améliorations qui sont uniques à WCF.  
  
 WCF offre plusieurs avantages importants par rapport aux services Web ASP.NET. Outils des services Web ASP.NET sont uniquement pour la création de services Web, WCF fournit des outils qui peuvent être utilisés lorsque les entités logicielles doivent être effectuées pour communiquer avec un autre. Cela réduira le nombre de technologies que les développeurs sont tenus de connaître pour s'adapter aux différents scénarios de communication logicielle, ce qui, en conséquence, réduira le coût des ressources de développement logiciel, ainsi que le délai de réalisation des projets de développement logiciel.  
  
 Même pour les projets de développement de services Web, WCF prend en charge plusieurs protocoles de service Web à la prise en charge des services Web ASP.NET. Ces protocoles supplémentaires offrent des solutions plus sophistiquées impliquant, entre autres, des transactions et des sessions fiables.  
  
 WCF prend en charge plusieurs protocoles de transport de messages que les services Web ASP.NET. Les services Web ASP.NET prennent uniquement en charge l'envoi de messages à l'aide du protocole HTTP (Hypertext Transfer Protocol). WCF prend en charge l’envoi de messages à l’aide de HTTP, ainsi que le protocole TCP (Transmission Control), canaux nommés et Microsoft Message Queuing (MSMQ). Plus important, WCF peut être étendu pour prendre en charge d’autres protocoles de transport. Par conséquent, les logiciels développés à l’aide de WCF peuvent être adapté pour fonctionner avec une gamme plus vaste d’autres logiciels, augmentant ainsi le retour potentiel sur investissement.  
  
 WCF fournit beaucoup plus riches fonctionnalités pour le déploiement et la gestion des applications et services Web ASP.NET. Outre un système de configuration, dont il dispose également ASP.NET, WCF offre un éditeur de configuration, le suivi des activités des expéditeurs aux récepteurs et via n’importe quel nombre d’intermédiaires, une visionneuse de trace, journalisation des messages, un grand nombre de compteurs de performance, et prise en charge de Windows Management Instrumentation.  
  
 Étant donné les avantages potentiels de WCF par rapport à ASP.NET Web services, si vous utilisez ou envisagez d’utiliser les services Web ASP.NET que vous disposez de plusieurs options :  
  
-   Continuer à utiliser les services Web ASP.NET et renoncer aux avantages offerts par WCF.  
  
-   Continuer à utiliser les services Web ASP.NET intention d’adopter WCF à un moment donné dans le futur. Les rubriques de cette section expliquent comment optimiser vos chances de pouvoir utiliser les nouvelles applications de service Web ASP.NET ainsi que les futures applications WCF. Les rubriques de cette section expliquent également comment générer des services afin de simplifier leur migration vers WCF d’un site Web ASP.NET. Toutefois, si la sécurisation des services est importante, ou les garanties de fiabilité ou de transaction sont exigées, ou si personnalisé des fonctionnalités de gestion seront nécessaire doit être construite, alors il est préférable d’adopter WCF. WCF est conçu pour précisément ces scénarios.  
  
-   Adopter WCF pour tout nouveau développement, tout en continuant à maintenir vos applications de service Web ASP.NET existantes. Ce choix est très probablement le plus optimal. Il offre les avantages de WCF, tout en économisant le coût de la modification des applications existantes à l’utiliser. Dans ce scénario, les nouvelles applications WCF peuvent coexister avec les applications ASP.NET existantes. Nouvelles applications WCF sera en mesure d’utiliser les services Web ASP.NET existants, et WCF peut être utilisé pour programmer de nouvelles fonctionnalités opérationnelles dans les applications ASP.NET existantes en vertu du mode de compatibilité ASP.NET de WCF.  
  
-   Adopter WCF et migrer des applications de service Web ASP.NET existantes vers WCF. Vous pouvez choisir cette option pour améliorer les applications existantes avec les fonctionnalités fournies par WCF, ou reproduire les fonctionnalités des services Web ASP.NET existants dans de nouvelles, les plus puissantes applications WCF.  
  
> [!NOTE]
>  Soyez prudent si un service WCF est hébergé par IIS 5.x et ASP.NET est désinstallé. Lorsqu’un service WCF est hébergé par IIS 5.x, le code pour le service peut être demandé si ASP.NET est désinstallé. Lorsque ASP.NET est désinstallé sur un système d’exploitation qui exécute IIS 5.x et WCF est désinstallé, un fichier avec l’extension .svc est considéré comme un fichier texte et le contenu, y compris tout code source, est retourné au demandeur.  
  
 Cette section décrit en détail ces options, compare les Services Web ASP.NET vers WCF et fournit des instructions sur la migration de votre code des Services Web ASP.NET vers WCF.  
  
## <a name="see-also"></a>Voir aussi  
 [Anticipation de l’adoption de Windows Communication Foundation : faciliter la migration future](../../../../docs/framework/wcf/feature-details/anticipating-adopting-wcf-migration.md)  
 [Anticipation de l’adoption de Windows Communication Foundation : faciliter l’intégration future](../../../../docs/framework/wcf/feature-details/anticipating-adopting-the-wcf-easing-future-integration.md)  
 [Adoption de Windows Communication Foundation](../../../../docs/framework/wcf/feature-details/adopting-wcf.md)  
 [Comparaison des services web ASP.NET et de WCF en fonction de l’objectif et des normes utilisées](../../../../docs/framework/wcf/feature-details/comparing-aspnet-web-services-to-wcf-based-on-purpose-and-standards-used.md)  
 [Comparaison des services web ASP.NET et de WCF du point de vue du développement](../../../../docs/framework/wcf/feature-details/comparing-aspnet-web-services-to-wcf-based-on-development.md)
