---
title: Création de l'application cliente .NET Framework (démarrage rapide des services de données WCF)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 41ade767-eeab-437d-9121-9797e8fb8045
ms.openlocfilehash: efea92fa5176641ac64265dfffd44a088115bb61
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59305934"
---
# <a name="creating-the-net-framework-client-application-wcf-data-services-quickstart"></a>Création de l'application cliente .NET Framework (démarrage rapide des services de données WCF)

Il s’agit de la dernière tâche du démarrage rapide WCF Data Services. Dans cette tâche, vous ajoutez une application console à la solution, ajoutez une référence à la [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] alimenter cette nouvelle application cliente et accéder au flux à partir de l’application cliente en utilisant les classes de service de données client générées et les bibliothèques clientes OData .

> [!NOTE]
> Il n'est pas obligatoire pour une application cliente .NET Framework d'accéder à un flux de données. Le service de données est accessible par n’importe quel composant d’application qui consomme un flux OData. Pour plus d’informations, consultez [à l’aide d’un Service de données dans une Application cliente](../../../../docs/framework/data/wcf/using-a-data-service-in-a-client-application-wcf-data-services.md).

## <a name="to-create-the-client-application-by-using-visual-studio"></a>Pour créer l'application cliente à l'aide de Visual Studio

1. Dans **l’Explorateur de solutions**, avec le bouton droit de la solution, cliquez sur **ajouter**, puis cliquez sur **nouveau projet**.

2. Dans le volet gauche, sélectionnez **installé** > [**Visual C#**  ou **Visual Basic**] > **Windows Desktop**, puis sélectionnez le  **Application WPF** modèle.

3. Entrez `NorthwindClient` pour le nom du projet, puis cliquez sur **OK**.

4. Ouvrez le fichier MainWindow.xaml et remplacez le code XAML par le code suivant :

     [!code-xaml[Astoria Quickstart Client#Window1Xaml](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml#window1xaml)]

## <a name="to-add-a-data-service-reference-to-the-project"></a>Pour ajouter une référence de service de données au projet

1. Dans **l’Explorateur de solutions**, cliquez sur le projet NorthwindClient, cliquez sur **ajouter** > **une référence de Service**, puis cliquez sur **Discover** .

     Cette opération affiche le service de données Northwind que vous avez créé dans la première tâche.

2. Dans le **Namespace** zone de texte, tapez `Northwind`, puis cliquez sur **OK**.

     Cette opération ajoute un nouveau fichier de code au projet qui contient les classes de données utilisées pour accéder et interagir avec les ressources du service de données sous la forme d'objets. Les classes de données sont créées dans l'espace de noms `NorthwindClient.Northwind`.

## <a name="to-access-data-service-data-in-the-wpf-application"></a>Pour accéder aux données du service des données dans l'application WPF

1. Dans **l’Explorateur de solutions** sous **NorthwindClient**, cliquez sur le projet, puis cliquez sur **ajouter une référence**.

2. Dans le **ajouter une référence** boîte de dialogue, cliquez sur le **.NET** onglet, sélectionnez l’assembly System.Data.Services.Client.dll, puis cliquez sur **OK**.

3. Dans **l’Explorateur de solutions** sous **NorthwindClient**, ouvrez la page de codes pour le fichier MainWindow.xaml et ajoutez le code suivant `using` instruction (`Imports` en Visual Basic).

     [!code-csharp[Astoria Quickstart Client#Using](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart client/cs/window1.xaml.cs#using)]
     [!code-vb[Astoria Quickstart Client#Using](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml.vb#using)]

3. Insérez le code suivant qui interroge le service de données et lie le résultat à une <xref:System.Data.Services.Client.DataServiceCollection%601> dans la classe `MainWindow`:

    > [!NOTE]
    > Vous devez remplacer le nom d'hôte `localhost:12345` par le serveur et le port qui hébergent votre instance du service de données Northwind.

     [!code-csharp[Astoria Quickstart Client#QueryCode](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart client/cs/window1.xaml.cs#querycode)]
     [!code-vb[Astoria Quickstart Client#QueryCode](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml.vb#querycode)]

4. Insérez le code suivant qui enregistre les modifications dans la classe `MainWindow` :

     [!code-csharp[Astoria Quickstart Client#SaveChanges](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart client/cs/window1.xaml.cs#savechanges)]
     [!code-vb[Astoria Quickstart Client#SaveChanges](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart client/vb/window1.xaml.vb#savechanges)]

## <a name="to-build-and-run-the-northwindclient-application"></a>Pour générer et exécuter l'application NothwindClient

1. Dans **l’Explorateur de solutions**, cliquez sur le projet NorthwindClient et sélectionnez **définir comme projet de démarrage**.

2. Appuyez sur **F5** pour démarrer l’application.

     Cette opération génère et démarre l'application cliente. Les données sont demandées auprès du service et s'affichent dans la console.

3. Modifier une valeur dans le **quantité** colonne de la grille de données, puis cliquez sur **enregistrer**.

     Les modifications sont enregistrées sur le service de données.

    > [!NOTE]
    > Cette version de l'application NorthwindClient ne prend pas en charge l'ajout et la suppression d'entités.

## <a name="next-steps"></a>Étapes suivantes

Vous avez créé avec succès l’application cliente qui accède à l’exemple de que flux OData de Northwind. Vous avez également terminé le démarrage rapide WCF Data Services.

Pour plus d’informations sur l’accès à un OData flux à partir d’un [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] application, consultez [bibliothèque de Client WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md).

## <a name="see-also"></a>Voir aussi

- [Prise en main](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)
- [Ressources](../../../../docs/framework/data/wcf/wcf-data-services-resources.md)
