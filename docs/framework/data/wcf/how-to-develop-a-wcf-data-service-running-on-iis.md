---
title: 'Procédure : développer un WCF Data Service qui fonctionne sur IIS'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, developing
- WCF Data Services, deploying
- WCF Data Services, hosting
ms.assetid: f6f768c5-4989-49e3-a36f-896ab4ded86e
ms.openlocfilehash: af81e65dfd4661d62d7aa4a3e6075be312765cb7
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46579964"
---
# <a name="how-to-develop-a-wcf-data-service-running-on-iis"></a>Comment : développer un service de données WCF en cours d’exécution sur IIS

Cette rubrique montre comment utiliser WCF Data Services pour créer un service de données qui est basé sur la base de données Northwind qui est hébergé par une application Web ASP.NET qui s’exécute sur Internet Information Services (IIS). Pour obtenir un exemple montrant comment créer le même service de données Northwind en tant qu’une application Web ASP.NET qui s’exécute sur le serveur de développement ASP.NET, consultez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).

> [!NOTE]
> Pour créer le service de données Northwind, vous avez dû installer l'exemple de base de données Northwind sur l'ordinateur local. Pour télécharger cette base de données exemple, consultez la page de téléchargement [Sample Databases for SQL Server](https://go.microsoft.com/fwlink/?linkid=24758).

 Cette rubrique indique comment créer un service de données à l’aide du fournisseur Entity Framework. Il existe d'autres fournisseurs de services de données. Pour plus d’informations, consultez [fournisseurs de Services de données](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).

 Après avoir créé le service, vous devez explicitement fournir un accès aux ressources du service de données. Pour plus d’informations, consultez [Comment : activer l’accès au Service de données](../../../../docs/framework/data/wcf/how-to-enable-access-to-the-data-service-wcf-data-services.md).

## <a name="create-the-aspnet-web-application-that-runs-on-iis"></a>Créer l’application web ASP.NET qui s’exécute sur IIS

1. Dans Visual Studio, sur le **fichier** menu, sélectionnez **New** > **projet**.

2. Dans le **nouveau projet** boîte de dialogue, sélectionnez le **installé** > [**Visual C#** ou **Visual Basic**] > **Web** catégorie.

3. Sélectionnez le **Application Web ASP.NET** modèle.

1. Entrez `NorthwindService` comme nom du projet.

5. Cliquez sur **OK**.

6. Sur le **projet** menu, sélectionnez **propriétés NorthwindService**.

7. Sélectionnez le **Web** onglet, puis sélectionnez **utiliser le serveur Web IIS Local**.

8. Cliquez sur **créer un répertoire virtuel** puis cliquez sur **OK**.

9. À partir de l'invite de commandes avec des privilèges d'administrateur, exécutez une des commandes suivantes (en fonction du système d'exploitation) :

    -   Systèmes 32 bits :

        ```console
        "%windir%\Microsoft.NET\Framework\v3.0\Windows Communication Foundation\ServiceModelReg.exe" -i
        ```

    -   Systèmes 64 bits :

        ```console
        "%windir%\Microsoft.NET\Framework64\v3.0\Windows Communication Foundation\ServiceModelReg.exe" -i
        ```

     Cela permet de vérifier que Windows Communication Foundation (WCF) est inscrit sur l'ordinateur.

10. À partir de l'invite de commandes avec des privilèges d'administrateur, exécutez une des commandes suivantes (en fonction du système d'exploitation) :

    -   Systèmes 32 bits :

        ```console
        "%windir%\Microsoft.NET\Framework\v4.0.30319\aspnet_regiis.exe" -i -enable
        ```

    -   Systèmes 64 bits :

        ```console
        "%windir%\Microsoft.NET\Framework64\v4.0.30319\aspnet_regiis.exe" -i -enable
        ```

     Cela permet de s'assurer qu'IIS s'exécute correctement après que WCF a été installé sur l'ordinateur. Vous devrez peut-être redémarrer IIS.

11. Lorsque l'application ASP.NET s'exécute sur IIS7, vous devez aussi effectuer les étapes suivantes :

    1. Ouvrez le Gestionnaire des services Internet et accédez à l’application PhotoService sous **Site Web par défaut**.

    2. Dans **affichage des fonctionnalités**, double-cliquez sur **authentification**.

    3. Sur le **authentification** page, sélectionnez **l’authentification anonyme**.

    4. Dans le **Actions** volet, cliquez sur **modifier** pour définir la sécurité du principal sous lequel les utilisateurs anonymes se connecteront au site.

    5. Dans le **modifier les informations d’identification d’authentification anonyme** boîte de dialogue, sélectionnez **identité du pool d’Application**.

    > [!IMPORTANT]
    > Lorsque vous utilisez le compte de service réseau, vous accordez aux utilisateurs anonymes l'accès à tout le réseau interne associé à ce compte.

12. En utilisant SQL Server Management Studio, l'utilitaire sqlcmd.exe ou l'Éditeur Transact-SQL dans Visual Studio, exécutez la commande Transact-SQL suivante sur l'instance SQL Server à laquelle la base de données Northwind est attachée :

    ```sql
    CREATE LOGIN [NT AUTHORITY\NETWORK SERVICE] FROM WINDOWS;
    GO
    ```

    Cela crée une connexion dans l'instance SQL Server pour le compte Windows utilisé pour exécuter IIS. Cela permet à IIS de se connecter à l'instance de SQL Server.

13. Avec la base de données Northwind attachée, exécutez les commandes Transact-SQL suivantes :

    ```sql
    USE Northwind
    GO
    CREATE USER [NT AUTHORITY\NETWORK SERVICE]
    FOR LOGIN [NT AUTHORITY\NETWORK SERVICE] WITH DEFAULT_SCHEMA=[dbo];
    GO
    ALTER LOGIN [NT AUTHORITY\NETWORK SERVICE]
    WITH DEFAULT_DATABASE=[Northwind];
    GO
    EXEC sp_addrolemember 'db_datareader', 'NT AUTHORITY\NETWORK SERVICE'
    GO
    EXEC sp_addrolemember 'db_datawriter', 'NT AUTHORITY\NETWORK SERVICE'
    GO
    ```

    Cela accorde des droits à la nouvelle connexion et permet à IIS de lire et d'écrire les données dans la base de données Northwind.

## <a name="define-the-data-model"></a>Définir le modèle de données

1. Dans **l’Explorateur de solutions**, cliquez sur le nom du projet ASP.NET, puis cliquez sur **ajouter** > **un nouvel élément**.

2. Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez **ADO.NET Entity Data Model**.

3. Pour le nom du modèle de données, tapez `Northwind.edmx`.

4. Dans l’Assistant Entity Data Model, sélectionnez **générer à partir de la base de données**, puis cliquez sur **suivant**.

5. Connectez le modèle de données à la base de données en effectuant l’une des étapes suivantes, puis cliquez sur **suivant**:

    -   Si vous n’avez pas déjà configuré une connexion de base de données, cliquez sur **nouvelle connexion** et créer une nouvelle connexion. Pour plus d’informations, consultez [Comment : créer des connexions aux bases de données SQL Server](https://go.microsoft.com/fwlink/?LinkId=123631). Cette instance SQL Server doit avoir l'exemple de base de données Northwind joint.

         \- ou -

    -   Si vous avez une connexion de base de données déjà configurée pour vous connecter à la base de données Northwind, sélectionnez cette connexion dans la liste des connexions.

6. Dans la page finale de l'Assistant, activez les cases à cocher pour toutes les tables de la base de données puis désactivez les cases pour les vues et les procédures stockées.

7. Cliquez sur **Terminer** pour fermer l’Assistant.

## <a name="create-the-data-service"></a>Créer le service de données

1. Dans **l’Explorateur de solutions**, cliquez sur le nom de votre projet ASP.NET, puis cliquez sur **ajouter** > **un nouvel élément**.

2. Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez **Service de données WCF**.

   ![Modèle d’élément de Service de données WCF dans Visual Studio 2015](media/wcf-data-service-item-template.png)

   > [!NOTE]
   > Le **Service de données WCF** modèle est disponible dans Visual Studio 2015, mais pas dans Visual Studio 2017.

3. Entrez le nom du service `Northwind`.

     Visual Studio crée le balisage XML et des fichiers de code pour le nouveau service. La fenêtre de l'éditeur de code s'ouvre par défaut. Dans **l’Explorateur de solutions**, le service a le nom, Northwind et l’extension. svc.cs ou. svc.vb.

4. Dans le code du service de données, remplacez le commentaire `/* TODO: put your data source class name here */` dans la définition de la classe qui définit le service de données par le type qui est le conteneur d'entités du modèle de données, dans ce cas `NorthwindEntities`. La définition de classe doit ressembler aux éléments suivants:

     [!code-csharp[Astoria Quickstart Service#ServiceDefinition](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart service/cs/northwind.svc.cs#servicedefinition)]
     [!code-vb[Astoria Quickstart Service#ServiceDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart service/vb/northwind.svc.vb#servicedefinition)]

## <a name="see-also"></a>Voir aussi

- [Exposition de vos données comme service](../../../../docs/framework/data/wcf/exposing-your-data-as-a-service-wcf-data-services.md)
