---
title: Mise en route Tutorial1
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], getting started
- Windows Communication Foundation [WCF], getting started
- getting started [WCF]
ms.assetid: df939177-73cb-4440-bd95-092a421516a1
ms.openlocfilehash: b0abe7a6b127a254c2f5c72dc66fc128d35374fb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491361"
---
# <a name="getting-started-tutorial"></a>Didacticiel de mise en route
Les rubriques contenues dans cette section sont conçues pour vous permettre l’exposition rapide pour le Windows Communication Foundation (WCF) expérience de programmation. Elles doivent être parcourues dans l'ordre de la liste indiquée au bas de cette rubrique. Ce didacticiel vous offre une compréhension de base des étapes requises pour créer des applications client et le service WCF. Un service expose un ou plusieurs points de terminaison, chaque point de terminaison exposant une ou plusieurs opérations de service. Le *point de terminaison* d’un service spécifie une adresse où le service peut être trouvé, une liaison qui contient les informations qui décrivent comment un client doit communiquer avec le service et un contrat qui définit les fonctionnalités fourni par le service à ses clients.

 Une fois que vous aurez terminé la séquence de rubriques de ce didacticiel, vous disposerez d'un service opérationnel et d'un client qui appelle le service. Les trois premières rubriques décrivent comment définir un contrat de service, comment implémenter le contrat de service et comment héberger le service. Le service créé est auto-hébergé dans une application console. Les services peuvent également être hébergés sous IIS (Internet Information Services). Pour plus d’informations sur la manière de procéder, consultez [Guide pratique pour Héberger un Service WCF dans IIS](../../../docs/framework/wcf/feature-details/how-to-host-a-wcf-service-in-iis.md). Le service est configuré dans le code ; toutefois, les services peuvent également être configurés dans un fichier de configuration. Pour plus d’informations sur l’utilisation d’un fichier de configuration, consultez [fichiers de configuration des Services à l’aide de la Configuration](../../../docs/framework/wcf/configuring-services-using-configuration-files.md).

 Les trois rubriques suivantes décrivent comment créer un proxy client, comment configurer l'application cliente et comment utiliser le proxy client pour appeler l'opération de service exposée par le service. Les services publient les métadonnées qui définissent les informations dont une application cliente a besoin pour communiquer avec le service. Visual Studio 2012 automatise le processus d’accès à ces métadonnées et l’utilise pour construire et configurer l’application cliente pour le service. Si vous n’utilisez pas Visual Studio 2012, vous pouvez utiliser la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour créer et configurer l’application cliente pour le service.

Les rubriques de cette section supposent que vous utilisez Visual Studio comme environnement de développement. Si vous utilisez un autre environnement de développement, ignorer les instructions spécifiques à Visual Studio.

Pour des exemples d’applications qui peuvent être téléchargés sur votre disque dur et exécuter, consultez les rubriques dans [exemples Windows Communication Foundation](https://msdn.microsoft.com/library/8ec9d192-5d81-4f64-bfd3-90c5e5858c91). Pour cette rubrique, consultez, en particulier, le [mise en route](../../../docs/framework/wcf/samples/getting-started-sample.md).

Pour plus d’informations sur la création de services et les clients, consultez [programmation WCF de base](../../../docs/framework/wcf/basic-wcf-programming.md).

## <a name="in-this-section"></a>Dans cette section
 [Guide pratique pour Définir un contrat de Service](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md)

 Décrit comment créer un contrat WCF à l’aide d’une interface définie par l’utilisateur. Le contrat définit les fonctionnalités exposées par le service.

 [Guide pratique pour Implémenter un contrat de Service](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

 Décrit comment implémenter un contrat de service. Une fois qu'un contrat est défini, il doit être implémenté avec une classe de service.

 [Guide pratique pour Héberger et exécuter un Service de base](../../../docs/framework/wcf/how-to-host-and-run-a-basic-wcf-service.md)

 Décrit comment configurer un point de terminaison pour le service dans du code et comment héberger le service dans une application console. Pour qu'il devienne actif, un service doit être configuré et hébergé dans un environnement d'exécution. Cet environnement crée le service et contrôle son contexte et sa durée de vie.

 [Guide pratique pour Créer un Client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)

 Décrit comment extraire les métadonnées utilisées pour créer un proxy de client WCF à partir d’un service WCF. Ce processus utilise la fonctionnalité Ajouter une référence de Service au sein de Visual Studio.

 [Guide pratique pour Configurer un Client](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

 Décrit comment configurer un client WCF. La configuration du client nécessite la spécification du point de terminaison que le client utilise pour accéder au service.

 [Guide pratique pour Utiliser un Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

 Décrit comment utiliser le proxy client WCF pour appeler des opérations de service.

## <a name="reference"></a>Référence

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>

## <a name="related-sections"></a>Rubriques connexes

- [Exemples Windows Communication Foundation](https://msdn.microsoft.com/library/8ec9d192-5d81-4f64-bfd3-90c5e5858c91)
- [Cycle de vie de la programmation de base](../../../docs/framework/wcf/basic-programming-lifecycle.md)

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble conceptuelle](../../../docs/framework/wcf/conceptual-overview.md)
- [Guide de la documentation](../../../docs/framework/wcf/guide-to-the-documentation.md)
- [Présentation de Windows Communication Foundation](../../../docs/framework/wcf/whats-wcf.md)
- [Informations détaillées sur les fonctionnalités de WCF](../../../docs/framework/wcf/feature-details/index.md)