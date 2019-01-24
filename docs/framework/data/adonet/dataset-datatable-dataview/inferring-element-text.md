---
title: Déduction du texte d'un élément
ms.date: 03/30/2017
ms.assetid: 789799e5-716f-459f-a168-76c5cf22178b
ms.openlocfilehash: d457985bfbec924748d1a418e318609b6837b9d2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745158"
---
# <a name="inferring-element-text"></a>Déduction du texte d'un élément
Si un élément contient du texte et ne contient aucun élément enfant à déduire en tant que tables telles que (éléments avec attributs) ou des éléments répétés, une nouvelle colonne portant le nom **TableName_Text** sera ajouté à la table qui est déduite pour l’élément. Le texte contenu dans l'élément sera ajouté à une ligne de la table et stocké dans la nouvelle colonne. Le **ColumnMapping** propriété de la nouvelle colonne est définie **MappingType.SimpleContent**.  
  
 Examinons, par exemple, le code XML suivant.  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1">Text1</Element1>  
</DocumentElement>  
```  
  
 Le processus d’inférence produira une table nommée **Element1** avec deux colonnes : **attr1** et **Element1_Text**. Le **ColumnMapping** propriété de la **attr1** jeu de colonnes **MappingType.Attribute**. Le **ColumnMapping** propriété de la **Element1_Text** jeu de colonnes **MappingType.SimpleContent**.  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|attr1|Element1_Text|  
|-----------|--------------------|  
|value1|Text1|  
  
 Si un élément contient du texte, mais possède également des éléments enfants contenant du texte, une colonne ne sera pas ajoutée à la table pour stocker le texte contenu dans l'élément. Ce texte sera ignoré, alors que le texte des éléments enfants sera inclus dans une ligne de la table. Examinons, par exemple, le code XML suivant.  
  
```xml  
<Element1>  
  Text1  
  <ChildElement1>Text2</ChildElement1>  
  Text3  
</Element1>  
```  
  
 Le processus d’inférence produira une table nommée **Element1** avec une colonne nommée **ChildElement1**. Le texte pour le **ChildElement1** élément figureront dans une ligne dans la table. L'autre texte sera ignoré. Le **ColumnMapping** propriété de la **ChildElement1** jeu de colonnes **MappingType.Element**.  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|ChildElement1|  
|-------------------|  
|Text2|  
  
## <a name="see-also"></a>Voir aussi
- [Inférence de la structure relationnelle d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [Chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [Chargement des informations de schéma de DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
