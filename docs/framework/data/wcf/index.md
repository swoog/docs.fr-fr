---
title: WCF Data Services 4.5
ms.date: 03/30/2017
helpviewer_keywords:
- Astoria
- WCF Data Services, getting started
ms.assetid: 73d2bec3-7c92-4110-b905-11bb0462357a
ms.openlocfilehash: 9ece2fe051855d0fd39556f56a4343ead2c437bc
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44197009"
---
# <a name="wcf-data-services-45"></a>WCF Data Services 4.5

WCF Data Services (anciennement « ADO.NET Data Services ») est un composant du .NET Framework qui vous permet de créer des services qui utilisent le [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] pour exposer et consommer des données sur le Web ou l’intranet à l’aide de la sémantique de [ transfert d’état Representational (REST)](https://go.microsoft.com/fwlink/?LinkId=113919). OData expose les données sous forme de ressources adressables par des URI. Les données sont accessibles et modifiables à l'aide des verbes HTTP standard GET, PUT, POST et DELETE. OData utilise les conventions relation-entité de la [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md) pour exposer des ressources sous forme de jeux d’entités qui sont reliées par des associations.

WCF Data Services utilise le protocole OData pour l’adressage et la mise à jour des ressources. De cette façon, vous pouvez accéder à ces services à partir de n’importe quel client qui prend en charge d’OData. OData vous permet de demander et écrire des données dans les ressources à l’aide de formats de transfert classiques : Atom, un ensemble de normes pour l’échange et la mise à jour des données en tant que XML et JavaScript Objet Notation (JSON), un format d’échange de données textuel utilisé largement dans AJAX application.

WCF Data Services peut exposer des données provenant de différentes sources en tant que flux OData. Visual Studio tools facilitent la création d’un service OData à l’aide d’un modèle de données ADO.NET Entity Framework. Vous pouvez également créer des flux OData en fonction des classes common language runtime (CLR) et les données même à liaison tardive ou non typées.

WCF Data Services inclut également un ensemble de bibliothèques clientes, un pour les applications clientes .NET Framework générales et un autre spécifique aux applications basées sur Silverlight. Ces bibliothèques clientes fournissent un modèle de programmation basé sur l’objet lorsque vous accédez à un flux OData depuis des environnements tels que .NET Framework et Silverlight.

## <a name="where-should-i-start"></a>Où est-ce que je dois démarrer ?

En fonction de vos centres d’intérêt, envisagez la mise en route avec les Services de données WCF dans une des rubriques suivantes.

Je veux rentrer dans le vif du sujet...

-   [Démarrage rapide](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)

-   [Prise en main](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)

-   [Démarrage rapide avec Silverlight](https://go.microsoft.com/fwlink/?LinkID=192782)

-   [Démarrage rapide avec Silverlight pour le développement de Windows Phone](https://go.microsoft.com/fwlink/?LinkID=214535)

Montrez-moi du code...

-   [Démarrage rapide](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)

-   [Comment : exécuter les requêtes de services de données](../../../../docs/framework/data/wcf/how-to-execute-data-service-queries-wcf-data-services.md)

-   [Comment : lier les données aux éléments Windows Presentation Foundation](../../../../docs/framework/data/wcf/bind-data-to-wpf-elements-wcf-data-services.md)

Je souhaite en savoir plus sur OData...

 -   [Livre blanc : présentation d’OData](https://go.microsoft.com/fwlink/?LinkId=220867)

-   [Site web Open Data Protocol](https://go.microsoft.com/fwlink/?LinkID=184554)

-   [Kit de développement logiciel (SDK) OData](https://go.microsoft.com/fwlink/?LinkID=185248)

-   [OData : forum aux questions](https://go.microsoft.com/fwlink/?LinkId=185867)

Je souhaite regarder des vidéos...

-   [Guide du débutant sur WCF Data Services](https://go.microsoft.com/fwlink/?LinkId=220864)

-   [Vidéos du développeur WCF Data Services](https://go.microsoft.com/fwlink/?LinkId=220861)

-   [OData : site web développeurs](https://go.microsoft.com/fwlink/?LinkId=185866)

Je souhaite consulter des exemples de bout en bout...

-   [Exemples de documentation WCF Data Services dans la galerie d’exemples MSDN](https://go.microsoft.com/fwlink/?LinkID=220865)

-   [Autres exemples WCF Data Services dans la galerie d’exemples MSDN](https://go.microsoft.com/fwlink/?LinkId=220866)

-   [Kit de développement logiciel (SDK) OData](https://go.microsoft.com/fwlink/?LinkID=185248)

Qu'en est-il de l'intégration avec Visual Studio ?

-   [Génération de la bibliothèque cliente du service de données](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)

-   [Création du service de données](../../../../docs/framework/data/wcf/creating-the-data-service.md)

-   [Fournisseur Entity Framework](../../../../docs/framework/data/wcf/entity-framework-provider-wcf-data-services.md)

Comment puis-je l'utiliser ?

-   [Vue d’ensemble](../../../../docs/framework/data/wcf/wcf-data-services-overview.md)

-   [Livre blanc : présentation d’OData](https://go.microsoft.com/fwlink/?LinkId=220867)

-   [Scénarios d’application](../../../../docs/framework/data/wcf/application-scenarios-wcf-data-services.md)

Je souhaite utiliser Silverlight...

-   [Démarrage rapide avec Silverlight](https://go.microsoft.com/fwlink/?LinkID=192782)

-   [WCF Data Services (Silverlight)](https://go.microsoft.com/fwlink/?LinkID=143149)

-   [Prise en main de Silverlight](https://go.microsoft.com/fwlink/?LinkId=148366)

Je souhaite utiliser LINQ...

-   [Interrogation du service de données](../../../../docs/framework/data/wcf/querying-the-data-service-wcf-data-services.md)

-   [Considérations sur LINQ](../../../../docs/framework/data/wcf/linq-considerations-wcf-data-services.md)

-   [Comment : exécuter les requêtes de services de données](../../../../docs/framework/data/wcf/how-to-execute-data-service-queries-wcf-data-services.md)

Toujours, j’ai besoin d’informations supplémentaires...

-   [Blog de l’équipe WCF Data Services](https://go.microsoft.com/fwlink/?LinkID=150511)

-   [Ressources](../../../../docs/framework/data/wcf/wcf-data-services-resources.md)

-   [Centre de développement WCF Data Services](https://go.microsoft.com/fwlink/?LinkId=220868)

-   [Site web Open Data Protocol](https://go.microsoft.com/fwlink/?LinkID=184554)

## <a name="in-this-section"></a>Dans cette section

 [Vue d’ensemble](../../../../docs/framework/data/wcf/wcf-data-services-overview.md)

 Fournit une vue d’ensemble des fonctionnalités et des fonctionnalités disponibles dans WCF Data Services.

 [Nouveautés de WCF Data Services](https://msdn.microsoft.com/library/cf22cad5-b8d9-472b-8d7c-b863b64eaae8)

 Décrit les nouvelles fonctionnalités dans WCF Data Services et la prise en charge des nouvelles fonctionnalités OData.

 [Prise en main](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)

 Décrit comment exposer et consommer des flux OData à l’aide de WCF Data Services.

 [Définition de WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)

 Décrit comment créer et configurer un service de données qui expose des flux OData.

 [Bibliothèque cliente WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)

 Décrit comment utiliser les bibliothèques clientes pour consommer des flux OData à partir d’une application cliente .NET Framework.

## <a name="see-also"></a>Voir aussi

- [Representational State Transfer (REST)](https://go.microsoft.com/fwlink/?LinkId=113919)
