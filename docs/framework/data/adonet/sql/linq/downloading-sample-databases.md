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
# <a name="get-the-sample-databases-for-adonet-code-samples"></a>Obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET

Un nombre d’exemples et procédures pas à pas dans le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation utilisent des bases de données exemple SQL Server et SQL Server Express. Vous pouvez télécharger ces produits gratuites à partir de Microsoft.

## <a name="get-the-northwind-sample-database-for-sql-server"></a>Obtenir la base de données Northwind pour SQL Server

Téléchargez le script `instnwnd.sql` à partir du référentiel GitHub suivant pour créer et charger la base de données Northwind pour SQL Server :

[Données exemple Northwind et pubs pour Microsoft SQL Server](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)

Avant de pouvoir utiliser la base de données Northwind, vous devez exécuter téléchargées `instnwnd.sql` fichier de script pour recréer la base de données sur une instance de SQL Server à l’aide de [SQL Server Management Studio](#get_ssms) ou un outil similaire. Suivez les instructions dans le fichier Lisez-moi dans le référentiel.

> [!TIP]
> Si vous avez besoin pour la base de données Northwind pour Microsoft Access, consultez [installer la base de données Northwind pour Microsoft Access](#northwind_access).

## <a name="northwind_access"></a> Obtenir la base de données Northwind pour Microsoft Access

La base de données Northwind pour Microsoft Access n’est pas disponible sur du Microsoft Download Center. Pour installer Northwind directement à partir d’Access, procédez comme suit :

1. Ouvrir l’accès.

1. Entrée **Northwind** dans le **rechercher des modèles en ligne** zone, puis sélectionnez **entrée**.

1. Dans l’écran des résultats, sélectionnez **Northwind**. Une nouvelle fenêtre s’ouvre avec une description de la base de données Northwind.

1. Dans la nouvelle fenêtre, dans le **nom de fichier** texte Entrez un nom de fichier pour votre copie de la base de données Northwind.

1. Sélectionnez **Créer**. Accès aux téléchargements de la base de données Northwind et prépare le fichier.

1. Lorsque ce processus est terminé, la base de données s’ouvre avec un écran de bienvenue.

## <a name="get-the-adventureworks-sample-database-for-sql-server"></a>Obtenir la base de données AdventureWorks pour SQL Server

Télécharger la base de données AdventureWorks pour SQL Server à partir du référentiel GitHub suivant :

[Bases de données AdventureWorks](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

Une fois que vous téléchargez un de la sauvegarde de base de données (\*.bak) des fichiers, restaurez la sauvegarde à une instance de SQL Server à l’aide de SQL Server Management Studio (SSMS). Consultez [obtenir SQL Server Management Studio](#get_ssms).

## <a name="get_ssms"></a> Obtenir SQL Server Management Studio
Si vous souhaitez afficher ou modifier une base de données que vous avez téléchargé, vous pouvez utiliser SQL Server Management Studio (SSMS). Télécharger SSMS à partir de la page suivante :

[Télécharger SQL Server Management Studio (SSMS)](/sql/ssms/download-sql-server-management-studio-ssms) 

Vous pouvez également afficher et gérer des bases de données dans l’environnement de développement intégré (IDE) Visual Studio. Dans [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), se connecter à la base de données à partir de **Explorateur d’objets SQL Server**, ou créer une connexion de données à la base de données **Explorateur de serveurs**. Ouvrez ces volets Explorateur à partir de la **vue** menu.

## <a name="get_sql"></a> Obtenir SQL Server Express

SQL Server Express est une édition gratuite d’entrée de gamme de SQL Server que vous pouvez redistribuer avec les applications. Téléchargez SQL Server Express à partir de la page suivante :
  
[SQL Server Express Edition](https://www.microsoft.com/sql-server/sql-server-editions-express)

Si vous utilisez [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB est inclus dans l’édition Community gratuite de Visual Studio, ainsi que les éditions Professional et versions ultérieures.  

## <a name="see-also"></a>Voir aussi

- [Prise en main](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
