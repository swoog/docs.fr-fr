---
title: Déduction des relations
ms.date: 03/30/2017
ms.assetid: 8fa86a9d-6545-4a9d-b1f5-58d9742179c7
ms.openlocfilehash: 7dc3fb0c6098d636e640aaf52b72a404c1486492
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46492994"
---
# <a name="inferring-relationships"></a><span data-ttu-id="77a0c-102">Déduction des relations</span><span class="sxs-lookup"><span data-stu-id="77a0c-102">Inferring Relationships</span></span>
<span data-ttu-id="77a0c-103">Si un élément déduit en tant que table comporte un élément enfant également déduit en tant que table, un objet <xref:System.Data.DataRelation> sera créé entre les deux tables.</span><span class="sxs-lookup"><span data-stu-id="77a0c-103">If an element that is inferred as a table has a child element that is also inferred as a table, a <xref:System.Data.DataRelation> will be created between the two tables.</span></span> <span data-ttu-id="77a0c-104">Une nouvelle colonne avec un nom de **ParentTableName_Id** sera ajouté à la table créée par l’élément parent et à la table créée pour l’élément enfant.</span><span class="sxs-lookup"><span data-stu-id="77a0c-104">A new column with a name of **ParentTableName_Id** will be added to both the table created for the parent element, and the table created for the child element.</span></span> <span data-ttu-id="77a0c-105">Le **ColumnMapping** propriété de cette colonne d’identité est définie **MappingType.Hidden**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-105">The **ColumnMapping** property of this identity column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="77a0c-106">La colonne sera une clé primaire auto-incrémentée pour la table parente et sera utilisée pour le **DataRelation** entre les deux tables.</span><span class="sxs-lookup"><span data-stu-id="77a0c-106">The column will be an auto-incrementing primary key for the parent table, and will be used for the **DataRelation** between the two tables.</span></span> <span data-ttu-id="77a0c-107">Le type de données de la colonne d’identité ajoutée sera **System.Int32**, contrairement au type de données de toutes les autres colonnes déduites, qui est **System.String**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-107">The data type of the added identity column will be **System.Int32**, unlike the data type of all other inferred columns, which is **System.String**.</span></span> <span data-ttu-id="77a0c-108">Un <xref:System.Data.ForeignKeyConstraint> avec **DeleteRule** = **Cascade** sera également créé à l’aide de la nouvelle colonne dans les tables parent et enfant.</span><span class="sxs-lookup"><span data-stu-id="77a0c-108">A <xref:System.Data.ForeignKeyConstraint> with **DeleteRule** = **Cascade** will also be created using the new column in both the parent and child tables.</span></span>  
  
 <span data-ttu-id="77a0c-109">Examinons, par exemple, le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="77a0c-109">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1 attr1="value1" attr2="value2"/>  
    <ChildElement2>Text2</ChildElement2>  
  </Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="77a0c-110">Le processus d’inférence produira deux tables : **Element1** et **ChildElement1**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-110">The inference process will produce two tables: **Element1** and **ChildElement1**.</span></span>  
  
 <span data-ttu-id="77a0c-111">Le **Element1** table aura deux colonnes : **Element1_Id** et **ChildElement2**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-111">The **Element1** table will have two columns: **Element1_Id** and **ChildElement2**.</span></span> <span data-ttu-id="77a0c-112">Le **ColumnMapping** propriété de la **Element1_Id** jeu de colonnes **MappingType.Hidden**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-112">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="77a0c-113">Le **ColumnMapping** propriété de la **ChildElement2** jeu de colonnes **MappingType.Element**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-113">The **ColumnMapping** property of the **ChildElement2** column will be set to **MappingType.Element**.</span></span> <span data-ttu-id="77a0c-114">Le **Element1_Id** colonne sera définie en tant que la clé primaire de la **Element1** table.</span><span class="sxs-lookup"><span data-stu-id="77a0c-114">The **Element1_Id** column will be set as the primary key of the **Element1** table.</span></span>  
  
 <span data-ttu-id="77a0c-115">Le **ChildElement1** table aura trois colonnes : **attr1**, **attr2** et **Element1_Id**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-115">The **ChildElement1** table will have three columns: **attr1**, **attr2** and **Element1_Id**.</span></span> <span data-ttu-id="77a0c-116">Le **ColumnMapping** propriété pour le **attr1** et **attr2** colonnes seront définies sur **MappingType.Attribute**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-116">The **ColumnMapping** property for the **attr1** and **attr2** columns will be set to **MappingType.Attribute**.</span></span> <span data-ttu-id="77a0c-117">Le **ColumnMapping** propriété de la **Element1_Id** jeu de colonnes **MappingType.Hidden**.</span><span class="sxs-lookup"><span data-stu-id="77a0c-117">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span>  
  
 <span data-ttu-id="77a0c-118">Un **DataRelation** et **ForeignKeyConstraint** sera créé à l’aide de la **Element1_Id** colonnes des deux tables.</span><span class="sxs-lookup"><span data-stu-id="77a0c-118">A **DataRelation** and **ForeignKeyConstraint** will be created using the **Element1_Id** columns from both tables.</span></span>  
  
 <span data-ttu-id="77a0c-119">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="77a0c-119">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="77a0c-120">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="77a0c-120">**Table:** Element1</span></span>  
  
|<span data-ttu-id="77a0c-121">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="77a0c-121">Element1_Id</span></span>|<span data-ttu-id="77a0c-122">ChildElement2</span><span class="sxs-lookup"><span data-stu-id="77a0c-122">ChildElement2</span></span>|  
|------------------|-------------------|  
|<span data-ttu-id="77a0c-123">0</span><span class="sxs-lookup"><span data-stu-id="77a0c-123">0</span></span>|<span data-ttu-id="77a0c-124">Text2</span><span class="sxs-lookup"><span data-stu-id="77a0c-124">Text2</span></span>|  
  
 <span data-ttu-id="77a0c-125">**Table :** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="77a0c-125">**Table:** ChildElement1</span></span>  
  
|<span data-ttu-id="77a0c-126">attr1</span><span class="sxs-lookup"><span data-stu-id="77a0c-126">attr1</span></span>|<span data-ttu-id="77a0c-127">attr2</span><span class="sxs-lookup"><span data-stu-id="77a0c-127">attr2</span></span>|<span data-ttu-id="77a0c-128">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="77a0c-128">Element1_Id</span></span>|  
|-----------|-----------|------------------|  
|<span data-ttu-id="77a0c-129">value1</span><span class="sxs-lookup"><span data-stu-id="77a0c-129">value1</span></span>|<span data-ttu-id="77a0c-130">value2</span><span class="sxs-lookup"><span data-stu-id="77a0c-130">value2</span></span>|<span data-ttu-id="77a0c-131">0</span><span class="sxs-lookup"><span data-stu-id="77a0c-131">0</span></span>|  
  
 <span data-ttu-id="77a0c-132">**DataRelation :** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="77a0c-132">**DataRelation:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="77a0c-133">**ParentTable :** Element1</span><span class="sxs-lookup"><span data-stu-id="77a0c-133">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="77a0c-134">**ParentColumn :** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="77a0c-134">**ParentColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="77a0c-135">**ChildTable :** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="77a0c-135">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="77a0c-136">**ChildColumn :** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="77a0c-136">**ChildColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="77a0c-137">**Imbriqué :** True</span><span class="sxs-lookup"><span data-stu-id="77a0c-137">**Nested:** True</span></span>  
  
 <span data-ttu-id="77a0c-138">**ForeignKeyConstraint :** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="77a0c-138">**ForeignKeyConstraint:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="77a0c-139">**Colonne :** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="77a0c-139">**Column:** Element1_Id</span></span>  
  
 <span data-ttu-id="77a0c-140">**ParentTable :** Element1</span><span class="sxs-lookup"><span data-stu-id="77a0c-140">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="77a0c-141">**ChildTable :** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="77a0c-141">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="77a0c-142">**DeleteRule :** en Cascade</span><span class="sxs-lookup"><span data-stu-id="77a0c-142">**DeleteRule:** Cascade</span></span>  
  
 <span data-ttu-id="77a0c-143">**AcceptRejectRule :** None</span><span class="sxs-lookup"><span data-stu-id="77a0c-143">**AcceptRejectRule:** None</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77a0c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77a0c-144">See Also</span></span>  
 [<span data-ttu-id="77a0c-145">Inférence de la structure relationnelle d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="77a0c-145">Inferring DataSet Relational Structure from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)  
 [<span data-ttu-id="77a0c-146">Chargement d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="77a0c-146">Loading a DataSet from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)  
 [<span data-ttu-id="77a0c-147">Chargement des informations de schéma de DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="77a0c-147">Loading DataSet Schema Information from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)  
 [<span data-ttu-id="77a0c-148">Imbrication de DataRelations</span><span class="sxs-lookup"><span data-stu-id="77a0c-148">Nesting DataRelations</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md)  
 [<span data-ttu-id="77a0c-149">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="77a0c-149">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)  
 [<span data-ttu-id="77a0c-150">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="77a0c-150">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 [<span data-ttu-id="77a0c-151">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="77a0c-151">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
