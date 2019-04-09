---
title: Datasets typés
ms.date: 03/30/2017
ms.assetid: 033d2548-cf24-4c05-8179-67d8b009c048
ms.openlocfilehash: 92ed3f8fd392238785fd2d205668f14fe477f2b8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59098649"
---
# <a name="typed-datasets"></a><span data-ttu-id="0b231-102">Datasets typés</span><span class="sxs-lookup"><span data-stu-id="0b231-102">Typed DataSets</span></span>
<span data-ttu-id="0b231-103">En plus d'un accès par liaison tardive aux valeurs via des variables faiblement typées, l'objet <xref:System.Data.DataSet> permet un accès aux données par l'intermédiaire d'une métaphore fortement typée.</span><span class="sxs-lookup"><span data-stu-id="0b231-103">Along with late bound access to values through weakly typed variables, the <xref:System.Data.DataSet> provides access to data through a strongly typed metaphor.</span></span> <span data-ttu-id="0b231-104">Tables et colonnes qui font partie de la **DataSet** sont accessibles à l’aide des noms conviviaux et de variables fortement typées.</span><span class="sxs-lookup"><span data-stu-id="0b231-104">Tables and columns that are part of the **DataSet** can be accessed using user-friendly names and strongly typed variables.</span></span>  
  
 <span data-ttu-id="0b231-105">Typé **DataSet** est une classe qui dérive un **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="0b231-105">A typed **DataSet** is a class that derives from a **DataSet**.</span></span> <span data-ttu-id="0b231-106">Par conséquent, il hérite de toutes les méthodes, événements et propriétés d’un **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="0b231-106">As such, it inherits all the methods, events, and properties of a **DataSet**.</span></span> <span data-ttu-id="0b231-107">En outre, typé **DataSet** fournit des méthodes fortement typées, propriétés et événements.</span><span class="sxs-lookup"><span data-stu-id="0b231-107">Additionally, a typed **DataSet** provides strongly typed methods, events, and properties.</span></span> <span data-ttu-id="0b231-108">Cela signifie que vous pouvez accéder à des tables et à des colonnes par leur nom au lieu d'utiliser les méthodes associées à des collections.</span><span class="sxs-lookup"><span data-stu-id="0b231-108">This means you can access tables and columns by name, instead of using collection-based methods.</span></span> <span data-ttu-id="0b231-109">À part d’améliorer la lisibilité du code, typé **DataSet** autorise également le code de Visual Studio .NET éditeur complète automatiquement les lignes en cours de frappe.</span><span class="sxs-lookup"><span data-stu-id="0b231-109">Aside from the improved readability of the code, a typed **DataSet** also allows the Visual Studio .NET code editor to automatically complete lines as you type.</span></span>  
  
 <span data-ttu-id="0b231-110">En outre, fortement typée **DataSet** donne accès aux valeurs avec le type approprié au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="0b231-110">Additionally, the strongly typed **DataSet** provides access to values as the correct type at compile time.</span></span> <span data-ttu-id="0b231-111">Avec fortement typé **DataSet**, interception des erreurs d’incompatibilité de type lorsque le code est compilé et non au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0b231-111">With a strongly typed **DataSet**, type mismatch errors are caught when the code is compiled rather than at run time.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0b231-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="0b231-112">In This Section</span></span>  
 [<span data-ttu-id="0b231-113">Génération de datasets fortement typés</span><span class="sxs-lookup"><span data-stu-id="0b231-113">Generating Strongly Typed DataSets</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-strongly-typed-datasets.md)  
 <span data-ttu-id="0b231-114">Décrit comment créer et utiliser fortement typé **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="0b231-114">Describes how to create and use a strongly typed **DataSet**.</span></span>  
  
 [<span data-ttu-id="0b231-115">Annotation de DataSet typés</span><span class="sxs-lookup"><span data-stu-id="0b231-115">Annotating Typed DataSets</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/annotating-typed-datasets.md)  
 <span data-ttu-id="0b231-116">Explique comment annoter le schéma XML Schema definition language (XSD) permet de générer un fortement typée **DataSet**afin de donner aux **DataSet** noms conviviaux d’éléments sans modifier le schéma sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0b231-116">Describes how to annotate the XML Schema definition language (XSD) schema used to generate a strongly typed **DataSet**, to give **DataSet** elements friendly names without altering the underlying schema.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b231-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b231-117">See also</span></span>

- [<span data-ttu-id="0b231-118">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="0b231-118">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="0b231-119">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="0b231-119">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
