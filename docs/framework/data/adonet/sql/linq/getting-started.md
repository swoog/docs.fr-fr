---
title: Prise en main
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: db8a557a-fef8-4f4f-bb91-8cff7250ee25
ms.openlocfilehash: 17b014a5a56a2c60359f6fb0b60df29feb97f2a7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43419023"
---
# <a name="getting-started"></a>Prise en main
À l’aide de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], vous pouvez utiliser le [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] bases de données de la technologie pour accéder à SQL tout comme vous accéderiez à une collection en mémoire.  
  
 Par exemple, l'objet `nw` dans le code suivant est créé pour représenter la base de données `Northwind`, la table `Customers` est ciblée, les lignes sont filtrées sur `Customers` à partir de `London`, et une chaîne pour `CompanyName` est sélectionnée pour la récupération.  
  
 Lors de l'exécution de la boucle, la collection de valeurs `CompanyName` est récupérée.  
  
 [!code-csharp[DLinqGettingStarted#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqGettingStarted/cs/Program.cs#1)]
 [!code-vb[DLinqGettingStarted#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqGettingStarted/vb/Module1.vb#1)]  
  
## <a name="next-steps"></a>Étapes suivantes  
 Pour plus d’exemples, y compris l’insertion et la mise à jour, consultez [ce que vous pouvez faire avec LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/what-you-can-do-with-linq-to-sql.md).  
  
 Suivez ensuite des procédures pas à pas et des didacticiels pour bénéficier d'une expérience pratique de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]. Consultez [apprentissage par les procédures pas à pas](../../../../../../docs/framework/data/adonet/sql/linq/learning-by-walkthroughs.md).  
  
 Enfin, découvrez comment prendre en main votre propre [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] projet en lisant [les étapes classiques pour l’aide de LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/typical-steps-for-using-linq-to-sql.md).  
  
## <a name="see-also"></a>Voir aussi  
 [LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/index.md)  
 [Introduction à LINQ](https://msdn.microsoft.com/library/24dddf19-12a0-4707-a4bc-eba4fa7f219e)  
 [Modèle objet LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
