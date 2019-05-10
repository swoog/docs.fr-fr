---
title: Déduction de tables
ms.date: 03/30/2017
ms.assetid: 74a288d4-b8e9-4f1a-b2cd-10df92c1ed1f
ms.openlocfilehash: 174d305688c7090c163df60a11e233aea24b8f79
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64587362"
---
# <a name="inferring-tables"></a>Déduction de tables
Lors de l'inférence du schéma d'un objet <xref:System.Data.DataSet> à partir d'un document XML, ADO.NET identifie d'abord les éléments XML qui représentent des tables. Les structures XML suivantes donneront une table pour le **DataSet** schéma :  
  
- éléments avec attributs ;  
  
- éléments avec éléments enfants ;  
  
- éléments qui se répètent.  
  
## <a name="elements-with-attributes"></a>Éléments avec attributs  
 Les éléments contenant des attributs spécifiés donnent des tables déduites. Examinons, par exemple, le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1"/>  
  <Element1 attr1="value2">Text1</Element1>  
</DocumentElement>  
```  
  
 Le processus d'inférence produit une table nommée « Element1 ».  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|attr1|Element1_Text|  
|-----------|--------------------|  
|valeur1||  
|valeur2|Text1|  
  
## <a name="elements-with-child-elements"></a>Éléments avec éléments enfants  
 Les éléments possédant des éléments enfants donnent des tables déduites. Examinons, par exemple, le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1>Text1</ChildElement1>  
  </Element1>  
</DocumentElement>  
```  
  
 Le processus d'inférence produit une table nommée « Element1 ».  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|ChildElement1|  
|-------------------|  
|Text1|  
  
 L'élément document, ou racine, donne une table déduite s'il comporte des attributs ou des éléments enfants qui sont inférés en tant que colonnes. Si l’élément document ne comporte pas d’attributs et pas d’éléments enfants qui seraient déduits en tant que colonnes, il est déduit en tant qu’un **DataSet**. Examinons, par exemple, le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element2>Text2</Element2>  
</DocumentElement>  
```  
  
 Le processus d'inférence produit une table nommée « DocumentElement ».  
  
 **Jeu de données :** NewDataSet  
  
 **Table :** DocumentElement  
  
|Element1|Element2|  
|--------------|--------------|  
|Text1|Text2|  
  
 Examinons également le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1" attr2="value2"/>  
</DocumentElement>  
```  
  
 Le processus d’inférence produit un **DataSet** nommée « DocumentElement » contenant une table nommée « Element1 ».  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|attr1|attr2|  
|-----------|-----------|  
|valeur1|valeur2|  
  
## <a name="repeating-elements"></a>Éléments qui se répètent  
 Les éléments qui se répètent donnent une seule table déduite. Examinons, par exemple, le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element1>Text2</Element1>  
</DocumentElement>  
```  
  
 Le processus d'inférence produit une table nommée « Element1 ».  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|Element1_Text|  
|--------------------|  
|Text1|  
|Text2|  
  
## <a name="see-also"></a>Voir aussi

- [Inférence de la structure relationnelle d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [Chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [Chargement des informations de schéma de DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
