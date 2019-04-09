---
title: Limitations des inférences
ms.date: 03/30/2017
ms.assetid: 78517994-5d57-44f8-9d20-38812977de09
ms.openlocfilehash: 308d2ffdd9e2cb16626861e25613657f341a4ccb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59076237"
---
# <a name="inference-limitations"></a><span data-ttu-id="89c98-102">Limitations des inférences</span><span class="sxs-lookup"><span data-stu-id="89c98-102">Inference Limitations</span></span>
<span data-ttu-id="89c98-103">Le processus d'inférence d'un schéma de l'objet <xref:System.Data.DataSet> à partir de XML peut aboutir à des schémas différents en fonction des éléments XML figurant dans chaque document.</span><span class="sxs-lookup"><span data-stu-id="89c98-103">The process of inferring a <xref:System.Data.DataSet> schema from XML can result in different schemas depending on the XML elements in each document.</span></span> <span data-ttu-id="89c98-104">Examinons, par exemple, les documents XML suivants.</span><span class="sxs-lookup"><span data-stu-id="89c98-104">For example, consider the following XML documents.</span></span>  
  
 <span data-ttu-id="89c98-105">Document1 :</span><span class="sxs-lookup"><span data-stu-id="89c98-105">Document1:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element1>Text2</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="89c98-106">Document2 :</span><span class="sxs-lookup"><span data-stu-id="89c98-106">Document2:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="89c98-107">Pour « Document1 », le processus d’inférence produit un **DataSet** nommé « DocumentElement » et une table nommée « Element1 » car « Element1 » est un élément récurrent.</span><span class="sxs-lookup"><span data-stu-id="89c98-107">For "Document1," the inference process produces a **DataSet** named "DocumentElement" and a table named "Element1," because "Element1" is a repeating element.</span></span>  
  
 <span data-ttu-id="89c98-108">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="89c98-108">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="89c98-109">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="89c98-109">**Table:** Element1</span></span>  
  
|<span data-ttu-id="89c98-110">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="89c98-110">Element1_Text</span></span>|  
|--------------------|  
|<span data-ttu-id="89c98-111">Text1</span><span class="sxs-lookup"><span data-stu-id="89c98-111">Text1</span></span>|  
|<span data-ttu-id="89c98-112">Text2</span><span class="sxs-lookup"><span data-stu-id="89c98-112">Text2</span></span>|  
  
 <span data-ttu-id="89c98-113">Toutefois, pour « Document2 », le processus d’inférence produit un **DataSet** nommé « NewDataSet » et une table nommée « DocumentElement ».</span><span class="sxs-lookup"><span data-stu-id="89c98-113">However, for "Document2," the inference process produces a **DataSet** named "NewDataSet" and a table named "DocumentElement."</span></span> <span data-ttu-id="89c98-114">« Element1 » est déduit en tant que colonne car il n'a ni attribut, ni élément enfant.</span><span class="sxs-lookup"><span data-stu-id="89c98-114">"Element1" is inferred as a column because it has no attributes and no child elements.</span></span>  
  
 <span data-ttu-id="89c98-115">**Jeu de données :** NewDataSet</span><span class="sxs-lookup"><span data-stu-id="89c98-115">**DataSet:** NewDataSet</span></span>  
  
 <span data-ttu-id="89c98-116">**Table :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="89c98-116">**Table:** DocumentElement</span></span>  
  
|<span data-ttu-id="89c98-117">Element1</span><span class="sxs-lookup"><span data-stu-id="89c98-117">Element1</span></span>|  
|--------------|  
|<span data-ttu-id="89c98-118">Text1</span><span class="sxs-lookup"><span data-stu-id="89c98-118">Text1</span></span>|  
  
 <span data-ttu-id="89c98-119">Ces deux documents XML peuvent avoir été conçus de manière à produire le même schéma, mais le processus d'inférence donne des résultats très différents en fonction des éléments contenus dans chaque document.</span><span class="sxs-lookup"><span data-stu-id="89c98-119">These two XML documents may have been intended to produce the same schema, but the inference process produces very different results based on the elements contained in each document.</span></span>  
  
 <span data-ttu-id="89c98-120">Pour éviter les différences qui peuvent se produire lors de la génération de schéma à partir d’un document XML, nous vous recommandons de spécifier explicitement un schéma à l’aide du langage de définition de schéma XML (XSD) ou (XML-Data Reduced) lors du chargement d’un **DataSet** à partir de XML.</span><span class="sxs-lookup"><span data-stu-id="89c98-120">To avoid the discrepancies that can occur when generating schema from an XML document, we recommend that you explicitly specify a schema using XML Schema definition language (XSD) or XML-Data Reduced (XDR) when loading a **DataSet** from XML.</span></span> <span data-ttu-id="89c98-121">Pour plus d’informations sur la spécification explicite un **DataSet** schéma avec un schéma XML, consultez [dérivation Structure relationnelle des DataSet à partir de XSD (XML Schema)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/deriving-dataset-relational-structure-from-xml-schema-xsd.md).</span><span class="sxs-lookup"><span data-stu-id="89c98-121">For more information about explicitly specifying a **DataSet** schema with XML Schema, see [Deriving DataSet Relational Structure from XML Schema (XSD)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/deriving-dataset-relational-structure-from-xml-schema-xsd.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89c98-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89c98-122">See also</span></span>

- [<span data-ttu-id="89c98-123">Déduction de la structure relationnelle des DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="89c98-123">Inferring DataSet Relational Structure from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="89c98-124">Chargement d'un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="89c98-124">Loading a DataSet from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [<span data-ttu-id="89c98-125">Chargement des informations de schéma de DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="89c98-125">Loading DataSet Schema Information from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="89c98-126">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="89c98-126">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [<span data-ttu-id="89c98-127">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="89c98-127">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="89c98-128">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="89c98-128">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
