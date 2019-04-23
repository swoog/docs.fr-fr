---
title: DataSets, DataTables et DataViews
ms.date: 03/30/2017
ms.assetid: 6d4c4b69-8919-4224-8a65-6cca1c61b48f
ms.openlocfilehash: 9c57f75dd94f3fbda74c13a5d5773825051fe416
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59105727"
---
# <a name="datasets-datatables-and-dataviews"></a><span data-ttu-id="51a7b-102">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="51a7b-102">DataSets, DataTables, and DataViews</span></span>
<span data-ttu-id="51a7b-103">L'objet <xref:System.Data.DataSet> ADO.NET est une représentation de données résidente en mémoire qui propose un modèle de programmation relationnel cohérent, quelle que soit la source des données qu'il contient.</span><span class="sxs-lookup"><span data-stu-id="51a7b-103">The ADO.NET <xref:System.Data.DataSet> is a memory-resident representation of data that provides a consistent relational programming model regardless of the source of the data it contains.</span></span> <span data-ttu-id="51a7b-104">Un objet <xref:System.Data.DataSet> représente un jeu de données complet, y compris les tables qui contiennent et organisent les données et y appliquent des contraintes, ainsi que les relations entre les tables.</span><span class="sxs-lookup"><span data-stu-id="51a7b-104">A <xref:System.Data.DataSet> represents a complete set of data including the tables that contain, order, and constrain the data, as well as the relationships between the tables.</span></span>  
  
 <span data-ttu-id="51a7b-105">L'utilisation d'un objet <xref:System.Data.DataSet> peut se faire via différentes méthodes qui peuvent être appliquées indépendamment les unes des autres ou combinées.</span><span class="sxs-lookup"><span data-stu-id="51a7b-105">There are several ways of working with a <xref:System.Data.DataSet>, which can be applied independently or in combination.</span></span> <span data-ttu-id="51a7b-106">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="51a7b-106">You can:</span></span>  
  
-   <span data-ttu-id="51a7b-107">Créer par programmation un objet <xref:System.Data.DataTable>, <xref:System.Data.DataRelation> et <xref:System.Data.Constraint> dans un objet <xref:System.Data.DataSet>, puis remplir les tables de données.</span><span class="sxs-lookup"><span data-stu-id="51a7b-107">Programmatically create a <xref:System.Data.DataTable>, <xref:System.Data.DataRelation>, and <xref:System.Data.Constraint> within a <xref:System.Data.DataSet> and populate the tables with data.</span></span>  
  
-   <span data-ttu-id="51a7b-108">Remplir l'objet <xref:System.Data.DataSet> de tables de données provenant d'une source de données relationnelles existante à l'aide d'un objet `DataAdapter`.</span><span class="sxs-lookup"><span data-stu-id="51a7b-108">Populate the <xref:System.Data.DataSet> with tables of data from an existing relational data source using a `DataAdapter`.</span></span>  
  
-   <span data-ttu-id="51a7b-109">Charger et rendre persistent le contenu de l'objet <xref:System.Data.DataSet> à l'aide de XML.</span><span class="sxs-lookup"><span data-stu-id="51a7b-109">Load and persist the <xref:System.Data.DataSet> contents using XML.</span></span> <span data-ttu-id="51a7b-110">Pour plus d’informations, consultez [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md).</span><span class="sxs-lookup"><span data-stu-id="51a7b-110">For more information, see [Using XML in a DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md).</span></span>  
  
 <span data-ttu-id="51a7b-111">Un objet <xref:System.Data.DataSet> fortement typé peut aussi être transporté au moyen d’un service web XML.</span><span class="sxs-lookup"><span data-stu-id="51a7b-111">A strongly typed <xref:System.Data.DataSet> can also be transported using an XML Web service.</span></span> <span data-ttu-id="51a7b-112">Le design de l’objet <xref:System.Data.DataSet> le rend idéal pour le transport de données à l’aide des services web XML.</span><span class="sxs-lookup"><span data-stu-id="51a7b-112">The design of the <xref:System.Data.DataSet> makes it ideal for transporting data using XML Web services.</span></span> <span data-ttu-id="51a7b-113">Pour une vue d’ensemble des services web XML, consultez [Vue d’ensemble des services web XML](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/w9fdtx28(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="51a7b-113">For an overview of XML Web services, see [XML Web Services Overview](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/w9fdtx28(v=vs.100)).</span></span> <span data-ttu-id="51a7b-114">Pour obtenir un exemple d’utilisation d’un <xref:System.Data.DataSet> à partir d’un service web XML, consultez [Consommation d’un DataSet à partir d’un service web XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/consuming-a-dataset-from-an-xml-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="51a7b-114">For an example of consuming a <xref:System.Data.DataSet> from an XML Web service, see [Consuming a DataSet from an XML Web Service](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/consuming-a-dataset-from-an-xml-web-service.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="51a7b-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="51a7b-115">In This Section</span></span>  
 [<span data-ttu-id="51a7b-116">Création d’un DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-116">Creating a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/creating-a-dataset.md)  
 <span data-ttu-id="51a7b-117">Décrit la syntaxe permettant de créer une instance d'un objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="51a7b-117">Describes the syntax for creating an instance of a <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="51a7b-118">Ajout d’un DataTable à un DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-118">Adding a DataTable to a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/adding-a-datatable-to-a-dataset.md)  
 <span data-ttu-id="51a7b-119">Explique comment créer et ajouter des tables et des colonnes à un objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="51a7b-119">Describes how to create and add tables and columns to a <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="51a7b-120">Ajout de DataRelations</span><span class="sxs-lookup"><span data-stu-id="51a7b-120">Adding DataRelations</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/adding-datarelations.md)  
 <span data-ttu-id="51a7b-121">Explique comment créer des relations entre différentes tables d'un objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="51a7b-121">Describes how to create relations between tables in a <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="51a7b-122">Parcours des DataRelations</span><span class="sxs-lookup"><span data-stu-id="51a7b-122">Navigating DataRelations</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/navigating-datarelations.md)  
 <span data-ttu-id="51a7b-123">Explique comment utiliser les relations entre différentes tables d'un objet <xref:System.Data.DataSet> afin de retourner les lignes enfants ou parentes d'une relation parent-enfant.</span><span class="sxs-lookup"><span data-stu-id="51a7b-123">Describes how to use the relations between tables in a <xref:System.Data.DataSet> to return the child or parent rows of a parent-child relationship.</span></span>  
  
 [<span data-ttu-id="51a7b-124">Fusion de contenu de DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-124">Merging DataSet Contents</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/merging-dataset-contents.md)  
 <span data-ttu-id="51a7b-125">Décrit comment fusionner le contenu d’un tableau <xref:System.Data.DataSet>, <xref:System.Data.DataTable> ou <xref:System.Data.DataRow> dans un autre objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="51a7b-125">Describes how to merge the contents of one <xref:System.Data.DataSet>, <xref:System.Data.DataTable>, or <xref:System.Data.DataRow> array into another <xref:System.Data.DataSet>.</span></span>  
  
 [<span data-ttu-id="51a7b-126">Copie de contenu de DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-126">Copying DataSet Contents</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/copying-dataset-contents.md)  
 <span data-ttu-id="51a7b-127">Explique comment créer une copie d'un objet <xref:System.Data.DataSet> susceptible de contenir un schéma et des données spécifiées.</span><span class="sxs-lookup"><span data-stu-id="51a7b-127">Describes how to create a copy of a <xref:System.Data.DataSet> that can contain schema as well as specified data.</span></span>  
  
 [<span data-ttu-id="51a7b-128">Gestion des événements de DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-128">Handling DataSet Events</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/handling-dataset-events.md)  
 <span data-ttu-id="51a7b-129">Décrit les événements d'un objet <xref:System.Data.DataSet> et comment les utiliser.</span><span class="sxs-lookup"><span data-stu-id="51a7b-129">Describes the events of a <xref:System.Data.DataSet> and how to use them.</span></span>  
  
 [<span data-ttu-id="51a7b-130">Datasets typés</span><span class="sxs-lookup"><span data-stu-id="51a7b-130">Typed DataSets</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md)  
 <span data-ttu-id="51a7b-131">Explique ce qu'est un objet <xref:System.Data.DataSet> typé et comment en créer un et l'utiliser.</span><span class="sxs-lookup"><span data-stu-id="51a7b-131">Discusses what a typed <xref:System.Data.DataSet> is and how to create and use it.</span></span>  
  
 [<span data-ttu-id="51a7b-132">DataTables</span><span class="sxs-lookup"><span data-stu-id="51a7b-132">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)  
 <span data-ttu-id="51a7b-133">Explique comment créer un objet <xref:System.Data.DataTable>, définir le schéma et manipuler les données.</span><span class="sxs-lookup"><span data-stu-id="51a7b-133">Describes how to create a <xref:System.Data.DataTable>, define the schema, and manipulate data.</span></span>  
  
 [<span data-ttu-id="51a7b-134">DataTableReaders</span><span class="sxs-lookup"><span data-stu-id="51a7b-134">DataTableReaders</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatablereaders.md)  
 <span data-ttu-id="51a7b-135">Explique comment créer et utiliser un <xref:System.Data.DataTableReader>.</span><span class="sxs-lookup"><span data-stu-id="51a7b-135">Describes how to create and use a <xref:System.Data.DataTableReader>.</span></span>  
  
 [<span data-ttu-id="51a7b-136">DataViews</span><span class="sxs-lookup"><span data-stu-id="51a7b-136">DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/dataviews.md)  
 <span data-ttu-id="51a7b-137">Décrit la façon de créer et d'utiliser des `DataViews` et d'utiliser des événements <xref:System.Data.DataView>.</span><span class="sxs-lookup"><span data-stu-id="51a7b-137">Describes how to create and work with `DataViews` and work with <xref:System.Data.DataView> events.</span></span>  
  
 [<span data-ttu-id="51a7b-138">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-138">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)  
 <span data-ttu-id="51a7b-139">Explique comment l'objet <xref:System.Data.DataSet> interagit avec XML en tant que source de données, notamment en ce qui concerne le chargement et la persistance du contenu d'un objet <xref:System.Data.DataSet> en tant que données XML.</span><span class="sxs-lookup"><span data-stu-id="51a7b-139">Describes how the <xref:System.Data.DataSet> interacts with XML as a data source, including loading and persisting the contents of a <xref:System.Data.DataSet> as XML data.</span></span>  
  
 [<span data-ttu-id="51a7b-140">Consommation d’un DataSet à partir d’un service web XML</span><span class="sxs-lookup"><span data-stu-id="51a7b-140">Consuming a DataSet from an XML Web Service</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/consuming-a-dataset-from-an-xml-web-service.md)  
 <span data-ttu-id="51a7b-141">Explique comment créer un service web XML qui utilise un <xref:System.Data.DataSet> pour le transport des données.</span><span class="sxs-lookup"><span data-stu-id="51a7b-141">Describes how to create an XML Web service that uses a <xref:System.Data.DataSet> to transport data.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="51a7b-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51a7b-142">Related Sections</span></span>  
 [<span data-ttu-id="51a7b-143">Nouveautés d’ADO.NET</span><span class="sxs-lookup"><span data-stu-id="51a7b-143">What's New in ADO.NET</span></span>](../../../../../docs/framework/data/adonet/whats-new.md)  
 <span data-ttu-id="51a7b-144">Introduit des fonctionnalités nouvelles dans ADO.NET.</span><span class="sxs-lookup"><span data-stu-id="51a7b-144">Introduces features that are new in ADO.NET.</span></span>  
  
 [<span data-ttu-id="51a7b-145">Vue d’ensemble d’ADO.NET</span><span class="sxs-lookup"><span data-stu-id="51a7b-145">ADO.NET Overview</span></span>](../../../../../docs/framework/data/adonet/ado-net-overview.md)  
 <span data-ttu-id="51a7b-146">Propose une introduction à la conception et aux composants de la technologie ADO.NET.</span><span class="sxs-lookup"><span data-stu-id="51a7b-146">Provides an introduction to the design and components of ADO.NET.</span></span>  
  
 [<span data-ttu-id="51a7b-147">Remplissage d’un DataSet à partir d’un DataAdapter</span><span class="sxs-lookup"><span data-stu-id="51a7b-147">Populating a DataSet from a DataAdapter</span></span>](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md)  
 <span data-ttu-id="51a7b-148">Explique comment charger un **DataSet** avec des données provenant d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="51a7b-148">Describes how to load a **DataSet** with data from a data source.</span></span>  
  
 [<span data-ttu-id="51a7b-149">Mise à jour de sources de données avec des DataAdapters</span><span class="sxs-lookup"><span data-stu-id="51a7b-149">Updating Data Sources with DataAdapters</span></span>](../../../../../docs/framework/data/adonet/updating-data-sources-with-dataadapters.md)  
 <span data-ttu-id="51a7b-150">Explique comment répercuter à la source de données les modifications apportées aux données d’un **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="51a7b-150">Describes how to resolve changes to the data in a **DataSet** back to the data source.</span></span>  
  
 [<span data-ttu-id="51a7b-151">Ajout de contraintes existantes à un DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-151">Adding Existing Constraints to a DataSet</span></span>](../../../../../docs/framework/data/adonet/adding-existing-constraints-to-a-dataset.md)  
 <span data-ttu-id="51a7b-152">Explique comment remplir un **DataSet** avec les informations de clé primaire d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="51a7b-152">Describes how to populate a **DataSet** with primary key information from a data source.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51a7b-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51a7b-153">See also</span></span>

- [<span data-ttu-id="51a7b-154">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="51a7b-154">ADO.NET</span></span>](../../../../../docs/framework/data/adonet/index.md)
- [<span data-ttu-id="51a7b-155">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="51a7b-155">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
