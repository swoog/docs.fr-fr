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
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46482077"
---
# <a name="how-to-develop-a-wcf-data-service-running-on-iis"></a><span data-ttu-id="36ddc-102">Comment : développer un service de données WCF en cours d’exécution sur IIS</span><span class="sxs-lookup"><span data-stu-id="36ddc-102">How to: Develop a WCF data service running on IIS</span></span>

<span data-ttu-id="36ddc-103">Cette rubrique montre comment utiliser WCF Data Services pour créer un service de données qui est basé sur la base de données Northwind qui est hébergé par une application Web ASP.NET qui s’exécute sur Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="36ddc-103">This topic shows how to use WCF Data Services to create a data service that is based on the Northwind sample database that is hosted by an ASP.NET Web application that is running on Internet Information Services (IIS).</span></span> <span data-ttu-id="36ddc-104">Pour obtenir un exemple montrant comment créer le même service de données Northwind en tant qu’une application Web ASP.NET qui s’exécute sur le serveur de développement ASP.NET, consultez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="36ddc-104">For an example of how to create the same Northwind data service as an ASP.NET Web application that runs on the ASP.NET Development Server, see the [WCF Data Services quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span></span>

> [!NOTE]
> <span data-ttu-id="36ddc-105">Pour créer le service de données Northwind, vous avez dû installer l'exemple de base de données Northwind sur l'ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="36ddc-105">To create the Northwind data service, you must have installed the Northwind sample database on the local computer.</span></span> <span data-ttu-id="36ddc-106">Pour télécharger cette base de données exemple, consultez la page de téléchargement [Sample Databases for SQL Server](https://go.microsoft.com/fwlink/?linkid=24758).</span><span class="sxs-lookup"><span data-stu-id="36ddc-106">To download this sample database, see the download page, [Sample Databases for SQL Server](https://go.microsoft.com/fwlink/?linkid=24758).</span></span>

 <span data-ttu-id="36ddc-107">Cette rubrique indique comment créer un service de données à l’aide du fournisseur Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="36ddc-107">This topic shows how to create a data service by using the Entity Framework provider.</span></span> <span data-ttu-id="36ddc-108">Il existe d'autres fournisseurs de services de données.</span><span class="sxs-lookup"><span data-stu-id="36ddc-108">Other data services providers are available.</span></span> <span data-ttu-id="36ddc-109">Pour plus d’informations, consultez [fournisseurs de Services de données](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="36ddc-109">For more information, see [Data Services Providers](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).</span></span>

 <span data-ttu-id="36ddc-110">Après avoir créé le service, vous devez explicitement fournir un accès aux ressources du service de données.</span><span class="sxs-lookup"><span data-stu-id="36ddc-110">After you create the service, you must explicitly provide access to data service resources.</span></span> <span data-ttu-id="36ddc-111">Pour plus d’informations, consultez [Comment : activer l’accès au Service de données](../../../../docs/framework/data/wcf/how-to-enable-access-to-the-data-service-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="36ddc-111">For more information, see [How to: Enable Access to the Data Service](../../../../docs/framework/data/wcf/how-to-enable-access-to-the-data-service-wcf-data-services.md).</span></span>

## <a name="create-the-aspnet-web-application-that-runs-on-iis"></a><span data-ttu-id="36ddc-112">Créer l’application web ASP.NET qui s’exécute sur IIS</span><span class="sxs-lookup"><span data-stu-id="36ddc-112">Create the ASP.NET web application that runs on IIS</span></span>

1. <span data-ttu-id="36ddc-113">Dans Visual Studio, sur le **fichier** menu, sélectionnez **New** > **projet**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-113">In Visual Studio, on the **File** menu, select **New** > **Project**.</span></span>

2. <span data-ttu-id="36ddc-114">Dans le **nouveau projet** boîte de dialogue, sélectionnez le **installé** > [**Visual C#** ou **Visual Basic**] > **Web** catégorie.</span><span class="sxs-lookup"><span data-stu-id="36ddc-114">In the **New Project** dialog box, select the **Installed** > [**Visual C#** or **Visual Basic**] > **Web** category.</span></span>

3. <span data-ttu-id="36ddc-115">Sélectionnez le **Application Web ASP.NET** modèle.</span><span class="sxs-lookup"><span data-stu-id="36ddc-115">Select the **ASP.NET Web Application** template.</span></span>

1. <span data-ttu-id="36ddc-116">Entrez `NorthwindService` comme nom du projet.</span><span class="sxs-lookup"><span data-stu-id="36ddc-116">Enter `NorthwindService` as the name of the project.</span></span>

5. <span data-ttu-id="36ddc-117">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-117">Click **OK**.</span></span>

6. <span data-ttu-id="36ddc-118">Sur le **projet** menu, sélectionnez **propriétés NorthwindService**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-118">On the **Project** menu, select **NorthwindService Properties**.</span></span>

7. <span data-ttu-id="36ddc-119">Sélectionnez le **Web** onglet, puis sélectionnez **utiliser le serveur Web IIS Local**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-119">Select the **Web** tab, and then select **Use Local IIS Web Server**.</span></span>

8. <span data-ttu-id="36ddc-120">Cliquez sur **créer un répertoire virtuel** puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-120">Click **Create Virtual Directory** and then click **OK**.</span></span>

9. <span data-ttu-id="36ddc-121">À partir de l'invite de commandes avec des privilèges d'administrateur, exécutez une des commandes suivantes (en fonction du système d'exploitation) :</span><span class="sxs-lookup"><span data-stu-id="36ddc-121">From the command prompt with administrator privileges, execute one of the following commands (depending on the operating system):</span></span>

    -   <span data-ttu-id="36ddc-122">Systèmes 32 bits :</span><span class="sxs-lookup"><span data-stu-id="36ddc-122">32-bit systems:</span></span>

        ```console
        "%windir%\Microsoft.NET\Framework\v3.0\Windows Communication Foundation\ServiceModelReg.exe" -i
        ```

    -   <span data-ttu-id="36ddc-123">Systèmes 64 bits :</span><span class="sxs-lookup"><span data-stu-id="36ddc-123">64-bit systems:</span></span>

        ```console
        "%windir%\Microsoft.NET\Framework64\v3.0\Windows Communication Foundation\ServiceModelReg.exe" -i
        ```

     <span data-ttu-id="36ddc-124">Cela permet de vérifier que Windows Communication Foundation (WCF) est inscrit sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36ddc-124">This makes sure that Windows Communication Foundation (WCF) is registered on the computer.</span></span>

10. <span data-ttu-id="36ddc-125">À partir de l'invite de commandes avec des privilèges d'administrateur, exécutez une des commandes suivantes (en fonction du système d'exploitation) :</span><span class="sxs-lookup"><span data-stu-id="36ddc-125">From the command prompt with administrator privileges, execute one of the following commands (depending on the operating system):</span></span>

    -   <span data-ttu-id="36ddc-126">Systèmes 32 bits :</span><span class="sxs-lookup"><span data-stu-id="36ddc-126">32-bit systems:</span></span>

        ```console
        "%windir%\Microsoft.NET\Framework\v4.0.30319\aspnet_regiis.exe" -i -enable
        ```

    -   <span data-ttu-id="36ddc-127">Systèmes 64 bits :</span><span class="sxs-lookup"><span data-stu-id="36ddc-127">64-bit systems:</span></span>

        ```console
        "%windir%\Microsoft.NET\Framework64\v4.0.30319\aspnet_regiis.exe" -i -enable
        ```

     <span data-ttu-id="36ddc-128">Cela permet de s'assurer qu'IIS s'exécute correctement après que WCF a été installé sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36ddc-128">This makes sure that IIS runs correctly after WCF has been installed on the computer.</span></span> <span data-ttu-id="36ddc-129">Vous devrez peut-être redémarrer IIS.</span><span class="sxs-lookup"><span data-stu-id="36ddc-129">You might have to also restart IIS.</span></span>

11. <span data-ttu-id="36ddc-130">Lorsque l'application ASP.NET s'exécute sur IIS7, vous devez aussi effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="36ddc-130">When the ASP.NET application runs on IIS7, you must also perform the following steps:</span></span>

    1. <span data-ttu-id="36ddc-131">Ouvrez le Gestionnaire des services Internet et accédez à l’application PhotoService sous **Site Web par défaut**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-131">Open IIS Manager and navigate to the PhotoService application under **Default Web Site**.</span></span>

    2. <span data-ttu-id="36ddc-132">Dans **affichage des fonctionnalités**, double-cliquez sur **authentification**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-132">In **Features View**, double-click **Authentication**.</span></span>

    3. <span data-ttu-id="36ddc-133">Sur le **authentification** page, sélectionnez **l’authentification anonyme**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-133">On the **Authentication** page, select **Anonymous Authentication**.</span></span>

    4. <span data-ttu-id="36ddc-134">Dans le **Actions** volet, cliquez sur **modifier** pour définir la sécurité du principal sous lequel les utilisateurs anonymes se connecteront au site.</span><span class="sxs-lookup"><span data-stu-id="36ddc-134">In the **Actions** pane, click **Edit** to set the security principal under which anonymous users will connect to the site.</span></span>

    5. <span data-ttu-id="36ddc-135">Dans le **modifier les informations d’identification d’authentification anonyme** boîte de dialogue, sélectionnez **identité du pool d’Application**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-135">In the **Edit Anonymous Authentication Credentials** dialog box, select **Application pool identity**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="36ddc-136">Lorsque vous utilisez le compte de service réseau, vous accordez aux utilisateurs anonymes l'accès à tout le réseau interne associé à ce compte.</span><span class="sxs-lookup"><span data-stu-id="36ddc-136">When you use the Network Service account, you grant anonymous users all the internal network access associated with that account.</span></span>

12. <span data-ttu-id="36ddc-137">En utilisant SQL Server Management Studio, l'utilitaire sqlcmd.exe ou l'Éditeur Transact-SQL dans Visual Studio, exécutez la commande Transact-SQL suivante sur l'instance SQL Server à laquelle la base de données Northwind est attachée :</span><span class="sxs-lookup"><span data-stu-id="36ddc-137">By using SQL Server Management Studio, the sqlcmd.exe utility, or the Transact-SQL Editor in Visual Studio, execute the following Transact-SQL command against the instance of SQL Server that has the Northwind database attached:</span></span>

    ```sql
    CREATE LOGIN [NT AUTHORITY\NETWORK SERVICE] FROM WINDOWS;
    GO
    ```

    <span data-ttu-id="36ddc-138">Cela crée une connexion dans l'instance SQL Server pour le compte Windows utilisé pour exécuter IIS.</span><span class="sxs-lookup"><span data-stu-id="36ddc-138">This creates a login in the SQL Server instance for the Windows account used to run IIS.</span></span> <span data-ttu-id="36ddc-139">Cela permet à IIS de se connecter à l'instance de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="36ddc-139">This enables IIS to connect to the SQL Server instance.</span></span>

13. <span data-ttu-id="36ddc-140">Avec la base de données Northwind attachée, exécutez les commandes Transact-SQL suivantes :</span><span class="sxs-lookup"><span data-stu-id="36ddc-140">With the Northwind database attached, execute the following Transact-SQL commands:</span></span>

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

    <span data-ttu-id="36ddc-141">Cela accorde des droits à la nouvelle connexion et permet à IIS de lire et d'écrire les données dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="36ddc-141">This grants rights to the new login, which enables IIS to read data from and write data to the Northwind database.</span></span>

## <a name="define-the-data-model"></a><span data-ttu-id="36ddc-142">Définir le modèle de données</span><span class="sxs-lookup"><span data-stu-id="36ddc-142">Define the data model</span></span>

1. <span data-ttu-id="36ddc-143">Dans **l’Explorateur de solutions**, cliquez sur le nom du projet ASP.NET, puis cliquez sur **ajouter** > **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-143">In **Solution Explorer**, right-click the name of the ASP.NET project, and then click **Add** > **New Item**.</span></span>

2. <span data-ttu-id="36ddc-144">Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez **ADO.NET Entity Data Model**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-144">In the **Add New Item** dialog box, select **ADO.NET Entity Data Model**.</span></span>

3. <span data-ttu-id="36ddc-145">Pour le nom du modèle de données, tapez `Northwind.edmx`.</span><span class="sxs-lookup"><span data-stu-id="36ddc-145">For the name of the data model, type `Northwind.edmx`.</span></span>

4. <span data-ttu-id="36ddc-146">Dans l’Assistant Entity Data Model, sélectionnez **générer à partir de la base de données**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-146">In the Entity Data Model Wizard, select **Generate from Database**, and then click **Next**.</span></span>

5. <span data-ttu-id="36ddc-147">Connectez le modèle de données à la base de données en effectuant l’une des étapes suivantes, puis cliquez sur **suivant**:</span><span class="sxs-lookup"><span data-stu-id="36ddc-147">Connect the data model to the database by doing one of the following steps, and then click **Next**:</span></span>

    -   <span data-ttu-id="36ddc-148">Si vous n’avez pas déjà configuré une connexion de base de données, cliquez sur **nouvelle connexion** et créer une nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="36ddc-148">If you do not have a database connection already configured, click **New Connection** and create a new connection.</span></span> <span data-ttu-id="36ddc-149">Pour plus d’informations, consultez [Comment : créer des connexions aux bases de données SQL Server](https://go.microsoft.com/fwlink/?LinkId=123631).</span><span class="sxs-lookup"><span data-stu-id="36ddc-149">For more information, see [How to: Create Connections to SQL Server Databases](https://go.microsoft.com/fwlink/?LinkId=123631).</span></span> <span data-ttu-id="36ddc-150">Cette instance SQL Server doit avoir l'exemple de base de données Northwind joint.</span><span class="sxs-lookup"><span data-stu-id="36ddc-150">This SQL Server instance must have the Northwind sample database attached.</span></span>

         <span data-ttu-id="36ddc-151">\- ou -</span><span class="sxs-lookup"><span data-stu-id="36ddc-151">\- or -</span></span>

    -   <span data-ttu-id="36ddc-152">Si vous avez une connexion de base de données déjà configurée pour vous connecter à la base de données Northwind, sélectionnez cette connexion dans la liste des connexions.</span><span class="sxs-lookup"><span data-stu-id="36ddc-152">If you have a database connection already configured to connect to the Northwind database, select that connection from the list of connections.</span></span>

6. <span data-ttu-id="36ddc-153">Dans la page finale de l'Assistant, activez les cases à cocher pour toutes les tables de la base de données puis désactivez les cases pour les vues et les procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="36ddc-153">On the final page of the wizard, select the check boxes for all tables in the database, and clear the check boxes for views and stored procedures.</span></span>

7. <span data-ttu-id="36ddc-154">Cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="36ddc-154">Click **Finish** to close the wizard.</span></span>

## <a name="create-the-data-service"></a><span data-ttu-id="36ddc-155">Créer le service de données</span><span class="sxs-lookup"><span data-stu-id="36ddc-155">Create the data service</span></span>

1. <span data-ttu-id="36ddc-156">Dans **l’Explorateur de solutions**, cliquez sur le nom de votre projet ASP.NET, puis cliquez sur **ajouter** > **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-156">In **Solution Explorer**, right-click the name of your ASP.NET project, and then click **Add** > **New Item**.</span></span>

2. <span data-ttu-id="36ddc-157">Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez **Service de données WCF**.</span><span class="sxs-lookup"><span data-stu-id="36ddc-157">In the **Add New Item** dialog box, select **WCF Data Service**.</span></span>

   ![Modèle d’élément de Service de données WCF dans Visual Studio 2015](media/wcf-data-service-item-template.png)

   > [!NOTE]
   > <span data-ttu-id="36ddc-159">Le **Service de données WCF** modèle est disponible dans Visual Studio 2015, mais pas dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="36ddc-159">The **WCF Data Service** template is available in Visual Studio 2015, but not in Visual Studio 2017.</span></span>

3. <span data-ttu-id="36ddc-160">Entrez le nom du service `Northwind`.</span><span class="sxs-lookup"><span data-stu-id="36ddc-160">For the name of the service, enter `Northwind`.</span></span>

     <span data-ttu-id="36ddc-161">Visual Studio crée le balisage XML et des fichiers de code pour le nouveau service.</span><span class="sxs-lookup"><span data-stu-id="36ddc-161">Visual Studio creates the XML markup and code files for the new service.</span></span> <span data-ttu-id="36ddc-162">La fenêtre de l'éditeur de code s'ouvre par défaut.</span><span class="sxs-lookup"><span data-stu-id="36ddc-162">By default, the code-editor window opens.</span></span> <span data-ttu-id="36ddc-163">Dans **l’Explorateur de solutions**, le service a le nom, Northwind et l’extension. svc.cs ou. svc.vb.</span><span class="sxs-lookup"><span data-stu-id="36ddc-163">In **Solution Explorer**, the service has the name, Northwind, and the extension .svc.cs or .svc.vb.</span></span>

4. <span data-ttu-id="36ddc-164">Dans le code du service de données, remplacez le commentaire `/* TODO: put your data source class name here */` dans la définition de la classe qui définit le service de données par le type qui est le conteneur d'entités du modèle de données, dans ce cas `NorthwindEntities`.</span><span class="sxs-lookup"><span data-stu-id="36ddc-164">In the code for the data service, replace the comment `/* TODO: put your data source class name here */` in the definition of the class that defines the data service with the type that is the entity container of the data model, which in this case is `NorthwindEntities`.</span></span> <span data-ttu-id="36ddc-165">La définition de classe doit ressembler aux éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="36ddc-165">The class definition should look this the following:</span></span>

     [!code-csharp[Astoria Quickstart Service#ServiceDefinition](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart service/cs/northwind.svc.cs#servicedefinition)]
     [!code-vb[Astoria Quickstart Service#ServiceDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart service/vb/northwind.svc.vb#servicedefinition)]

## <a name="see-also"></a><span data-ttu-id="36ddc-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36ddc-166">See also</span></span>

- [<span data-ttu-id="36ddc-167">Exposition de vos données comme service</span><span class="sxs-lookup"><span data-stu-id="36ddc-167">Exposing Your Data as a Service</span></span>](../../../../docs/framework/data/wcf/exposing-your-data-as-a-service-wcf-data-services.md)
