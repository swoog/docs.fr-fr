---
title: Formuler des projections
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 745742df-0eda-479b-83f8-29bd8a80db96
ms.openlocfilehash: adf854429f2b13fd2421252a6281ad96d9d88500
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64655566"
---
# <a name="formulate-projections"></a>Formuler des projections
Les exemples suivants montrent comment la `select` instruction dans C# et `Select` instruction en Visual Basic peut être combinée avec d’autres fonctionnalités pour former des projections de requête.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Select` clause en Visual Basic (`select` clause dans C#) pour retourner une séquence de noms de contact pour `Customers`.  
  
 [!code-csharp[DLinqQueryExamples#57](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#57)]
 [!code-vb[DLinqQueryExamples#57](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#57)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Select` clause en Visual Basic (`select` clause dans C#) et *types anonymes* pour retourner une séquence de noms de contact et numéros de téléphone pour `Customers`.  
  
 [!code-csharp[DLinqQueryExamples#58](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#58)]
 [!code-vb[DLinqQueryExamples#58](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#58)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Select` clause en Visual Basic (`select` clause dans C#) et *types anonymes* pour retourner une séquence de noms et numéros de téléphone pour les employés. Le `FirstName` et `LastName` champs sont combinés en un seul champ (`Name`) et le `HomePhone` champ a été renommé en `Phone` dans la séquence résultante.  
  
 [!code-csharp[DLinqQueryExamples#59](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#59)]
 [!code-vb[DLinqQueryExamples#59](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#59)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Select` clause en Visual Basic (`select` clause dans C#) et *types anonymes* pour retourner une séquence de tous les `ProductID`s et une valeur calculée nommée `HalfPrice`. Cette valeur correspond à `UnitPrice` divisé par 2.  
  
 [!code-csharp[DLinqQueryExamples#60](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#60)]
 [!code-vb[DLinqQueryExamples#60](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#60)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Select` clause en Visual Basic (`select` clause dans C#) et un *instruction conditionnelle* pour retourner une séquence de nom de produit et la disponibilité du produit.  
  
 [!code-csharp[DLinqQueryExamples#61](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#61)]
 [!code-vb[DLinqQueryExamples#61](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#61)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise Visual Basic `Select` clause (`select` clause dans C#) et un *type connu* (nom) pour retourner une séquence des noms des employés.  
  
 [!code-csharp[DLinqQueryExamples#62](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#62)]
 [!code-vb[DLinqQueryExamples#62](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#62)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise `Select` et `Where` en Visual Basic (`select` et `where` dans C#) pour retourner un *séquence filtrée* de noms de contact pour les clients de Londres.  
  
 [!code-csharp[DLinqQueryExamples#63](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#63)]
 [!code-vb[DLinqQueryExamples#63](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#63)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un `Select` clause en Visual Basic (`select` clause dans C#) et *types anonymes* pour retourner un *en forme de sous-ensemble* des données sur les clients.  
  
 [!code-csharp[DLinqQueryExamples#64](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#64)]
 [!code-vb[DLinqQueryExamples#64](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#64)]  
  
## <a name="example"></a>Exemple  
 L'exemple suivant utilise des requêtes imbriquées pour retourner les résultats suivants :  
  
- Séquence de toutes les commandes et des `OrderID` correspondants.  
  
- Sous-séquence des éléments dans la commande pour laquelle il existe une remise.  
  
- Montant enregistré si le coût d'expédition n'est pas inclus.  
  
 [!code-csharp[DLinqQueryExamples#65](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#65)]
 [!code-vb[DLinqQueryExamples#65](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#65)]  
  
## <a name="see-also"></a>Voir aussi

- [Exemples de requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
