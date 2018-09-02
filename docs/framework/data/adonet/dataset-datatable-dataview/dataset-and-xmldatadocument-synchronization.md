---
title: Synchronisation DataSet et XmlDataDocument
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0ce3793d-54b2-47e4-8cf7-b0591cc4dd21
ms.openlocfilehash: 54991234d4eaa9edab218d3b0d221a6e477d2be5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43420101"
---
# <a name="dataset-and-xmldatadocument-synchronization"></a>Synchronisation DataSet et XmlDataDocument
L'objet <xref:System.Data.DataSet> ADO.NET vous propose une représentation relationnelle des données. Pour un accès hiérarchique aux données, vous pouvez utiliser les classes XML disponibles dans le .NET Framework. Pour des raisons historiques, ces deux représentations des données ont jusqu'à présent été utilisées séparément. Toutefois, le .NET Framework permet un accès synchrone et en temps réel aux représentations relationnelles et hiérarchiques des données via le **DataSet** objet et le <xref:System.Xml.XmlDataDocument> de l’objet, respectivement.  
  
 Quand un **DataSet** est synchronisé avec un **XmlDataDocument**, les deux objets fonctionnent avec un seul jeu de données. Cela signifie que si une modification est apportée à la **DataSet**, la modification est répercutée dans le **XmlDataDocument**et vice versa. La relation entre la **DataSet** et **XmlDataDocument** crée une grande souplesse en permettant à une application unique, à l’aide d’un jeu unique de données, pour accéder à la suite complète de services intégrés autour du **DataSet** (par exemple, les contrôles Web Forms et Windows Forms et les concepteurs de Visual Studio .NET), ainsi que la suite de services XML, y compris la feuille de style XSL (Extensible Language), XSLT (XSL Transformations) et chemin d’accès XML Language (XPath). Vous n'avez pas à choisir l'ensemble de services que l'application devra utiliser, puisque les deux sont disponibles.  
  
 Il existe plusieurs méthodes que vous pouvez synchroniser un **DataSet** avec un **XmlDataDocument**. Vous pouvez :  
  
-   Remplir un **DataSet** avec schéma (autrement dit, une structure relationnelle) et les données, puis le synchroniser avec un nouveau **XmlDataDocument**. Vous obtenez ainsi une vue hiérarchique des données relationnelles existantes. Exemple :  
  
    ```vb  
    Dim dataSet As DataSet = New DataSet  
  
    ' Add code here to populate the DataSet with schema and data.  
  
    Dim xmlDoc As XmlDataDocument = New XmlDataDocument(dataSet)  
    ```  
  
    ```csharp  
    DataSet dataSet = new DataSet();  
  
    // Add code here to populate the DataSet with schema and data.  
  
    XmlDataDocument xmlDoc = new XmlDataDocument(dataSet);  
    ```  
  
-   Remplir un **jeu de données** avec schéma uniquement (tels que fortement typé **DataSet**), synchroniser avec un **XmlDataDocument**, puis chargez le  **XmlDataDocument** à partir d’un document XML. Vous obtenez ainsi une vue relationnelle des données hiérarchiques existantes. Les noms de table et les noms de colonnes dans votre **DataSet** schéma doit correspondre aux noms des éléments XML que vous voulez les synchroniser. Cette mise en correspondance respecte la casse.  
  
     Notez que le schéma de la **DataSet** suffit faire correspondre les éléments XML que vous souhaitez exposer dans votre vue relationnelle. De cette façon, vous pouvez disposer d'un document XML très volumineux et d'une toute petite « fenêtre » relationnelle sur ce document. Le **XmlDataDocument** conserve l’ensemble du document XML, bien que le **DataSet** expose uniquement une petite partie de celui-ci. (Pour un exemple détaillé, consultez [synchronisation d’un DataSet avec un XmlDataDocument](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/synchronizing-a-dataset-with-an-xmldatadocument.md).)  
  
     L’exemple de code suivant montre les étapes de création d’un **DataSet** remplissage de son schéma, puis sa synchronisation avec un **XmlDataDocument**. Notez que le **DataSet** schéma ne doit faire correspondre les éléments à partir de la **XmlDataDocument** que vous souhaitez exposer à l’aide la **DataSet**.  
  
    ```vb  
    Dim dataSet As DataSet = New DataSet  
  
    ' Add code here to populate the DataSet with schema, but not data.  
  
    Dim xmlDoc As XmlDataDocument = New XmlDataDocument(dataSet)  
    xmlDoc.Load("XMLDocument.xml")  
    ```  
  
    ```csharp  
    DataSet dataSet = new DataSet();  
  
    // Add code here to populate the DataSet with schema, but not data.  
  
    XmlDataDocument xmlDoc = new XmlDataDocument(dataSet);  
    xmlDoc.Load("XMLDocument.xml");  
    ```  
  
     Impossible de charger un **XmlDataDocument** s’il est synchronisé avec un **DataSet** qui contient les données. Une exception sera levée.  
  
-   Créer un nouveau **XmlDataDocument** et charger à partir d’un document XML, puis accéder à la vue relationnelle des données à l’aide la **DataSet** propriété de la **XmlDataDocument**. Vous devez définir le schéma de la **DataSet** avant de pouvoir afficher les données dans le **XmlDataDocument** à l’aide de la **DataSet**. Là encore, les noms de table et de la colonne de noms dans votre **DataSet** schéma doit correspondre aux noms des éléments XML que vous voulez les synchroniser. Cette mise en correspondance respecte la casse.  
  
     L’exemple de code suivant montre comment accéder à la vue relationnelle des données dans un **XmlDataDocument**.  
  
    ```vb  
    Dim xmlDoc As XmlDataDocument = New XmlDataDocument  
    Dim dataSet As DataSet = xmlDoc.DataSet  
  
    ' Add code here to create the schema of the DataSet to view the data.  
  
    xmlDoc.Load("XMLDocument.xml")  
    ```  
  
    ```csharp  
    XmlDataDocument xmlDoc = new XmlDataDocument();  
    DataSet dataSet = xmlDoc.DataSet;  
  
    // Add code here to create the schema of the DataSet to view the data.  
  
    xmlDoc.Load("XMLDocument.xml");  
    ```  
  
 Un autre avantage de la synchronisation d’un **XmlDataDocument** avec un **DataSet** préserver la fidélité d’un document XML. Si le **DataSet** est remplie à partir d’un document XML en utilisant **ReadXml**, lorsque les données sont réécrites sous un document XML en utilisant **WriteXml** peut différer considérablement de la document XML d’origine. Il s’agit, car le **DataSet** ne conserve pas la mise en forme, telles que des espaces blancs ou des informations hiérarchiques, comme l’ordre des éléments, à partir du document XML. Le **DataSet** ne contient pas les éléments du document XML qui ont été ignorés parce qu’ils ne correspondaient pas le schéma de la **Dataset**. Synchronisation d’un **XmlDataDocument** avec un **DataSet** permet la mise en forme et élément la structure hiérarchique du document XML d’origine doivent être conservées dans le **XmlDataDocument**, tandis que le **DataSet** contient uniquement des informations données et le schéma appropriées à la **DataSet**.  
  
 Lors de la synchronisation une **DataSet** avec un **XmlDataDocument**, résultats peuvent différer selon s’il faut ou non votre <xref:System.Data.DataRelation> sont les objets imbriqués. Pour plus d’informations, consultez [d’imbrication de DataRelations](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Synchronisation d’un DataSet et d’un XmlDataDocument](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/synchronizing-a-dataset-with-an-xmldatadocument.md)  
 Montre comment synchroniser fortement typé **DataSet**, avec un schéma minimal, avec un **XmlDataDocument**.  
  
 [Exécution d’une requête XPath sur un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/performing-an-xpath-query-on-a-dataset.md)  
 Présente l’exécution d’une requête XPath sur le contenu d’un **DataSet**.  
  
 [Application d’une transformation XSLT à un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/applying-an-xslt-transform-to-a-dataset.md)  
 Montre comment appliquer une transformation XSLT au contenu d’un **DataSet**.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)  
 Décrit comment la **DataSet** interagit avec XML comme source de données, y compris le chargement et la persistance du contenu d’un **DataSet** en tant que données XML.  
  
 [Imbrication de DataRelations](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md)  
 Explique l’importance des imbriquée **DataRelation** objets lorsqu’il représente le contenu d’un **DataSet** en tant que données XML et décrit comment créer ces relations.  
  
 [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 Décrit le **DataSet** et comment l’utiliser pour gérer les données d’application et d’interagir avec les sources de données, y compris les bases de données relationnelles et XML.  
  
 <xref:System.Xml.XmlDataDocument>  
 Contient des informations de référence sur les **XmlDataDocument** classe.  
  
## <a name="see-also"></a>Voir aussi  
 [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
