---
title: LINQ to DataSet
ms.date: 03/30/2017
ms.assetid: 743e3755-3ecb-45a2-8d9b-9ed41f0dcf17
ms.openlocfilehash: 8a16e3fe0cea04813be50a83f906170199e78e3e
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="linq-to-dataset"></a>LINQ to DataSet
[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] facilite et accélère l'interrogation de données mises en cache dans un objet <xref:System.Data.DataSet>. Plus précisément, [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] simplifie l’interrogation en permettant aux développeurs d’écrire des requêtes dans le langage de programmation, à la place d’à l’aide d’un langage de requête distincte. Cela est particulièrement utile pour les développeurs de Visual Studio, qui peuvent désormais tirer parti de la vérification de la syntaxe de la compilation, les types statiques et prise en charge de IntelliSense fournis par Visual Studio dans les requêtes.  
  
 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] peut également être utilisé pour interroger des données qui ont été consolidées à partir d'une ou plusieurs sources de données. Cela permet plusieurs scénarios qui requièrent de la flexibilité dans la manière dont les données sont représentées et gérées, comme l'interrogation de données agrégées localement et la mise en cache en couche intermédiaire dans les applications Web. En particulier, les applications génériques de création de rapports, d'analyse et de business intelligence requièrent cette méthode de manipulation.  
  
 Le [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] fonctionnalité est exposée principalement via les méthodes d’extension dans le <xref:System.Data.DataRowExtensions> et <xref:System.Data.DataTableExtensions> classes. [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] s’appuie sur et utilise existants [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] architecture et n’est pas censé remplacer [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] dans le code d’application. Le code ADO.NET 2.0 existant continuera à fonctionner dans une application [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]. La relation de [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] avec [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] et le magasin de données est illustrée dans le diagramme suivant.  
  
 ![LINQ to DataSet est basé sur le fournisseur ADO.NET](../../../../docs/framework/data/adonet/media/linqtodataset.gif "LINQtoDataSet")  
  
## <a name="in-this-section"></a>Dans cette section  
 [Prise en main](../../../../docs/framework/data/adonet/getting-started-linq-to-dataset.md)  
  
 [Guide de programmation](../../../../docs/framework/data/adonet/programming-guide-linq-to-dataset.md)  
  
## <a name="reference"></a>Référence  
 <xref:System.Data.DataTableExtensions>  
  
 <xref:System.Data.DataRowExtensions>  
  
 <xref:System.Data.DataRowComparer>  
  
## <a name="see-also"></a>Voir aussi  
 [LINQ (Language Integrated Query)](http://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)  
 [LINQ et ADO.NET](../../../../docs/framework/data/adonet/linq-and-ado-net.md)  
 [ADO.NET](../../../../docs/framework/data/adonet/index.md)
