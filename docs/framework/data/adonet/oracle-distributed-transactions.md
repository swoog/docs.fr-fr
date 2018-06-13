---
title: Transactions distribuées Oracle
ms.date: 03/30/2017
ms.assetid: c340ca81-ef79-402f-b204-c5156b890fe5
ms.openlocfilehash: 0e9dcb30eb1962071d7154d4bbf929871c8a12d2
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32765199"
---
# <a name="oracle-distributed-transactions"></a>Transactions distribuées Oracle
L'objet <xref:System.Data.OracleClient.OracleConnection> s'inscrit automatiquement dans une transaction distribuée existante s'il détermine qu'une transaction est active. L'inscription automatique dans une transaction se produit lorsque la connexion est ouverte et extraite du pool de connexions. Vous pouvez désactiver l'inscription automatique dans des transactions existantes en spécifiant  
  
```  
Enlist=false  
```  
  
 comme paramètre de chaîne de connexion pour un <xref:System.Data.OracleClient.OracleConnection>.  
  
## <a name="see-also"></a>Voir aussi  
 [Oracle et ADO.NET](../../../../docs/framework/data/adonet/oracle-and-adonet.md)  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](http://go.microsoft.com/fwlink/?LinkId=217917)
