---
title: 'Procédure : Personnaliser des classes d’entité à l’aide de l’éditeur de code'
ms.date: 03/30/2017
ms.assetid: ec28332f-9f3c-4e0a-baca-60f9141a68c0
ms.openlocfilehash: 05a523f8b98c7b64350b67c217baba07dca14de3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62037828"
---
# <a name="how-to-customize-entity-classes-by-using-the-code-editor"></a><span data-ttu-id="3c6ee-102">Procédure : Personnaliser des classes d’entité à l’aide de l’éditeur de code</span><span class="sxs-lookup"><span data-stu-id="3c6ee-102">How to: Customize Entity Classes by Using the Code Editor</span></span>
<span data-ttu-id="3c6ee-103">Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour créer ou personnaliser leurs classes d’entité.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-103">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to create or customize their entity classes.</span></span>  
  
 <span data-ttu-id="3c6ee-104">Vous pouvez également utiliser l’éditeur de code Visual Studio pour écrire votre propre code de mappage ou personnaliser du code qui a déjà été généré.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-104">You can also use the Visual Studio code editor to write your own mapping code or to customize code that has already been generated.</span></span> <span data-ttu-id="3c6ee-105">Pour plus d’informations, consultez [mappage basé sur l’attribut](../../../../../../docs/framework/data/adonet/sql/linq/attribute-based-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="3c6ee-105">For more information, see [Attribute-Based Mapping](../../../../../../docs/framework/data/adonet/sql/linq/attribute-based-mapping.md).</span></span>  
  
 <span data-ttu-id="3c6ee-106">Les rubriques de cette section décrivent comment personnaliser votre modèle objet.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-106">The topics in this section describe how to customize your object model.</span></span>  
  
 [<span data-ttu-id="3c6ee-107">Guide pratique pour Spécifiez les noms de base de données</span><span class="sxs-lookup"><span data-stu-id="3c6ee-107">How to: Specify Database Names</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-database-names.md)  
 <span data-ttu-id="3c6ee-108">Explique comment utiliser <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-108">Describes how to use <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-109">Guide pratique pour Représentent les Tables en tant que Classes</span><span class="sxs-lookup"><span data-stu-id="3c6ee-109">How to: Represent Tables as Classes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-tables-as-classes.md)  
 <span data-ttu-id="3c6ee-110">Explique comment utiliser <xref:System.Data.Linq.Mapping.TableAttribute>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-110">Describes how to use <xref:System.Data.Linq.Mapping.TableAttribute>.</span></span>  
  
 [<span data-ttu-id="3c6ee-111">Guide pratique pour Représenter des colonnes en tant que membres de classe</span><span class="sxs-lookup"><span data-stu-id="3c6ee-111">How to: Represent Columns as Class Members</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-columns-as-class-members.md)  
 <span data-ttu-id="3c6ee-112">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-112">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span></span>  
  
 [<span data-ttu-id="3c6ee-113">Guide pratique pour Représenter les clés primaires</span><span class="sxs-lookup"><span data-stu-id="3c6ee-113">How to: Represent Primary Keys</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-primary-keys.md)  
 <span data-ttu-id="3c6ee-114">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-114">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-115">Guide pratique pour Mapper des relations de base de données</span><span class="sxs-lookup"><span data-stu-id="3c6ee-115">How to: Map Database Relationships</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-map-database-relationships.md)  
 <span data-ttu-id="3c6ee-116">Fournit des exemples d'utilisation de l'attribut <xref:System.Data.Linq.Mapping.AssociationAttribute>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-116">Provides examples of using the <xref:System.Data.Linq.Mapping.AssociationAttribute> attribute.</span></span>  
  
 [<span data-ttu-id="3c6ee-117">Guide pratique pour Représenter des colonnes en tant que base de données générée</span><span class="sxs-lookup"><span data-stu-id="3c6ee-117">How to: Represent Columns as Database-Generated</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-columns-as-database-generated.md)  
 <span data-ttu-id="3c6ee-118">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-118">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-119">Guide pratique pour Représentent les colonnes en tant que Timestamp ou Version</span><span class="sxs-lookup"><span data-stu-id="3c6ee-119">How to: Represent Columns as Timestamp or Version Columns</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-columns-as-timestamp-or-version-columns.md)  
 <span data-ttu-id="3c6ee-120">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-120">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-121">Guide pratique pour Spécifier les Types de données de base de données</span><span class="sxs-lookup"><span data-stu-id="3c6ee-121">How to: Specify Database Data Types</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-database-data-types.md)  
 <span data-ttu-id="3c6ee-122">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-122">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-123">Guide pratique pour Représenter des colonnes calculées</span><span class="sxs-lookup"><span data-stu-id="3c6ee-123">How to: Represent Computed Columns</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-computed-columns.md)  
 <span data-ttu-id="3c6ee-124">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-124">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-125">Guide pratique pour Spécifier des champs de stockage privés</span><span class="sxs-lookup"><span data-stu-id="3c6ee-125">How to: Specify Private Storage Fields</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-private-storage-fields.md)  
 <span data-ttu-id="3c6ee-126">Explique comment utiliser <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-126">Describes how to use <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-127">Guide pratique pour Représenter des colonnes comme autorisant les valeurs Null</span><span class="sxs-lookup"><span data-stu-id="3c6ee-127">How to: Represent Columns as Allowing Null Values</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-represent-columns-as-allowing-null-values.md)  
 <span data-ttu-id="3c6ee-128">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-128">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>.</span></span>  
  
 [<span data-ttu-id="3c6ee-129">Guide pratique pour Mapper des hiérarchies d’héritage</span><span class="sxs-lookup"><span data-stu-id="3c6ee-129">How to: Map Inheritance Hierarchies</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-map-inheritance-hierarchies.md)  
 <span data-ttu-id="3c6ee-130">Décrit les mappages requis pour spécifier une hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-130">Describes the mappings required to specify an inheritance hierarchy.</span></span>  
  
 [<span data-ttu-id="3c6ee-131">Guide pratique pour Spécifier la vérification de conflits d’accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="3c6ee-131">How to: Specify Concurrency-Conflict Checking</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-concurrency-conflict-checking.md)  
 <span data-ttu-id="3c6ee-132">Explique comment utiliser <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span><span class="sxs-lookup"><span data-stu-id="3c6ee-132">Describes how to use <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c6ee-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c6ee-133">See also</span></span>

- [<span data-ttu-id="3c6ee-134">SqlMetal.exe (outil de génération de code)</span><span class="sxs-lookup"><span data-stu-id="3c6ee-134">SqlMetal.exe (Code Generation Tool)</span></span>](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md)
