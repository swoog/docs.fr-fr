---
title: Obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET
description: Télécharger l’exemple de bases de données utilisés dans les exemples de code dans la documentation ADO.NET, ainsi que les outils SQL Server et de gestion
ms.date: 10/12/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 75ae1895d683b669f51b33130fc2f47010e39814
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347502"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a><span data-ttu-id="2cf9f-103">Obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET</span><span class="sxs-lookup"><span data-stu-id="2cf9f-103">Get the sample databases for ADO.NET code samples</span></span>

<span data-ttu-id="2cf9f-104">Un nombre d’exemples et procédures pas à pas dans le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation utilisent des bases de données et SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-104">A number of samples and walkthroughs in the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation use sample databases and SQL Server Express.</span></span> <span data-ttu-id="2cf9f-105">Vous pouvez télécharger ces produits gratuites à partir de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-105">You can download these products free of charge from Microsoft.</span></span>

## <a name="get-the-adventureworks-sample-database"></a><span data-ttu-id="2cf9f-106">Obtenir la base de données AdventureWorks</span><span class="sxs-lookup"><span data-stu-id="2cf9f-106">Get the AdventureWorks sample database</span></span>

<span data-ttu-id="2cf9f-107">Téléchargez la base de données AdventureWorks à partir du référentiel GitHub suivant :</span><span class="sxs-lookup"><span data-stu-id="2cf9f-107">Download the AdventureWorks sample database from the following GitHub repository:</span></span>

[<span data-ttu-id="2cf9f-108">Bases de données AdventureWorks</span><span class="sxs-lookup"><span data-stu-id="2cf9f-108">AdventureWorks sample databases</span></span>](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

<span data-ttu-id="2cf9f-109">Une fois que vous téléchargez un de la sauvegarde de base de données (\*.bak) des fichiers, restaurez la sauvegarde à une instance de SQL Server à l’aide de SQL Server Management Studio (SSMS).</span><span class="sxs-lookup"><span data-stu-id="2cf9f-109">After you download one of the database backup (\*.bak) files, restore the backup to an instance of SQL Server by using SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="2cf9f-110">Consultez [obtenir SQL Server Management Studio](#get_ssms).</span><span class="sxs-lookup"><span data-stu-id="2cf9f-110">See [Get SQL Server Management Studio](#get_ssms).</span></span>

## <a name="get-the-northwind-sample-database"></a><span data-ttu-id="2cf9f-111">Obtenir la base de données Northwind</span><span class="sxs-lookup"><span data-stu-id="2cf9f-111">Get the Northwind sample database</span></span>

<span data-ttu-id="2cf9f-112">Téléchargez la base de données Northwind à partir de la page suivante dans du Microsoft Download Center :</span><span class="sxs-lookup"><span data-stu-id="2cf9f-112">Download the Northwind sample database from the following page in the Microsoft Download Center:</span></span>

[<span data-ttu-id="2cf9f-113">Northwind and Pubs Sample Databases</span><span class="sxs-lookup"><span data-stu-id="2cf9f-113">Northwind and Pubs Sample Databases</span></span>](https://go.microsoft.com/fwlink?linkid=64296)

<span data-ttu-id="2cf9f-114">Une fois le fichier téléchargé, double-cliquez sur le fichier pour extraire les bases de données et les scripts.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-114">After the file has downloaded, double-click the file to extract the databases and scripts.</span></span> <span data-ttu-id="2cf9f-115">Par défaut, les fichiers sont installés dans le dossier `<drive>:\SQL Server 2000 Sample Databases`.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-115">By default, the files are installed in the folder `<drive>:\SQL Server 2000 Sample Databases`.</span></span>

<span data-ttu-id="2cf9f-116">Avant de pouvoir utiliser la base de données Northwind, vous devez effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf9f-116">Before you can use the Northwind database, you have to do one of the following things:</span></span>

- <span data-ttu-id="2cf9f-117">Recréer la base de données sur une instance de SQL Server en exécutant le `instnwnd.sql` fichier de script dans le dossier d’installation.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-117">Recreate the database on an instance of SQL Server by running the `instnwnd.sql` script file in the installation folder.</span></span>

- <span data-ttu-id="2cf9f-118">Attacher le `northwnd.mdf` fichier avec son correspondant `*.ldf` fichier journal à une instance de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-118">Attach the `northwnd.mdf` file with its corresponding `*.ldf` log file to an instance of SQL Server.</span></span>

## <a name="get_sql"></a> <span data-ttu-id="2cf9f-119">Obtenir SQL Server Express</span><span class="sxs-lookup"><span data-stu-id="2cf9f-119">Get SQL Server Express</span></span>

<span data-ttu-id="2cf9f-120">SQL Server Express est une édition gratuite d’entrée de gamme de SQL Server que vous pouvez redistribuer avec les applications.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-120">SQL Server Express is a free, entry-level edition of SQL Server that you can redistribute with applications.</span></span> <span data-ttu-id="2cf9f-121">Téléchargez SQL Server Express à partir de la page suivante :</span><span class="sxs-lookup"><span data-stu-id="2cf9f-121">Download SQL Server Express from the following page:</span></span>
  
[<span data-ttu-id="2cf9f-122">Éditions Express de SQL Server</span><span class="sxs-lookup"><span data-stu-id="2cf9f-122">SQL Server Express Editions</span></span>](https://www.microsoft.com/sql-server/sql-server-editions-express)

<span data-ttu-id="2cf9f-123">Si vous utilisez [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB est inclus dans l’édition Community, ainsi que les éditions Professional et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-123">If you're using [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB is included in the Community edition as well as the Professional and higher editions.</span></span>  

## <a name="get_ssms"></a> <span data-ttu-id="2cf9f-124">Obtenir SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="2cf9f-124">Get SQL Server Management Studio</span></span>
<span data-ttu-id="2cf9f-125">Si vous souhaitez afficher ou modifier une base de données que vous avez téléchargé, vous pouvez utiliser SQL Server Management Studio (SSMS).</span><span class="sxs-lookup"><span data-stu-id="2cf9f-125">If you want to view or modify a database that you've downloaded, you can use SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="2cf9f-126">Télécharger SSMS à partir de la page suivante :</span><span class="sxs-lookup"><span data-stu-id="2cf9f-126">Download SSMS from the following page:</span></span>

[<span data-ttu-id="2cf9f-127">Télécharger SQL Server Management Studio (SSMS)</span><span class="sxs-lookup"><span data-stu-id="2cf9f-127">Download SQL Server Management Studio (SSMS)</span></span>](/sql/ssms/download-sql-server-management-studio-ssms) 

<span data-ttu-id="2cf9f-128">Vous pouvez également afficher et gérer des bases de données dans l’environnement de développement intégré (IDE) Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-128">You can also view and manage databases in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="2cf9f-129">Dans [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), se connecter à la base de données à partir de **Explorateur d’objets SQL Server**, ou créer une connexion de données à la base de données **Explorateur de serveurs**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-129">In [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), connect to the database from **SQL Server Object Explorer**, or create a Data Connection to the database in **Server Explorer**.</span></span> <span data-ttu-id="2cf9f-130">Ouvrez ces volets Explorateur à partir de la **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-130">Open these explorer panes from the **View** menu.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cf9f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cf9f-131">See also</span></span>

- [<span data-ttu-id="2cf9f-132">Prise en main</span><span class="sxs-lookup"><span data-stu-id="2cf9f-132">Getting Started</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
