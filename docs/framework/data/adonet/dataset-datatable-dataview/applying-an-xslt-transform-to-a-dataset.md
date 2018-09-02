---
title: Application d'une transformation XSLT à un DataSet
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 09f2e4ee-1d08-4ba8-8936-83394fee319d
ms.openlocfilehash: abcb3231aa92bd62edefc7f7341da5fcb3321e4b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405746"
---
# <a name="applying-an-xslt-transform-to-a-dataset"></a><span data-ttu-id="d8406-102">Application d'une transformation XSLT à un DataSet</span><span class="sxs-lookup"><span data-stu-id="d8406-102">Applying an XSLT Transform to a DataSet</span></span>
<span data-ttu-id="d8406-103">Le **WriteXml** méthode de la <xref:System.Data.DataSet> vous permet d’écrire le contenu d’un **DataSet** en tant que données XML.</span><span class="sxs-lookup"><span data-stu-id="d8406-103">The **WriteXml** method of the <xref:System.Data.DataSet> enables you to write the contents of a **DataSet** as XML data.</span></span> <span data-ttu-id="d8406-104">La tâche qui suit généralement consiste à transformer ce XML en un autre format à l’aide de transformations XSL (XSLT).</span><span class="sxs-lookup"><span data-stu-id="d8406-104">A common task is to then transform that XML to another format using XSL transformations (XSLT).</span></span> <span data-ttu-id="d8406-105">Toutefois, la synchronisation un **DataSet** avec un <xref:System.Xml.XmlDataDocument> vous permet d’appliquer une feuille de style XSLT au contenu d’un **DataSet** sans devoir d’abord écrire le contenu de la  **Jeu de données** en tant que données XML à l’aide **WriteXml**.</span><span class="sxs-lookup"><span data-stu-id="d8406-105">However, synchronizing a **DataSet** with an <xref:System.Xml.XmlDataDocument> enables you to apply an XSLT stylesheet to the contents of a **DataSet** without having to first write the contents of the **DataSet** as XML data using **WriteXml**.</span></span>  
  
 <span data-ttu-id="d8406-106">L’exemple suivant remplit un **DataSet** avec des tables et des relations, synchronise le **DataSet** avec un **XmlDataDocument**, puis écrit une partie de la  **Jeu de données** sous la forme d’un élément HTML fichier à l’aide d’une feuille de style XSLT.</span><span class="sxs-lookup"><span data-stu-id="d8406-106">The following example populates a **DataSet** with tables and relationships, synchronizes the **DataSet** with an **XmlDataDocument**, and writes a portion of the **DataSet** as an HTML file using an XSLT stylesheet.</span></span> <span data-ttu-id="d8406-107">Le contenu de la feuille de style XSLT vous est présenté ci-après.</span><span class="sxs-lookup"><span data-stu-id="d8406-107">Following are the contents of the XSLT stylesheet.</span></span>  
  
```xml  
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">  
  
<xsl:template match="CustomerOrders">  
  <HTML>  
  <STYLE>  
  BODY {font-family:verdana;font-size:9pt}  
  TD   {font-size:8pt}  
  </STYLE>  
    <BODY>  
    <TABLE BORDER="1">  
      <xsl:apply-templates select="Customers"/>  
    </TABLE>  
    </BODY>  
  </HTML>  
</xsl:template>  
  
<xsl:template match="Customers">  
    <TR><TD>  
      <xsl:value-of select="ContactName"/>, <xsl:value-of select="Phone"/><BR/>  
    </TD></TR>  
      <xsl:apply-templates select="Orders"/>  
</xsl:template>  
  
<xsl:template match="Orders">  
  <TABLE BORDER="1">  
    <TR><TD valign="top"><B>Order:</B></TD><TD valign="top"><xsl:value-of select="OrderID"/></TD></TR>  
    <TR><TD valign="top"><B>Date:</B></TD><TD valign="top"><xsl:value-of select="OrderDate"/></TD></TR>  
    <TR><TD valign="top"><B>Ship To:</B></TD>  
        <TD valign="top"><xsl:value-of select="ShipName"/><BR/>  
        <xsl:value-of select="ShipAddress"/><BR/>  
        <xsl:value-of select="ShipCity"/>, <xsl:value-of select="ShipRegion"/>  <xsl:value-of select="ShipPostalCode"/><BR/>  
        <xsl:value-of select="ShipCountry"/></TD></TR>  
  </TABLE>  
</xsl:template>  
  
</xsl:stylesheet>  
```  
  
 <span data-ttu-id="d8406-108">Le code suivant remplit la **DataSet** et applique la feuille de style XSLT.</span><span class="sxs-lookup"><span data-stu-id="d8406-108">The following code fills the **DataSet** and applies the XSLT style sheet.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d8406-109">Si vous appliquez une feuille de style XSLT à un **DataSet** qui contient des relations, vous obtiendrez de meilleures performances si vous définissez la **Nested** propriété de la <xref:System.Data.DataRelation> à **true**pour chaque relation imbriquée.</span><span class="sxs-lookup"><span data-stu-id="d8406-109">If you are applying an XSLT style sheet to a **DataSet** that contains relations, you achieve best performance if you set the **Nested** property of the <xref:System.Data.DataRelation> to **true** for each nested relation.</span></span> <span data-ttu-id="d8406-110">Cela vous permet d’utiliser les feuilles de style XSLT qui implémentent un traitement naturel vertical pour naviguer dans la hiérarchie et transformer les données, au lieu de recourir aux axes de localisation XPath exigeants en performances (par exemple, frère précédent et frère suivant dans les expressions de test de nœud de feuille de style) pour y naviguer.</span><span class="sxs-lookup"><span data-stu-id="d8406-110">This allows you to use XSLT style sheets that implement natural top-down processing to navigate the hierarchy and transform the data, as opposed to using performance-intensive XPath location axes (for example, preceding-sibling and following-sibling in style sheet node test expressions) to navigate it.</span></span> <span data-ttu-id="d8406-111">Pour plus d’informations sur les relations imbriquées, consultez [d’imbrication de DataRelations](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md).</span><span class="sxs-lookup"><span data-stu-id="d8406-111">For more information on nested relations, see [Nesting DataRelations](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md).</span></span>  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim dataSet As DataSet = New DataSet("CustomerOrders")  
  
Dim customerAdapter As SqlDataAdapter = New SqlDataAdapter( _  
  "SELECT * FROM Customers", connection)  
customerAdapter.Fill(dataSet, "Customers")  
  
Dim orderAdapter As SqlDataAdapter = New SqlDataAdapter( _  
  "SELECT * FROM Orders", connection)  
orderAdapter.Fill(dataSet, "Orders")  
  
connection.Close()  
  
dataSet.Relations.Add("CustOrders", _  
dataSet.Tables("Customers").Columns("CustomerID"), _  
dataSet.Tables("Orders").Columns("CustomerID")).Nested = true  
  
Dim xmlDoc As XmlDataDocument = New XmlDataDocument(dataSet)   
  
Dim xslTran As XslTransform = New XslTransform  
xslTran.Load("transform.xsl")  
  
Dim writer As XmlTextWriter = New XmlTextWriter( _  
  "xslt_output.html", System.Text.Encoding.UTF8)  
  
xslTran.Transform(xmlDoc, Nothing, writer)  
writer.Close()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
connection.Open();  
  
DataSet custDS = new DataSet("CustomerDataSet");  
  
SqlDataAdapter customerAdapter = new SqlDataAdapter(  
  "SELECT * FROM Customers", connection);  
customerAdapter.Fill(custDS, "Customers");  
  
SqlDataAdapter orderAdapter = new SqlDataAdapter(  
  "SELECT * FROM Orders", connection);  
orderAdapter.Fill(custDS, "Orders");  
  
connection.Close();  
  
custDS.Relations.Add("CustOrders",  
  custDS.Tables["Customers"].Columns["CustomerID"],  
                     custDS.Tables["Orders"].Columns["CustomerID"]).Nested = true;  
  
XmlDataDocument xmlDoc = new XmlDataDocument(custDS);   
  
XslTransform xslTran = new XslTransform();  
xslTran.Load("transform.xsl");  
  
XmlTextWriter writer = new XmlTextWriter("xslt_output.html",   
  System.Text.Encoding.UTF8);  
  
xslTran.Transform(xmlDoc, null, writer);  
writer.Close();  
```  
  
## <a name="see-also"></a><span data-ttu-id="d8406-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8406-112">See Also</span></span>  
 [<span data-ttu-id="d8406-113">Synchronisation DataSet et XmlDataDocument</span><span class="sxs-lookup"><span data-stu-id="d8406-113">DataSet and XmlDataDocument Synchronization</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataset-and-xmldatadocument-synchronization.md)  
 [<span data-ttu-id="d8406-114">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="d8406-114">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
