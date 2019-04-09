---
title: Données binaires et à valeurs élevées SQL Server
ms.date: 03/30/2017
ms.assetid: e00827b3-7511-4b2d-91d7-851ca86cc6b5
ms.openlocfilehash: 4b7a3f16726d6363cd702fb912bb7be281a25000
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59192964"
---
# <a name="sql-server-binary-and-large-value-data"></a>Données binaires et à valeurs élevées SQL Server
SQL Server fournit le spécificateur `max`, qui développe la capacité de stockage des types de données `varchar`, `nvarchar` et `varbinary`. `varchar(max)`, `nvarchar(max)`, et `varbinary(max)` sont appelés collectivement *les types de données de grande valeur*. Les types de données de valeur élevée permettent de stocker jusqu'à 2^31-1 octets de données.  
  
 SQL Server 2008 introduit l'attribut FILESTREAM, qui n'est pas un type de données, mais plutôt un attribut pouvant être défini sur une colonne et permettant alors de stocker des données de valeur élevée dans le système de fichiers et non dans la base de données.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Modification de données de valeurs élevées (max) dans ADO.NET](../../../../../docs/framework/data/adonet/sql/modifying-large-value-max-data.md)  
 Décrit comment utiliser les types de données de valeur volumineux.  
  
 [Données FILESTREAM](../../../../../docs/framework/data/adonet/sql/filestream-data.md)  
 Décrit comment utiliser les données de valeur élevée stockées dans SQL Server 2008 avec l'attribut FILESTREAM.  
  
## <a name="see-also"></a>Voir aussi

- [Types de données SQL Server et ADO.NET](../../../../../docs/framework/data/adonet/sql/sql-server-data-types.md)
- [Opérations de données SQL Server dans ADO.NET](../../../../../docs/framework/data/adonet/sql/sql-server-data-operations.md)
- [Extraction et modification de données dans ADO.NET](../../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
