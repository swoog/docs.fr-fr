---
title: 'Tutoriel : Prise en main les applications Windows Communication Foundation'
description: Ces didacticiels fournit une introduction à la création d’applications WCF.
ms.date: 01/25/2019
helpviewer_keywords:
- WCF [WCF], get started
- Windows Communication Foundation [WCF], get started
- get started [WCF]
ms.assetid: df939177-73cb-4440-bd95-092a421516a1
ms.openlocfilehash: d4613edefeb8db2c0d1e11e925f8ac41329efb0d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137921"
---
# <a name="tutorial-get-started-with-windows-communication-foundation-applications"></a>Tutoriel : Prise en main les applications Windows Communication Foundation
Les séries suivantes de didacticiels présentent pour le Windows Communication Foundation (WCF) expérience de programmation. Utilisation de ces didacticiels dans l’ordre vous donnera une compréhension de base des étapes requises pour créer des applications WCF. Une fois que vous avez terminé, vous disposerez d’un service WCF en cours d’exécution et un client WCF qui appelle le service. 

Ce didacticiel suppose que vous utilisez Visual Studio comme environnement de développement. Si vous utilisez un autre environnement de développement, ignorer les instructions spécifiques à Visual Studio. 

Pour plus d’exemples d’applications WCF que vous pouvez télécharger et exécuter, consultez [exemples Windows Communication Foundation](samples/index.md). Pour une introduction aux exemples, consultez [exemple de mise en route](samples/getting-started-sample.md).

Pour plus d’informations sur la création de services et les clients, consultez [programmation WCF de base](basic-wcf-programming.md).

## <a name="wcf-tutorials"></a>Didacticiels WCF

Les trois premiers didacticiels décrivent comment définir un contrat de service WCF, comment l’implémenter et comment héberger. Le service que vous créez est auto-hébergé dans une application console. Vous pouvez également héberger des services sous Microsoft Internet Information Services (IIS). Pour plus d'informations, voir [Procédure : Héberger un Service WCF dans IIS](feature-details/how-to-host-a-wcf-service-in-iis.md). Bien que vous utilisez le code pour configurer le service dans le didacticiel, vous pouvez également [configurer des services au sein d’un fichier de configuration](configuring-services-using-configuration-files.md). 

- [Tutoriel : Définir un contrat de service](how-to-define-a-wcf-service-contract.md)

    Vous créez un contrat WCF avec une interface définie par l’utilisateur. Ce contrat définit les fonctionnalités exposées par le service.

- [Tutoriel : Implémenter un contrat de service](how-to-implement-a-wcf-contract.md)

    Une fois que vous définissez un contrat, vous devez l’implémenter avec une classe de service.

- [Tutoriel : Héberger et exécuter un service de base](how-to-host-and-run-a-basic-wcf-service.md)

    Configurer un point de terminaison pour le service et héberger le service dans une application console. Pour un service devienne actif, vous devez le configurer et héberger dans un environnement d’exécution. Cet environnement d’exécution crée le service et contrôle son contexte et la durée de vie.

Les deux didacticiels expliquent comment créer, configurer et utiliser une application cliente pour appeler les opérations du service expose. Les services publient les métadonnées qui définissent les informations dont une application cliente a besoin pour communiquer avec le service. Visual Studio automatise le processus d’accès à ces métadonnées et l’utilise pour construire l’application cliente pour le service. Si vous décidez de ne pas utiliser Visual Studio, vous pouvez utiliser la [outil ServiceModel Metadata Utility (*Svcutil.exe*)](servicemodel-metadata-utility-tool-svcutil-exe.md) à la place.

- [Tutoriel : Créer un client](how-to-create-a-wcf-client.md)

    Récupérer les métadonnées pour la création d’un proxy de client WCF à partir d’un service WCF. Récupérer des métadonnées à l’aide de Visual Studio pour ajouter une référence de service, ou vous pouvez utiliser l’outil ServiceModel Metadata Utility. Vous spécifiez le point de terminaison que le client utilise pour accéder au service.

- [Tutoriel : Utiliser un client](how-to-use-a-wcf-client.md)

    Utiliser le proxy client WCF pour appeler les opérations de service.

## <a name="reference"></a>Référence

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble conceptuelle](conceptual-overview.md)
- [Guide de la documentation](guide-to-the-documentation.md)
- [Nouveautés de Windows Communication Foundation](whats-wcf.md)
- [Informations sur les fonctionnalités WCF](feature-details/index.md)
- [Cycle de vie de programmation base](basic-programming-lifecycle.md)
- [Génération de clients](building-clients.md)
- [Programmation de WCF de base](basic-wcf-programming.md)
- [Guide pratique pour Créer un contrat duplex](feature-details/how-to-create-a-duplex-contract.md)
- [Guide pratique pour Access services avec un contrat duplex](feature-details/how-to-access-services-with-a-duplex-contract.md)
- [ServiceModel Metadata Utility tool (Svcutil.exe)](servicemodel-metadata-utility-tool-svcutil-exe.md)
- [Guide pratique pour Utiliser Svcutil.exe pour télécharger des documents de métadonnées](feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
- [Guide pratique pour Publier les métadonnées pour un service à l’aide d’un fichier de configuration](feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [À l’aide de liaisons pour configurer les clients et services](using-bindings-to-configure-services-and-clients.md)
- [Getting started, exemple](samples/getting-started-sample.md)
- [Exemples Windows Communication Foundation](samples/index.md)
- [Auto-hébergement](samples/self-host.md)
