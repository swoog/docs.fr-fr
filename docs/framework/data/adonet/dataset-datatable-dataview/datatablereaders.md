---
title: DataTableReaders
ms.date: 03/30/2017
ms.assetid: 97546ae2-0e42-4d26-961d-e0b244d81ded
ms.openlocfilehash: a790335a25327563e3dab6093449345b99afd048
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213999"
---
# <a name="datatablereaders"></a>DataTableReaders
L'objet <xref:System.Data.DataTableReader> présente le contenu d'un objet <xref:System.Data.DataTable> ou d'un objet <xref:System.Data.DataSet> sous la forme d'un ou plusieurs jeux de résultats en lecture seule et en avant uniquement.  
  
 Lorsque vous créez un **DataTableReader** à partir d’un **DataTable**, résultant **DataTableReader** objet contient un jeu de résultats avec les mêmes données que le  **DataTable** à partir de laquelle il a été créé, à l’exception de toutes les lignes qui ont été marquées comme supprimées. Les colonnes apparaissent dans le même ordre que dans la version d’origine **DataTable**.  
  
 Un **DataTableReader** peut contenir plusieurs jeux de résultats s’il a été créé en appelant <xref:System.Data.DataSet.CreateDataReader%2A>. Les résultats sont dans le même ordre que les **DataTables** dans le **DataSet** l’objet <xref:System.Data.DataSet.Tables%2A> collection.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Création d'un DataReader](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/creating-a-datareader.md)  
 Explique comment créer un **DataTableReader** objet.  
  
 [Navigation sur les DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/navigating-datatables.md)  
 Décrit l’utilisation de la **en lecture** méthode pour parcourir le contenu d’un **DataTableReader**.  
  
## <a name="see-also"></a>Voir aussi

- [Extraction et modification de données dans ADO.NET](../../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
