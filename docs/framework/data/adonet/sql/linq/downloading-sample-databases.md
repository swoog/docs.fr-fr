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
# <a name="get-the-sample-databases-for-adonet-code-samples"></a>Obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET

Un nombre d’exemples et procédures pas à pas dans le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation utilisent des bases de données et SQL Server Express. Vous pouvez télécharger ces produits gratuites à partir de Microsoft.

## <a name="get-the-adventureworks-sample-database"></a>Obtenir la base de données AdventureWorks

Téléchargez la base de données AdventureWorks à partir du référentiel GitHub suivant :

[Bases de données AdventureWorks](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

Une fois que vous téléchargez un de la sauvegarde de base de données (\*.bak) des fichiers, restaurez la sauvegarde à une instance de SQL Server à l’aide de SQL Server Management Studio (SSMS). Consultez [obtenir SQL Server Management Studio](#get_ssms).

## <a name="get-the-northwind-sample-database"></a>Obtenir la base de données Northwind

Téléchargez la base de données Northwind à partir de la page suivante dans du Microsoft Download Center :

[Northwind and Pubs Sample Databases](https://go.microsoft.com/fwlink?linkid=64296)

Une fois le fichier téléchargé, double-cliquez sur le fichier pour extraire les bases de données et les scripts. Par défaut, les fichiers sont installés dans le dossier `<drive>:\SQL Server 2000 Sample Databases`.

Avant de pouvoir utiliser la base de données Northwind, vous devez effectuer l’une des opérations suivantes :

- Recréer la base de données sur une instance de SQL Server en exécutant le `instnwnd.sql` fichier de script dans le dossier d’installation.

- Attacher le `northwnd.mdf` fichier avec son correspondant `*.ldf` fichier journal à une instance de SQL Server.

## <a name="get_sql"></a> Obtenir SQL Server Express

SQL Server Express est une édition gratuite d’entrée de gamme de SQL Server que vous pouvez redistribuer avec les applications. Téléchargez SQL Server Express à partir de la page suivante :
  
[Éditions Express de SQL Server](https://www.microsoft.com/sql-server/sql-server-editions-express)

Si vous utilisez [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB est inclus dans l’édition Community, ainsi que les éditions Professional et versions ultérieures.  

## <a name="get_ssms"></a> Obtenir SQL Server Management Studio
Si vous souhaitez afficher ou modifier une base de données que vous avez téléchargé, vous pouvez utiliser SQL Server Management Studio (SSMS). Télécharger SSMS à partir de la page suivante :

[Télécharger SQL Server Management Studio (SSMS)](/sql/ssms/download-sql-server-management-studio-ssms) 

Vous pouvez également afficher et gérer des bases de données dans l’environnement de développement intégré (IDE) Visual Studio. Dans [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), se connecter à la base de données à partir de **Explorateur d’objets SQL Server**, ou créer une connexion de données à la base de données **Explorateur de serveurs**. Ouvrez ces volets Explorateur à partir de la **vue** menu.
  
## <a name="see-also"></a>Voir aussi

- [Prise en main](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
