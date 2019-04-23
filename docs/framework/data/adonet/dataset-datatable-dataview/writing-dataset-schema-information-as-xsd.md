---
title: Écriture des informations de schéma de DataSet comme XSD
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4e530831-695e-49ff-8f0b-e5b0c526b8eb
ms.openlocfilehash: 8403f9d9be88f34e473fd3512f5499193245d227
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59099441"
---
# <a name="writing-dataset-schema-information-as-xsd"></a><span data-ttu-id="e4236-102">Écriture des informations de schéma de DataSet comme XSD</span><span class="sxs-lookup"><span data-stu-id="e4236-102">Writing DataSet Schema Information as XSD</span></span>
<span data-ttu-id="e4236-103">Vous pouvez écrire le schéma d'un objet <xref:System.Data.DataSet> sous la forme d'un schéma en langage XSD (XML Schema Definition), de façon à pouvoir le transporter, avec ou sans les données connexes, dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="e4236-103">You can write the schema of a <xref:System.Data.DataSet> as XML Schema definition language (XSD) schema, so that you can transport it, with or without related data, in an XML document.</span></span> <span data-ttu-id="e4236-104">Schéma XML peut être écrit dans un fichier, un flux, un <xref:System.Xml.XmlWriter>, ou une chaîne ; il est utile pour générer un fortement typée **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="e4236-104">XML Schema can be written to a file, a stream, an <xref:System.Xml.XmlWriter>, or a string; it is useful for generating a strongly typed **DataSet**.</span></span> <span data-ttu-id="e4236-105">Pour plus d’informations sur fortement typées **DataSet** , consultez [typés](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md).</span><span class="sxs-lookup"><span data-stu-id="e4236-105">For more information about strongly typed **DataSet** objects, see [Typed DataSets](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md).</span></span>  
  
 <span data-ttu-id="e4236-106">Vous pouvez spécifier la façon dont une colonne d’une table est représentée dans le schéma XML à l’aide de la **ColumnMapping** propriété de la <xref:System.Data.DataColumn> objet.</span><span class="sxs-lookup"><span data-stu-id="e4236-106">You can specify how a column of a table is represented in XML Schema using the **ColumnMapping** property of the <xref:System.Data.DataColumn> object.</span></span> <span data-ttu-id="e4236-107">Pour plus d’informations, consultez « Mappage de colonnes de texte, des attributs et des éléments XML » dans [contenu du jeu de données écrit en tant que données XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/writing-dataset-contents-as-xml-data.md).</span><span class="sxs-lookup"><span data-stu-id="e4236-107">For more information, see "Mapping Columns to XML Elements, Attributes, and Text" in [Writing DataSet Contents as XML Data](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/writing-dataset-contents-as-xml-data.md).</span></span>  
  
 <span data-ttu-id="e4236-108">Pour écrire le schéma d’un **DataSet** en tant que schéma XML, dans un fichier, flux, ou **XmlWriter**, utiliser le **WriteXmlSchema** méthode de la **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="e4236-108">To write the schema of a **DataSet** as XML Schema, to a file, stream, or **XmlWriter**, use the **WriteXmlSchema** method of the **DataSet**.</span></span> <span data-ttu-id="e4236-109">**WriteXmlSchema** accepte un paramètre qui spécifie la destination du schéma XML qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="e4236-109">**WriteXmlSchema** takes one parameter that specifies the destination of the resulting XML Schema.</span></span> <span data-ttu-id="e4236-110">Les exemples de code suivants montrent comment écrire le schéma XML d’un **DataSet** dans un fichier en passant une chaîne contenant un nom de fichier et un <xref:System.IO.StreamWriter> objet.</span><span class="sxs-lookup"><span data-stu-id="e4236-110">The following code examples demonstrate how to write the XML Schema of a **DataSet** to a file by passing a string containing a file name and a <xref:System.IO.StreamWriter> object.</span></span>  
  
```vb  
dataSet.WriteXmlSchema("Customers.xsd")  
```  
  
```csharp  
dataSet.WriteXmlSchema("Customers.xsd");  
```  
  
```vb  
Dim writer As System.IO.StreamWriter = New System.IO.StreamWriter("Customers.xsd")  
dataSet.WriteXmlSchema(writer)  
writer.Close()  
```  
  
```csharp  
System.IO.StreamWriter writer = new System.IO.StreamWriter("Customers.xsd");  
dataSet.WriteXmlSchema(writer);  
writer.Close();  
```  
  
 <span data-ttu-id="e4236-111">Pour obtenir le schéma d’un **DataSet** et écrivez-le en tant que chaîne de schéma XML, utilisez la **GetXmlSchema** méthode, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e4236-111">To obtain the schema of a **DataSet** and write it as an XML Schema string, use the **GetXmlSchema** method, as shown in the following example.</span></span>  
  
```vb  
Dim schemaString As String = dataSet.GetXmlSchema()  
```  
  
```csharp  
string schemaString = dataSet.GetXmlSchema();  
```  
  
## <a name="see-also"></a><span data-ttu-id="e4236-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4236-112">See also</span></span>

- [<span data-ttu-id="e4236-113">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="e4236-113">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [<span data-ttu-id="e4236-114">Écriture du contenu d’un DataSet comme données XML</span><span class="sxs-lookup"><span data-stu-id="e4236-114">Writing DataSet Contents as XML Data</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/writing-dataset-contents-as-xml-data.md)
- [<span data-ttu-id="e4236-115">Datasets typés</span><span class="sxs-lookup"><span data-stu-id="e4236-115">Typed DataSets</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md)
- [<span data-ttu-id="e4236-116">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="e4236-116">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="e4236-117">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="e4236-117">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
