---
title: Déduction de tables
ms.date: 03/30/2017
ms.assetid: 74a288d4-b8e9-4f1a-b2cd-10df92c1ed1f
ms.openlocfilehash: 2c2a93d413f301dc3006b701e4bc7979a3fa7a1d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181829"
---
# <a name="inferring-tables"></a><span data-ttu-id="66ce3-102">Déduction de tables</span><span class="sxs-lookup"><span data-stu-id="66ce3-102">Inferring Tables</span></span>
<span data-ttu-id="66ce3-103">Lors de l'inférence du schéma d'un objet <xref:System.Data.DataSet> à partir d'un document XML, ADO.NET identifie d'abord les éléments XML qui représentent des tables.</span><span class="sxs-lookup"><span data-stu-id="66ce3-103">When inferring a schema for a <xref:System.Data.DataSet> from an XML document, ADO.NET first determines which XML elements represent tables.</span></span> <span data-ttu-id="66ce3-104">Les structures XML suivantes donneront une table pour le **DataSet** schéma :</span><span class="sxs-lookup"><span data-stu-id="66ce3-104">The following XML structures result in a table for the **DataSet** schema:</span></span>  
  
-   <span data-ttu-id="66ce3-105">éléments avec attributs ;</span><span class="sxs-lookup"><span data-stu-id="66ce3-105">Elements with attributes</span></span>  
  
-   <span data-ttu-id="66ce3-106">éléments avec éléments enfants ;</span><span class="sxs-lookup"><span data-stu-id="66ce3-106">Elements with child elements</span></span>  
  
-   <span data-ttu-id="66ce3-107">éléments qui se répètent.</span><span class="sxs-lookup"><span data-stu-id="66ce3-107">Repeating elements</span></span>  
  
## <a name="elements-with-attributes"></a><span data-ttu-id="66ce3-108">Éléments avec attributs</span><span class="sxs-lookup"><span data-stu-id="66ce3-108">Elements with Attributes</span></span>  
 <span data-ttu-id="66ce3-109">Les éléments contenant des attributs spécifiés donnent des tables déduites.</span><span class="sxs-lookup"><span data-stu-id="66ce3-109">Elements that have attributes specified in them result in inferred tables.</span></span> <span data-ttu-id="66ce3-110">Examinons, par exemple, le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="66ce3-110">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1"/>  
  <Element1 attr1="value2">Text1</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="66ce3-111">Le processus d'inférence produit une table nommée « Element1 ».</span><span class="sxs-lookup"><span data-stu-id="66ce3-111">The inference process produces a table named "Element1."</span></span>  
  
 <span data-ttu-id="66ce3-112">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="66ce3-112">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="66ce3-113">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="66ce3-113">**Table:** Element1</span></span>  
  
|<span data-ttu-id="66ce3-114">attr1</span><span class="sxs-lookup"><span data-stu-id="66ce3-114">attr1</span></span>|<span data-ttu-id="66ce3-115">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="66ce3-115">Element1_Text</span></span>|  
|-----------|--------------------|  
|<span data-ttu-id="66ce3-116">valeur1</span><span class="sxs-lookup"><span data-stu-id="66ce3-116">value1</span></span>||  
|<span data-ttu-id="66ce3-117">valeur2</span><span class="sxs-lookup"><span data-stu-id="66ce3-117">value2</span></span>|<span data-ttu-id="66ce3-118">Text1</span><span class="sxs-lookup"><span data-stu-id="66ce3-118">Text1</span></span>|  
  
## <a name="elements-with-child-elements"></a><span data-ttu-id="66ce3-119">Éléments avec éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66ce3-119">Elements with Child Elements</span></span>  
 <span data-ttu-id="66ce3-120">Les éléments possédant des éléments enfants donnent des tables déduites.</span><span class="sxs-lookup"><span data-stu-id="66ce3-120">Elements that have child elements result in inferred tables.</span></span> <span data-ttu-id="66ce3-121">Examinons, par exemple, le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="66ce3-121">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1>Text1</ChildElement1>  
  </Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="66ce3-122">Le processus d'inférence produit une table nommée « Element1 ».</span><span class="sxs-lookup"><span data-stu-id="66ce3-122">The inference process produces a table named "Element1."</span></span>  
  
 <span data-ttu-id="66ce3-123">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="66ce3-123">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="66ce3-124">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="66ce3-124">**Table:** Element1</span></span>  
  
|<span data-ttu-id="66ce3-125">ChildElement1</span><span class="sxs-lookup"><span data-stu-id="66ce3-125">ChildElement1</span></span>|  
|-------------------|  
|<span data-ttu-id="66ce3-126">Text1</span><span class="sxs-lookup"><span data-stu-id="66ce3-126">Text1</span></span>|  
  
 <span data-ttu-id="66ce3-127">L'élément document, ou racine, donne une table déduite s'il comporte des attributs ou des éléments enfants qui sont inférés en tant que colonnes.</span><span class="sxs-lookup"><span data-stu-id="66ce3-127">The document, or root, element result in an inferred table if it has attributes or child elements that are inferred as columns.</span></span> <span data-ttu-id="66ce3-128">Si l’élément document ne comporte pas d’attributs et pas d’éléments enfants qui seraient déduits en tant que colonnes, il est déduit en tant qu’un **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="66ce3-128">If the document element has no attributes and no child elements that would be inferred as columns, the element is inferred as a **DataSet**.</span></span> <span data-ttu-id="66ce3-129">Examinons, par exemple, le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="66ce3-129">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element2>Text2</Element2>  
</DocumentElement>  
```  
  
 <span data-ttu-id="66ce3-130">Le processus d'inférence produit une table nommée « DocumentElement ».</span><span class="sxs-lookup"><span data-stu-id="66ce3-130">The inference process produces a table named "DocumentElement."</span></span>  
  
 <span data-ttu-id="66ce3-131">**Jeu de données :** NewDataSet</span><span class="sxs-lookup"><span data-stu-id="66ce3-131">**DataSet:** NewDataSet</span></span>  
  
 <span data-ttu-id="66ce3-132">**Table :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="66ce3-132">**Table:** DocumentElement</span></span>  
  
|<span data-ttu-id="66ce3-133">Element1</span><span class="sxs-lookup"><span data-stu-id="66ce3-133">Element1</span></span>|<span data-ttu-id="66ce3-134">Element2</span><span class="sxs-lookup"><span data-stu-id="66ce3-134">Element2</span></span>|  
|--------------|--------------|  
|<span data-ttu-id="66ce3-135">Text1</span><span class="sxs-lookup"><span data-stu-id="66ce3-135">Text1</span></span>|<span data-ttu-id="66ce3-136">Text2</span><span class="sxs-lookup"><span data-stu-id="66ce3-136">Text2</span></span>|  
  
 <span data-ttu-id="66ce3-137">Examinons également le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="66ce3-137">Alternatively, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1" attr2="value2"/>  
</DocumentElement>  
```  
  
 <span data-ttu-id="66ce3-138">Le processus d’inférence produit un **DataSet** nommée « DocumentElement » contenant une table nommée « Element1 ».</span><span class="sxs-lookup"><span data-stu-id="66ce3-138">The inference process produces a **DataSet** named "DocumentElement" that contains a table named "Element1."</span></span>  
  
 <span data-ttu-id="66ce3-139">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="66ce3-139">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="66ce3-140">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="66ce3-140">**Table:** Element1</span></span>  
  
|<span data-ttu-id="66ce3-141">attr1</span><span class="sxs-lookup"><span data-stu-id="66ce3-141">attr1</span></span>|<span data-ttu-id="66ce3-142">attr2</span><span class="sxs-lookup"><span data-stu-id="66ce3-142">attr2</span></span>|  
|-----------|-----------|  
|<span data-ttu-id="66ce3-143">valeur1</span><span class="sxs-lookup"><span data-stu-id="66ce3-143">value1</span></span>|<span data-ttu-id="66ce3-144">valeur2</span><span class="sxs-lookup"><span data-stu-id="66ce3-144">value2</span></span>|  
  
## <a name="repeating-elements"></a><span data-ttu-id="66ce3-145">Éléments qui se répètent</span><span class="sxs-lookup"><span data-stu-id="66ce3-145">Repeating Elements</span></span>  
 <span data-ttu-id="66ce3-146">Les éléments qui se répètent donnent une seule table déduite.</span><span class="sxs-lookup"><span data-stu-id="66ce3-146">Elements that repeat result in a single inferred table.</span></span> <span data-ttu-id="66ce3-147">Examinons, par exemple, le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="66ce3-147">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>Text1</Element1>  
  <Element1>Text2</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="66ce3-148">Le processus d'inférence produit une table nommée « Element1 ».</span><span class="sxs-lookup"><span data-stu-id="66ce3-148">The inference process produces a table named "Element1."</span></span>  
  
 <span data-ttu-id="66ce3-149">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="66ce3-149">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="66ce3-150">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="66ce3-150">**Table:** Element1</span></span>  
  
|<span data-ttu-id="66ce3-151">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="66ce3-151">Element1_Text</span></span>|  
|--------------------|  
|<span data-ttu-id="66ce3-152">Text1</span><span class="sxs-lookup"><span data-stu-id="66ce3-152">Text1</span></span>|  
|<span data-ttu-id="66ce3-153">Text2</span><span class="sxs-lookup"><span data-stu-id="66ce3-153">Text2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="66ce3-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66ce3-154">See also</span></span>

- [<span data-ttu-id="66ce3-155">Inférence de la structure relationnelle d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="66ce3-155">Inferring DataSet Relational Structure from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="66ce3-156">Chargement d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="66ce3-156">Loading a DataSet from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [<span data-ttu-id="66ce3-157">Chargement des informations de schéma de DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="66ce3-157">Loading DataSet Schema Information from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="66ce3-158">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="66ce3-158">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [<span data-ttu-id="66ce3-159">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="66ce3-159">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="66ce3-160">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="66ce3-160">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
