---
title: 'Comment : générer le modèle objet en Visual Basic ou C#'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: a0c73b33-5650-420c-b9dc-f49310c201ee
caps.latest.revision: 3
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: 77d7020a985abb8ed56af4fdd9f50a98bfc478c4
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-generate-the-object-model-in-visual-basic-or-c"></a><span data-ttu-id="23789-102">Comment : générer le modèle objet en Visual Basic ou C#</span><span class="sxs-lookup"><span data-stu-id="23789-102">How to: Generate the Object Model in Visual Basic or C#</span></span> #
<span data-ttu-id="23789-103">Dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], un modèle objet dans votre propre langage de programmation est mappé à une base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="23789-103">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], an object model in your own programming language is mapped to a relational database.</span></span> <span data-ttu-id="23789-104">Deux outils sont disponibles pour générer automatiquement un modèle Visual Basic ou c# à partir des métadonnées de base de données existante.</span><span class="sxs-lookup"><span data-stu-id="23789-104">Two tools are available for automatically generating a Visual Basic or C# model from the metadata of an existing database.</span></span>  
  
-   <span data-ttu-id="23789-105">Si vous utilisez Visual Studio, vous pouvez utiliser la [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour générer un modèle d’objet.</span><span class="sxs-lookup"><span data-stu-id="23789-105">If you are using Visual Studio, you can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to generate an object model.</span></span> <span data-ttu-id="23789-106">Le [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)] fournit une interface utilisateur élaborée pour vous aider à générer un [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] modèle objet.</span><span class="sxs-lookup"><span data-stu-id="23789-106">The [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)] provides a rich user interface to help you generate a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] object model.</span></span> <span data-ttu-id="23789-107">Pour plus d’informations, consultez [Linq to SQL Tools dans Visual Studio](https://docs.microsoft.com/en-us/visualstudio/data-tools/linq-to-sql-tools-in-visual-studio2).</span><span class="sxs-lookup"><span data-stu-id="23789-107">For more information see, [Linq to SQL Tools in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/data-tools/linq-to-sql-tools-in-visual-studio2).</span></span>
  
-   <span data-ttu-id="23789-108">Outil en ligne de commande SQLMetal</span><span class="sxs-lookup"><span data-stu-id="23789-108">The SQLMetal command-line tool.</span></span> <span data-ttu-id="23789-109">Pour plus d’informations, consultez [SqlMetal.exe (outil de génération de code)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="23789-109">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="23789-110">Si vous ne possédez pas de base de données existante et que vous souhaitez en créer une à partir d'un modèle objet, vous pouvez utiliser votre éditeur de code et <xref:System.Data.Linq.DataContext.CreateDatabase%2A>.</span><span class="sxs-lookup"><span data-stu-id="23789-110">If you do not have an existing database and want to create one from an object model, you can create your object model by using your code editor and <xref:System.Data.Linq.DataContext.CreateDatabase%2A>.</span></span> <span data-ttu-id="23789-111">Pour plus d’informations, consultez [Comment : créer dynamiquement une base de données](../../../../../../docs/framework/data/adonet/sql/linq/how-to-dynamically-create-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="23789-111">For more information, see [How to: Dynamically Create a Database](../../../../../../docs/framework/data/adonet/sql/linq/how-to-dynamically-create-a-database.md).</span></span>  
  
 <span data-ttu-id="23789-112">Documentation pour le [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)] fournit des exemples montrant comment générer un modèle d’objet Visual Basic ou c# à l’aide de la [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="23789-112">Documentation for the [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)] provides examples of how to generate a Visual Basic or C# object model by using the [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)].</span></span> <span data-ttu-id="23789-113">Les informations suivantes fournissent des exemples d'utilisation de l'outil en ligne de commande SQLMetal.</span><span class="sxs-lookup"><span data-stu-id="23789-113">The following information provide examples of how to use the SQLMetal command-line tool.</span></span> <span data-ttu-id="23789-114">Pour plus d’informations, consultez [SqlMetal.exe (outil de génération de code)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="23789-114">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="23789-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="23789-115">Example</span></span>  
 <span data-ttu-id="23789-116">La ligne de commande SQLMetal indiquée dans l’exemple suivant génère le code Visual Basic en tant que le modèle objet basé sur un attribut de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="23789-116">The SQLMetal command line shown in the following example produces Visual Basic code as the attribute-based object model of the Northwind sample database.</span></span> <span data-ttu-id="23789-117">Des procédures stockées et des fonctions sont également restituées.</span><span class="sxs-lookup"><span data-stu-id="23789-117">Stored procedures and functions are also rendered.</span></span>  
  
```  
sqlmetal /code:northwind.vb /language:vb "c:\northwnd.mdf" /sprocs /functions  
```  
  
## <a name="example"></a><span data-ttu-id="23789-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="23789-118">Example</span></span>  
 <span data-ttu-id="23789-119">La ligne de commande SQLMetal présentée dans l'exemple suivant produit du code C# comme modèle objet basé sur les attributs de l'exemple de base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="23789-119">The SQLMetal command line shown in the following example produces C# code as the attribute-based object model of the Northwind sample database.</span></span> <span data-ttu-id="23789-120">Des procédures stockées et des fonctions sont également restituées, et les noms de table sont automatiquement pluralisés.</span><span class="sxs-lookup"><span data-stu-id="23789-120">Stored procedures and functions are also rendered, and table names are automatically pluralized.</span></span>  
  
```  
sqlmetal /code:northwind.cs /language:csharp "c:\northwnd.mdf" /sprocs /functions /pluralize  
```  
  
## <a name="see-also"></a><span data-ttu-id="23789-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23789-121">See Also</span></span>  
 [<span data-ttu-id="23789-122">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="23789-122">Programming Guide</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/programming-guide.md)  
 [<span data-ttu-id="23789-123">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="23789-123">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [<span data-ttu-id="23789-124">Apprentissage par les procédures pas à pas</span><span class="sxs-lookup"><span data-stu-id="23789-124">Learning by Walkthroughs</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/learning-by-walkthroughs.md)  
 [<span data-ttu-id="23789-125">Guide pratique pour personnaliser des classes d’entité à l’aide de l’éditeur de code</span><span class="sxs-lookup"><span data-stu-id="23789-125">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)  
 [<span data-ttu-id="23789-126">Mappage basé sur les attributs</span><span class="sxs-lookup"><span data-stu-id="23789-126">Attribute-Based Mapping</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/attribute-based-mapping.md)  
 [<span data-ttu-id="23789-127">SqlMetal.exe (outil de génération de code)</span><span class="sxs-lookup"><span data-stu-id="23789-127">SqlMetal.exe (Code Generation Tool)</span></span>](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md)  
 [<span data-ttu-id="23789-128">Mappage externe</span><span class="sxs-lookup"><span data-stu-id="23789-128">External Mapping</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/external-mapping.md)  
 [<span data-ttu-id="23789-129">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="23789-129">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)  
 [<span data-ttu-id="23789-130">Création du modèle objet</span><span class="sxs-lookup"><span data-stu-id="23789-130">Creating the Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/creating-the-object-model.md)
