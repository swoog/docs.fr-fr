---
title: Obtenir les bases de données exemple SQL Server pour obtenir des exemples de code ADO.NET
description: Téléchargez les bases de données exemple SQL Server utilisées dans les exemples de code dans la documentation ADO.NET, ainsi que les outils SQL Server et de gestion
ms.date: 01/11/2019
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 5580f06f3d28ed6d70f75b619498ac8de7bc3326
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62037932"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a><span data-ttu-id="d8d9c-103">Obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET</span><span class="sxs-lookup"><span data-stu-id="d8d9c-103">Get the sample databases for ADO.NET code samples</span></span>

<span data-ttu-id="d8d9c-104">Un nombre d’exemples et procédures pas à pas dans le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation utilisent des bases de données exemple SQL Server et SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-104">A number of examples and walkthroughs in the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation use sample SQL Server databases and SQL Server Express.</span></span> <span data-ttu-id="d8d9c-105">Vous pouvez télécharger ces produits gratuites à partir de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-105">You can download these products free of charge from Microsoft.</span></span>

## <a name="get-the-northwind-sample-database-for-sql-server"></a><span data-ttu-id="d8d9c-106">Obtenir la base de données Northwind pour SQL Server</span><span class="sxs-lookup"><span data-stu-id="d8d9c-106">Get the Northwind sample database for SQL Server</span></span>

<span data-ttu-id="d8d9c-107">Téléchargez le script `instnwnd.sql` à partir du référentiel GitHub suivant pour créer et charger la base de données Northwind pour SQL Server :</span><span class="sxs-lookup"><span data-stu-id="d8d9c-107">Download the script `instnwnd.sql` from the following GitHub repository to create and load the Northwind sample database for SQL Server:</span></span>

[<span data-ttu-id="d8d9c-108">Données exemple Northwind et pubs pour Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="d8d9c-108">Northwind and pubs sample databases for Microsoft SQL Server</span></span>](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)

<span data-ttu-id="d8d9c-109">Avant de pouvoir utiliser la base de données Northwind, vous devez exécuter téléchargées `instnwnd.sql` fichier de script pour recréer la base de données sur une instance de SQL Server à l’aide de [SQL Server Management Studio](#get_ssms) ou un outil similaire.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-109">Before you can use the Northwind database, you have to run the downloaded `instnwnd.sql` script file to recreate the database on an instance of SQL Server by using [SQL Server Management Studio](#get_ssms) or a similar tool.</span></span> <span data-ttu-id="d8d9c-110">Suivez les instructions dans le fichier Lisez-moi dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-110">Follow the instructions in the Readme file in the repository.</span></span>

> [!TIP]
> <span data-ttu-id="d8d9c-111">Si vous avez besoin pour la base de données Northwind pour Microsoft Access, consultez [installer la base de données Northwind pour Microsoft Access](#northwind_access).</span><span class="sxs-lookup"><span data-stu-id="d8d9c-111">If you're looking for the Northwind database for Microsoft Access, see [Install the Northwind sample database for Microsoft Access](#northwind_access).</span></span>

## <a name="northwind_access"></a> <span data-ttu-id="d8d9c-112">Obtenir la base de données Northwind pour Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="d8d9c-112">Get the Northwind sample database for Microsoft Access</span></span>

<span data-ttu-id="d8d9c-113">La base de données Northwind pour Microsoft Access n’est pas disponible sur du Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-113">The Northwind sample database for Microsoft Access is not available on the Microsoft Download Center.</span></span> <span data-ttu-id="d8d9c-114">Pour installer Northwind directement à partir d’Access, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d8d9c-114">To install Northwind directly from within Access, do the following things:</span></span>

1. <span data-ttu-id="d8d9c-115">Ouvrir l’accès.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-115">Open Access.</span></span>

1. <span data-ttu-id="d8d9c-116">Entrée **Northwind** dans le **rechercher des modèles en ligne** zone, puis sélectionnez **entrée**.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-116">Enter **Northwind** in the **Search for Online Templates** box, and then select **Enter**.</span></span>

1. <span data-ttu-id="d8d9c-117">Dans l’écran des résultats, sélectionnez **Northwind**.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-117">On the results screen, select **Northwind**.</span></span> <span data-ttu-id="d8d9c-118">Une nouvelle fenêtre s’ouvre avec une description de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-118">A new window opens with a description of the Northwind database.</span></span>

1. <span data-ttu-id="d8d9c-119">Dans la nouvelle fenêtre, dans le **nom de fichier** texte Entrez un nom de fichier pour votre copie de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-119">In the new window, in the **File Name** text box, provide a filename for your copy of the Northwind database.</span></span>

1. <span data-ttu-id="d8d9c-120">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-120">Select **Create**.</span></span> <span data-ttu-id="d8d9c-121">Accès aux téléchargements de la base de données Northwind et prépare le fichier.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-121">Access downloads the Northwind database and prepares the file.</span></span>

1. <span data-ttu-id="d8d9c-122">Lorsque ce processus est terminé, la base de données s’ouvre avec un écran de bienvenue.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-122">When this process is complete, the database opens with a Welcome screen.</span></span>

## <a name="get-the-adventureworks-sample-database-for-sql-server"></a><span data-ttu-id="d8d9c-123">Obtenir la base de données AdventureWorks pour SQL Server</span><span class="sxs-lookup"><span data-stu-id="d8d9c-123">Get the AdventureWorks sample database for SQL Server</span></span>

<span data-ttu-id="d8d9c-124">Télécharger la base de données AdventureWorks pour SQL Server à partir du référentiel GitHub suivant :</span><span class="sxs-lookup"><span data-stu-id="d8d9c-124">Download the AdventureWorks sample database for SQL Server from the following GitHub repository:</span></span>

[<span data-ttu-id="d8d9c-125">Bases de données AdventureWorks</span><span class="sxs-lookup"><span data-stu-id="d8d9c-125">AdventureWorks sample databases</span></span>](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

<span data-ttu-id="d8d9c-126">Une fois que vous téléchargez un de la sauvegarde de base de données (\*.bak) des fichiers, restaurez la sauvegarde à une instance de SQL Server à l’aide de SQL Server Management Studio (SSMS).</span><span class="sxs-lookup"><span data-stu-id="d8d9c-126">After you download one of the database backup (\*.bak) files, restore the backup to an instance of SQL Server by using SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="d8d9c-127">Consultez [obtenir SQL Server Management Studio](#get_ssms).</span><span class="sxs-lookup"><span data-stu-id="d8d9c-127">See [Get SQL Server Management Studio](#get_ssms).</span></span>

## <a name="get_ssms"></a> <span data-ttu-id="d8d9c-128">Obtenir SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="d8d9c-128">Get SQL Server Management Studio</span></span>
<span data-ttu-id="d8d9c-129">Si vous souhaitez afficher ou modifier une base de données que vous avez téléchargé, vous pouvez utiliser SQL Server Management Studio (SSMS).</span><span class="sxs-lookup"><span data-stu-id="d8d9c-129">If you want to view or modify a database that you've downloaded, you can use SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="d8d9c-130">Télécharger SSMS à partir de la page suivante :</span><span class="sxs-lookup"><span data-stu-id="d8d9c-130">Download SSMS from the following page:</span></span>

[<span data-ttu-id="d8d9c-131">Télécharger SQL Server Management Studio (SSMS)</span><span class="sxs-lookup"><span data-stu-id="d8d9c-131">Download SQL Server Management Studio (SSMS)</span></span>](/sql/ssms/download-sql-server-management-studio-ssms) 

<span data-ttu-id="d8d9c-132">Vous pouvez également afficher et gérer des bases de données dans l’environnement de développement intégré (IDE) Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-132">You can also view and manage databases in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="d8d9c-133">Dans [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), se connecter à la base de données à partir de **Explorateur d’objets SQL Server**, ou créer une connexion de données à la base de données **Explorateur de serveurs**.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-133">In [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), connect to the database from **SQL Server Object Explorer**, or create a Data Connection to the database in **Server Explorer**.</span></span> <span data-ttu-id="d8d9c-134">Ouvrez ces volets Explorateur à partir de la **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-134">Open these explorer panes from the **View** menu.</span></span>

## <a name="get_sql"></a> <span data-ttu-id="d8d9c-135">Obtenir SQL Server Express</span><span class="sxs-lookup"><span data-stu-id="d8d9c-135">Get SQL Server Express</span></span>

<span data-ttu-id="d8d9c-136">SQL Server Express est une édition gratuite d’entrée de gamme de SQL Server que vous pouvez redistribuer avec les applications.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-136">SQL Server Express is a free, entry-level edition of SQL Server that you can redistribute with applications.</span></span> <span data-ttu-id="d8d9c-137">Téléchargez SQL Server Express à partir de la page suivante :</span><span class="sxs-lookup"><span data-stu-id="d8d9c-137">Download SQL Server Express from the following page:</span></span>
  
[<span data-ttu-id="d8d9c-138">SQL Server Express Edition</span><span class="sxs-lookup"><span data-stu-id="d8d9c-138">SQL Server Express Edition</span></span>](https://www.microsoft.com/sql-server/sql-server-editions-express)

<span data-ttu-id="d8d9c-139">Si vous utilisez [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB est inclus dans l’édition Community gratuite de Visual Studio, ainsi que les éditions Professional et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d8d9c-139">If you're using [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB is included in the free Community edition of Visual Studio, as well as the Professional and higher editions.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8d9c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8d9c-140">See also</span></span>

- [<span data-ttu-id="d8d9c-141">Prise en main</span><span class="sxs-lookup"><span data-stu-id="d8d9c-141">Getting Started</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
