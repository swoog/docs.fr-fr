---
title: Créer un service de données WCF dans Visual Studio
ms.date: 08/24/2018
dev_langs:
- csharp
- vb
ms.assetid: 34d1d971-5e18-4c22-9bf6-d3612e27ea59
ms.openlocfilehash: 361582866dabf51665e1dc94fdc49e8710d8ad3e
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56091823"
---
# <a name="create-the-data-service"></a>Créer le service de données

Dans cette rubrique, vous créez un exemple de service de données qui utilise WCF Data Services pour exposer un [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] flux basé sur la base de données Northwind. La tâche implique les étapes fondamentales suivantes :

1. Créez une application Web ASP.NET.

2. Définissez le modèle de données à l'aide des outils Entity Data Model.

3. Ajoutez le service de données à l'application Web.

4. Activez l'accès au service de données.

## <a name="create-the-aspnet-web-app"></a>Créer l’application web ASP.NET

1. Dans Visual Studio, sur le **fichier** menu, sélectionnez **New** > **projet**.

1. Dans le **nouveau projet** boîte de dialogue, sous Visual Basic ou Visual c#, sélectionnez le **Web** catégorie, puis sélectionnez **Application Web ASP.NET**.

1. Entrez `NorthwindService` en tant que le nom du projet et sélectionnez **OK**.

1. Dans le **nouvelle Application Web ASP.NET** boîte de dialogue, sélectionnez **vide** , puis sélectionnez **OK**.

1. (Facultatif) Spécifiez un numéro de port spécifique pour votre application Web. Remarque : le numéro de port `12345` est utilisé dans cette série de rubriques de guide de démarrage rapide.

    1. Dans **l’Explorateur de solutions**, avec le bouton droit sur le projet ASP.NET que vous venez de créer, puis choisissez **propriétés**.

    2. Sélectionnez le **Web** onglet et définissez la valeur de la **port spécifique** zone de texte `12345`.

## <a name="define-the-data-model"></a>Définir le modèle de données

1. Dans **l’Explorateur de solutions**, cliquez sur le nom du projet ASP.NET, puis cliquez sur **ajouter** > **un nouvel élément**.

2. Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez le **données** catégorie, puis sélectionnez **ADO.NET Entity Data Model**.

3. Pour le nom du modèle de données, entrez `Northwind.edmx`.

4. Dans le **Assistant Entity Data Model**, sélectionnez **Entity Framework Designer à partir de la base de données**, puis cliquez sur **suivant**.

5. Connectez le modèle de données à la base de données en effectuant l’une des étapes suivantes, puis cliquez sur **suivant**:

    -   Si vous n’avez pas déjà configuré une connexion de base de données, cliquez sur **nouvelle connexion** et créer une nouvelle connexion. Pour plus d'informations, voir [Procédure : Créer des connexions aux bases de données SQL Server](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/s4yys16a(v=vs.90)). Cette instance SQL Server doit avoir l'exemple de base de données Northwind joint.

         \- ou -

    -   Si vous avez une connexion de base de données déjà configurée pour vous connecter à la base de données Northwind, sélectionnez cette connexion dans la liste des connexions.

6. Dans la page finale de l'Assistant, activez les cases à cocher pour toutes les tables de la base de données puis désactivez les cases pour les vues et les procédures stockées.

7. Cliquez sur **Terminer** pour fermer l’Assistant.

## <a name="create-the-wcf-data-service"></a>Créer le service de données WCF

1. Dans **l’Explorateur de solutions**, avec le bouton droit sur le projet ASP.NET, puis choisissez **ajouter** > **un nouvel élément**.

2. Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez le **Service de données WCF** modèle d’élément de la **Web** catégorie.

   ![Modèle d’élément de Service de données WCF dans Visual Studio 2015](media/wcf-data-service-item-template.png)

   > [!NOTE]
   > Le **Service de données WCF** modèle est disponible dans Visual Studio 2015, mais pas dans Visual Studio 2017.

3. Pour le nom du service, tapez `Northwind`.

     Visual Studio crée le balisage XML et des fichiers de code pour le nouveau service. La fenêtre de l'éditeur de code s'ouvre par défaut. Dans **l’Explorateur de solutions**, le service a le nom Northwind avec l’extension *. svc.cs* ou *. svc.vb*.

4. Dans le code du service de données, remplacez le commentaire `/* TODO: put your data source class name here */` dans la définition de la classe qui définit le service de données par le type qui est le conteneur d'entités du modèle de données, dans ce cas `NorthwindEntities`. La définition de classe doit ressembler aux éléments suivants:

     [!code-csharp[Astoria Quickstart Service#ServiceDefinition](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart service/cs/northwind.svc.cs#servicedefinition)]
     [!code-vb[Astoria Quickstart Service#ServiceDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart service/vb/northwind.svc.vb#servicedefinition)]

## <a name="enable-access-to-data-service-resources"></a>Activer l’accès aux ressources de service de données

1. Dans le code du service de données, remplacez le code d'espace réservé dans la fonction `InitializeService` par le code suivant :

     [!code-csharp[Astoria Quickstart Service#AllReadConfig](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart service/cs/northwind.svc.cs#allreadconfig)]
     [!code-vb[Astoria Quickstart Service#AllReadConfig](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart service/vb/northwind.svc.vb#allreadconfig)]

     Cela permet aux clients autorisés d'accéder aux ressources en lecture et en écriture pour les jeux d'entités spécifiés.

    > [!NOTE]
    > Tout client qui peut accéder à l'application ASP.NET peut également accéder aux ressources exposées par le service de données. Dans un service de données de production, pour empêcher l'accès non autorisé aux ressources, vous devez également sécuriser l'application elle-même. Pour plus d'informations, consultez [Securing WCF Data Services](../../../../docs/framework/data/wcf/securing-wcf-data-services.md).

## <a name="next-steps"></a>Étapes suivantes

Vous avez créé un nouveau service de données qui expose un flux OData est basé sur la base de données Northwind, et que vous avez activé l’accès au flux pour les clients qui ont des autorisations sur l’application Web ASP.NET. Ensuite, vous allez démarrer le service de données à partir de Visual Studio et accéder au flux en soumettant des demandes HTTP GET via un navigateur Web OData :

> [!div class="nextstepaction"]
> [Accéder au service à partir d’un navigateur web](../../../../docs/framework/data/wcf/accessing-the-service-from-a-web-browser-wcf-data-services-quickstart.md)

## <a name="see-also"></a>Voir aussi

- [ADO.NET Entity Data Model Tools](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))