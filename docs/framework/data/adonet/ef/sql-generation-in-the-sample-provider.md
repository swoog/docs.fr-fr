---
title: Génération SQL dans le Fournisseur d'exemples
ms.date: 03/30/2017
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
ms.openlocfilehash: 5aa6e31cfc93a4ae1871da63f466864b4ea6f5d9
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149716"
---
# <a name="sql-generation-in-the-sample-provider"></a>Génération SQL dans le Fournisseur d'exemples
Le [Entity Framework Sample Provider](https://code.msdn.microsoft.com/windowsdesktop/Entity-Framework-Sample-6a9801d0) montre les nouveaux composants des fournisseurs de données ADO.NET qui prennent en charge la [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].  Il utilise une base de données SQL Server 2005 et est implémenté comme un wrapper pour le fournisseur de données System.Data.SqlClient ADO.NET 2.0.  
  
 Le module Génération SQL du Fournisseur d'exemples (situé sous le dossier Génération SQL, à l'exception du fichier DmlSqlGenerator.cs) prend un DbQueryCommandTree d'entrée et produit une instruction SQL SELECT unique.  
  
## <a name="in-this-section"></a>Dans cette section  
 Cette section comprend les rubriques suivantes :  
  
 [Architecture et conception](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [Procédure pas à pas : Génération SQL](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Génération SQL](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
