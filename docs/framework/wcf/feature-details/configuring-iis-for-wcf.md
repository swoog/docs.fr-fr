---
title: Configuration des services Internet (IIS) 7.0 pour Windows Communication Foundation
ms.date: 03/30/2017
ms.assetid: 1050d395-092e-44d3-b4ba-66be3b039ffb
ms.openlocfilehash: 13fd068f7a058a0fbf4e15fc99a8de91671fb2d5
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45521354"
---
# <a name="configuring-internet-information-services-70-for-windows-communication-foundation"></a>Configuration des services Internet (IIS) 7.0 pour Windows Communication Foundation

Les services Internet (IIS) 7.0 sont conçus de manière modulaire vous permettant ainsi d'installer uniquement les composants dont vous avez besoin. Leur conception s'appuie sur la nouvelle technologie multi-composant orientée manifeste, utilisée pour la première fois dans [!INCLUDE[wv](../../../../includes/wv-md.md)]. Il existe plus de 40 composants autonomes d’IIS 7.0 qui peut être installé indépendamment. Cela permet aux professionnels de l'informatique de personnaliser plus facilement leur installation en fonction de leurs besoins. Cette rubrique explique comment configurer IIS 7.0 pour une utilisation avec Windows Communication Foundation (WCF) et déterminer quels composants sont nécessaires.

## <a name="minimal-installation-installing-was"></a>Installation minimale : installation du service WAS
 L’installation minimale de l’ensemble du package IIS 7.0 est d’installer le Service de l’Activation des processus Windows (WAS). A été est une fonctionnalité autonome et il est la seule fonctionnalité à partir d’IIS 7.0 qui est disponible pour tous les [!INCLUDE[wv](../../../../includes/wv-md.md)] les systèmes d’exploitation (Édition Familiale Basique, Édition familiale Premium, Professionnel et Édition intégrale et entreprise).

 À partir du Panneau de configuration, cliquez sur **programmes** puis cliquez sur **ou désactiver des fonctionnalités Windows activer** sous **programmes et fonctionnalités**, le composant WAS s’affiche dans la liste, comme dans l’illustration suivante.

 ![Activer la boîte de dialogue désactiver ou de fonctionnalités sur](../../../../docs/framework/wcf/feature-details/media/wcfc-turnfeaturesonoroffs.gif "wcfc_TurnFeaturesOnOrOffs")

 Cette fonctionnalité intègre les sous-composants suivants :

-   Environnement .NET

-   Interfaces API de configuration

-   Modèle de processus

 Si vous sélectionnez le nœud racine WAS, le **modèle de processus** sous-nœud est activée par défaut. Remarque : dans le cadre de la présente installation, seul le service WAS est installé car la prise en charge d’un serveur web n’est pas assurée.

 Pour WCF ou n’importe quel travail d’application ASP.NET, consultez le **environnement .NET** case à cocher. Cela signifie que tous les composants du service WAS sont requises pour que WCF et ASP.NET pour un fonctionnement optimal. Ces composants sont automatiquement activés dès lors que l'un d'entre eux est installé.

## <a name="iis-70-default-installation"></a>IIS 7.0 : installation par défaut
 En vérifiant la **Internet Information Services** fonctionnalité, certains nœuds secondaires sont automatiquement vérifiés comme indiqué dans l’illustration suivante.

 ![Paramètres par défaut pour les fonctionnalités d’IIS 7.0](../../../../docs/framework/wcf/feature-details/media/wcfc-turningfeaturesonoroff2.gif "wcfc_TurningFeaturesOnOrOff2")

 Il s’agit de l’installation par défaut d’IIS 7.0. Avec cette installation, vous pouvez utiliser IIS 7.0 pour fournir du contenu statique (par exemple, des pages HTML et d’autres contenus). Toutefois, vous ne pouvez pas exécuter les applications ASP.NET et CGI ou héberger des services WCF.

## <a name="iis-70-installation-with-aspnet-support"></a>IIS 7.0 : installation avec prise en charge ASP.NET
 Vous devez installer ASP.NET pour utiliser ASP.NET sur IIS 7.0. Après avoir vérifié **ASP.NET**, votre écran doit ressembler à l’illustration suivante.

 ![Asp.NET les paramètres requis](../../../../docs/framework/wcf/feature-details/media/wcfc-trunfeaturesonoroff3s.gif "wcfc_TrunFeaturesOnOrOFf3s")

 Il s’agit de l’environnement minimal pour les applications WCF et ASP.NET fonctionne dans IIS 7.0.

## <a name="iis-70-installation-with-iis-60-compatibility-components"></a>IIS 7.0 : installation avec les composants de compatibilité IIS 6.0
 Lors de l’installation d’IIS 7.0 sur un système avec Visual Studio 2005 ou certaines autres scripts d’automatisation ou certains outils (tels que Adsutil.vbs) qui configurent des applications virtuelles qui utilisent les API de métabase IIS 6.0, vérifiez que vous vérifiez l’IIS 6.0 **outils de script**. Cette procédure vérifie automatiquement les autres sous-nœuds d’IIS 6.0 **Management Compatibility**. L’illustration suivante montre l’écran une fois cette opération est effectuée :

 ![Paramètres de compatibilité IIS 6.0 Management](../../../../docs/framework/wcf/feature-details/media/scfc-turnfeaturesonoroff5s.gif "scfc_TurnFeaturesOnOrOff5s")

 Avec cette installation, vous disposez de tous les éléments requis pour utiliser les fonctionnalités IIS 7.0, ASP.NET et WCF et les exemples disponibles sur le Web.

## <a name="request-limits"></a>Limites de la demande
 Sur [!INCLUDE[wv](../../../../includes/wv-md.md)] avec IIS 7, la valeur par défaut des paramètres `maxUri` et `maxQueryStringSize` a été modifiée. Par défaut, le filtrage de demande dans IIS 7.0 autorise une URL d'une longueur de 4096 caractères et une longueur de chaîne de 2048 caractères. Pour modifier ces valeurs par défaut, ajoutez l'élément XML suivant au fichier App.config.

 `<system.webServer>`

 `<security>`

 `<requestFiltering>`

 `<requestLimits maxUrl="8192" maxQueryString="8192" />`

 `</requestFiltering>`

 `</security>`

 `</system.webServer>`

## <a name="see-also"></a>Voir aussi

- [Architecture d’activation WAS](../../../../docs/framework/wcf/feature-details/was-activation-architecture.md)
- [Configuration du service WAS pour une utilisation avec WCF](../../../../docs/framework/wcf/feature-details/configuring-the-wpa--service-for-use-with-wcf.md)
- [Guide pratique pour installer et configurer des composants d’activation WCF](../../../../docs/framework/wcf/feature-details/how-to-install-and-configure-wcf-activation-components.md)
- [Fonctionnalités d’hébergement de Windows Server App Fabric](https://go.microsoft.com/fwlink/?LinkId=201276)
