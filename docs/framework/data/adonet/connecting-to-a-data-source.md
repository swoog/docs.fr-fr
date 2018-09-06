---
title: Connexion à une source de données dans ADO.NET
ms.date: 03/30/2017
ms.assetid: 9abc3f92-1be3-4e1a-b360-762dc689650e
ms.openlocfilehash: f5788b9b0b19f32d03c917575db7b3f40324c0a2
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44031724"
---
# <a name="connecting-to-a-data-source-in-adonet"></a>Connexion à une source de données dans ADO.NET
Dans ADO.NET, vous utilisez un **connexion** objet pour se connecter à une source de données spécifique en fournissant des informations d’authentification nécessaires dans une chaîne de connexion. Le **connexion** objet que vous utilisez varie selon le type de source de données.  
  
 Chaque fournisseur de données .NET Framework inclut dans le .NET Framework comprend un objet <xref:System.Data.Common.DbConnection> : le fournisseur de données .ENT Framework pour OLE DB inclut un objet <xref:System.Data.OleDb.OleDbConnection>, le fournisseur de données .NET Framework pour SQL Server inclut un objet <xref:System.Data.SqlClient.SqlConnection>, le fournisseur de données .NET Framework pour ODBC inclut un objet <xref:System.Data.Odbc.OdbcConnection> et le fournisseur de données .NET Framework pour Oracle inclut un objet <xref:System.Data.OracleClient.OracleConnection>.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Établissement de la connexion](../../../../docs/framework/data/adonet/establishing-the-connection.md)  
 Décrit comment utiliser un **connexion** objet pour établir une connexion à une source de données.  
  
 [Événements de connexion](../../../../docs/framework/data/adonet/connection-events.md)  
 Décrit comment utiliser un **InfoMessage** événement afin de récupérer les messages d’information à partir d’une source de données.  
  
## <a name="see-also"></a>Voir aussi  
 [Chaînes de connexion](../../../../docs/framework/data/adonet/connection-strings.md)  
 [Regroupement de connexions](../../../../docs/framework/data/adonet/connection-pooling.md)  
 [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)  
 [Transactions et accès concurrentiel](../../../../docs/framework/data/adonet/transactions-and-concurrency.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
