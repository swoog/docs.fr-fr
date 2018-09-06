---
title: Utilisation des commandes pour modifier les données
ms.date: 03/30/2017
ms.assetid: f4160389-b9ff-4b74-b655-437c76dcd586
ms.openlocfilehash: 6388eecb2e96970f47383b61985d672bd0419a1e
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43773424"
---
# <a name="using-commands-to-modify-data"></a><span data-ttu-id="7a327-102">Utilisation des commandes pour modifier les données</span><span class="sxs-lookup"><span data-stu-id="7a327-102">Using Commands to Modify Data</span></span>
<span data-ttu-id="7a327-103">À l'aide d'un fournisseur de données .NET Framework, vous pouvez exécuter des procédures stockées ou des instructions DDL (CREATE TABLE et ALTER COLUMN, par exemple) pour effectuer une manipulation de schéma sur une base de données ou un catalogue.</span><span class="sxs-lookup"><span data-stu-id="7a327-103">Using a .NET Framework data provider, you can execute stored procedures or data definition language statements (for example, CREATE TABLE and ALTER COLUMN) to perform schema manipulation on a database or catalog.</span></span> <span data-ttu-id="7a327-104">Ces commandes ne retournent pas de lignes comme une requête le ferait, donc la **commande** objet fournit une **ExecuteNonQuery** à les traiter.</span><span class="sxs-lookup"><span data-stu-id="7a327-104">These commands do not return rows as a query would, so the **Command** object provides an **ExecuteNonQuery** to process them.</span></span>  
  
 <span data-ttu-id="7a327-105">Outre l’utilisation de **ExecuteNonQuery** pour modifier le schéma, vous pouvez également utiliser cette méthode pour traiter les instructions SQL qui modifient les données mais ne pas retourner des lignes, telles que INSERT, UPDATE et DELETE.</span><span class="sxs-lookup"><span data-stu-id="7a327-105">In addition to using **ExecuteNonQuery** to modify schema, you can also use this method to process SQL statements that modify data but that do not return rows, such as INSERT, UPDATE, and DELETE.</span></span>  
  
 <span data-ttu-id="7a327-106">Bien que les lignes ne sont pas retournées par la **ExecuteNonQuery** (méthode), entrée et sortie des paramètres et valeurs de retour peuvent être passés et retournés via la **paramètres** collection de la **commande**  objet.</span><span class="sxs-lookup"><span data-stu-id="7a327-106">Although rows are not returned by the **ExecuteNonQuery** method, input and output parameters and return values can be passed and returned via the **Parameters** collection of the **Command** object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7a327-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7a327-107">In This Section</span></span>  
 [<span data-ttu-id="7a327-108">Mise à jour des données dans une source de données</span><span class="sxs-lookup"><span data-stu-id="7a327-108">Updating Data in a Data Source</span></span>](../../../../docs/framework/data/adonet/updating-data-in-a-data-source.md)  
 <span data-ttu-id="7a327-109">Décrit l'exécution de commandes ou de procédures stockées qui modifient les données dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="7a327-109">Describes how to execute commands or stored procedures that modify data in a database.</span></span>  
  
 [<span data-ttu-id="7a327-110">Exécution d’opérations du catalogue</span><span class="sxs-lookup"><span data-stu-id="7a327-110">Performing Catalog Operations</span></span>](../../../../docs/framework/data/adonet/performing-catalog-operations.md)  
 <span data-ttu-id="7a327-111">Décrit l'exécution des commandes qui modifient le schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="7a327-111">Describes how to execute commands that modify database schema.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a327-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a327-112">See Also</span></span>  
 [<span data-ttu-id="7a327-113">Extraction et modification de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="7a327-113">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [<span data-ttu-id="7a327-114">Commandes et paramètres</span><span class="sxs-lookup"><span data-stu-id="7a327-114">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 [<span data-ttu-id="7a327-115">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="7a327-115">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
