---
title: Utilisation des commandes pour modifier les données
ms.date: 03/30/2017
ms.assetid: f4160389-b9ff-4b74-b655-437c76dcd586
ms.openlocfilehash: cec079d16c6dc3d98cee9bf17b4201654e9ba10a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509265"
---
# <a name="using-commands-to-modify-data"></a>Utilisation des commandes pour modifier les données
À l'aide d'un fournisseur de données .NET Framework, vous pouvez exécuter des procédures stockées ou des instructions DDL (CREATE TABLE et ALTER COLUMN, par exemple) pour effectuer une manipulation de schéma sur une base de données ou un catalogue. Ces commandes ne retournent pas de lignes comme une requête le ferait, donc la **commande** objet fournit une **ExecuteNonQuery** à les traiter.  
  
 Outre l’utilisation de **ExecuteNonQuery** pour modifier le schéma, vous pouvez également utiliser cette méthode pour traiter les instructions SQL qui modifient les données mais ne pas retourner des lignes, telles que INSERT, UPDATE et DELETE.  
  
 Bien que les lignes ne sont pas retournées par la **ExecuteNonQuery** (méthode), entrée et sortie des paramètres et valeurs de retour peuvent être passés et retournés via la **paramètres** collection de la **commande**  objet.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Mise à jour des données dans une source de données](../../../../docs/framework/data/adonet/updating-data-in-a-data-source.md)  
 Décrit l'exécution de commandes ou de procédures stockées qui modifient les données dans une base de données.  
  
 [Exécution d’opérations du catalogue](../../../../docs/framework/data/adonet/performing-catalog-operations.md)  
 Décrit l'exécution des commandes qui modifient le schéma de base de données.  
  
## <a name="see-also"></a>Voir aussi
- [Extraction et modification de données dans ADO.NET](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
