---
title: Démarrage rapide (services de données WCF)
ms.date: 08/24/2018
helpviewer_keywords:
- WCF Data Services, quick-start example
- WCF Data Services, Entity Data Model (EDM) service
ms.assetid: 7b18ca1e-d4d6-4c7a-afb9-ce3cebb98a8d
ms.openlocfilehash: f20ffcf356aa0493b1e2356746d9ad7b27d9a1aa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61876198"
---
# <a name="quickstart-wcf-data-services"></a>Démarrage rapide (services de données WCF)

Ce démarrage rapide vous permet de vous familiariser avec les Services de données WCF et le [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] via une série de tâches qui prennent en charge les rubriques de [mise en route](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md).

## <a name="what-youll-learn"></a>Ce que vous allez apprendre

La première tâche dans ce démarrage rapide montre comment créer un service de données pour exposer un flux OData depuis la base de données Northwind. Dans les rubriques ultérieures, vous accéderez OData flux à l’aide d’un navigateur Web, mais également créer une application Windows Presentation Foundation (WPF) application cliente qui consomme le OData flux à l’aide des bibliothèques clientes.

## <a name="prerequisites"></a>Prérequis

Pour effectuer ce démarrage rapide, vous devez installer les composants suivants :

- Visual Studio

- Une instance de SQL Server. Cela comprend SQL Server Express, qui est inclus dans une installation par défaut de Visual Studio 2015, ou dans le cadre de la **stockage de données et de traitement** charge de travail dans Visual Studio 2017.

- Exemple de base de données Northwind. Pour télécharger cet exemple de base de données, consultez la page de téléchargement, [Exemples de bases de données pour SQL Server](https://go.microsoft.com/fwlink/?linkid=24758).

## <a name="wcf-data-services-quickstart-tasks"></a>Tâches de démarrage rapide de WCF data services

 [Créer le Service de données](../../../../docs/framework/data/wcf/creating-the-data-service.md)

 Définir l'application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] , définir le modèle de données, créer le service de données et autoriser l'accès aux ressources.

 [Accéder au Service à partir d’un navigateur Web](../../../../docs/framework/data/wcf/accessing-the-service-from-a-web-browser-wcf-data-services-quickstart.md)

 Démarrer le service à partir de Visual Studio et accéder au service en soumettant des demandes HTTP GET via un navigateur Web au flux exposé.

 [Créer l’Application cliente .NET Framework](../../../../docs/framework/data/wcf/creating-the-dotnet-client-application-wcf-data-services-quickstart.md)

 Créer une application WPF pour consommer le flux OData, lier des données aux contrôles de Windows, modifier des données dans les contrôles dépendants, puis renvoyer les modifications apportées au service de données.

> [!NOTE]
> Les fichiers projet d’une version terminée du démarrage rapide peuvent être téléchargés à partir de la page [WCF Data Services Quickstart (OData Service and WPF Client)](https://go.microsoft.com/fwlink/?LinkId=179994) .

## <a name="next-steps"></a>Étapes suivantes

> [!div class="nextstepaction"]
> [Démarrer le didacticiel de démarrage rapide](../../../../docs/framework/data/wcf/creating-the-data-service.md)

## <a name="see-also"></a>Voir aussi

- [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)
