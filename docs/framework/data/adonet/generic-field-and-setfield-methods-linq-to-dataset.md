---
title: Méthodes génériques Field et SetField (LINQ to DataSet)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1883365f-9d6c-4ccb-9187-df309f47706d
ms.openlocfilehash: 7c7f1fef5d1fa575cd6d3bfdb7e6cbbea79ade28
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59086011"
---
# <a name="generic-field-and-setfield-methods-linq-to-dataset"></a>Méthodes génériques Field et SetField (LINQ to DataSet)
[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] Fournit des méthodes d’extension pour le <xref:System.Data.DataRow> classe pour accéder aux valeurs de colonne : la <xref:System.Data.DataRowExtensions.Field%2A> (méthode) et le <xref:System.Data.DataRowExtensions.SetField%2A> (méthode). Ces méthodes facilitent l'accès des développeurs aux valeurs de colonne, particulièrement pour les valeurs Null. Le <xref:System.Data.DataSet> utilise <xref:System.DBNull.Value> pour représenter les valeurs Null, alors que [!INCLUDE[vbteclinq](../../../../includes/vbteclinq-md.md)] utilise la prise en charge de type Nullable introduite dans [!INCLUDE[dnprdnlong](../../../../includes/dnprdnlong-md.md)]. À l’aide de l’accesseur de colonne existant dans <xref:System.Data.DataRow> , vous devez effectuer un cast de l’objet de retour vers le type approprié. Si un champ particulier dans un <xref:System.Data.DataRow> peut être null, vous devez vérifier explicitement une valeur null, car le renvoi <xref:System.DBNull.Value> et effectuer implicitement un cast vers un autre type lève une <xref:System.InvalidCastException>. Dans l’exemple suivant, si le <xref:System.Data.DataRow.IsNull%2A> méthode n’était pas utilisée pour rechercher une valeur null, une exception serait levée si l’indexeur retournait <xref:System.DBNull.Value> et a tenté d’effectuer un cast en un <xref:System.String>.  
  
 [!code-csharp[DP LINQ to DataSet Examples#WhereIsNull](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#whereisnull)]
 [!code-vb[DP LINQ to DataSet Examples#WhereIsNull](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#whereisnull)]  
  
 La méthode <xref:System.Data.DataRowExtensions.Field%2A> donne accès aux valeurs de colonne d'un <xref:System.Data.DataRow> et le <xref:System.Data.DataRowExtensions.SetField%2A> définit les valeurs de colonne dans un <xref:System.Data.DataRow>. Les deux méthodes <xref:System.Data.DataRowExtensions.Field%2A> et <xref:System.Data.DataRowExtensions.SetField%2A> gèrent des types Nullable, ce qui fait que vous n'avez pas à vérifier explicitement les valeurs Null comme dans l'exemple précédent. Les deux méthodes sont également des méthodes génériques, ce qui fait que vous n’avez pas à effectuer un cast du type de retour.  
  
 L'exemple suivant utilise la méthode <xref:System.Data.DataRowExtensions.Field%2A>.  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where3](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where3)]
 [!code-vb[DP LINQ to DataSet Examples#Where3](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where3)]  
  
 Notez que le type de données spécifié dans le paramètre générique `T` de la méthode <xref:System.Data.DataRowExtensions.Field%2A> et de la méthode <xref:System.Data.DataRowExtensions.SetField%2A> doit correspondre au type de la valeur sous-jacente, sinon une exception <xref:System.InvalidCastException> est levée. Le nom de la colonne spécifiée doit également correspondre à celui de la colonne dans le <xref:System.Data.DataSet>, sinon une <xref:System.ArgumentException> est levée. Dans les deux cas, l'exception est levée au moment de l'exécution pendant l'énumération des données lorsque la requête est exécutée.  
  
 La méthode <xref:System.Data.DataRowExtensions.SetField%2A> n'effectue aucune conversion de type. Toutefois, cela ne signifie pas qu'une conversion de type ne se produira pas. Le <xref:System.Data.DataRowExtensions.SetField%2A> méthode expose le [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] comportement de la <xref:System.Data.DataRow> classe. Une conversion de type pourrait être exécutée par le <xref:System.Data.DataRow> objet et la valeur convertie seraient enregistrées ensuite à la <xref:System.Data.DataRow> objet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.DataRowExtensions>
