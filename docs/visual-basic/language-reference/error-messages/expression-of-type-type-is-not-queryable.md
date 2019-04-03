---
title: L'expression de type '<type>' ne peut pas être interrogée
ms.date: 07/20/2015
f1_keywords:
- bc36593
- vbc36593
helpviewer_keywords:
- BC36593
ms.assetid: 6f1f5860-bf97-4885-9ebb-bc87d028095c
ms.openlocfilehash: 7f74d56b47629ff76f9b935d26278ace8df4c353
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58842328"
---
# <a name="expression-of-type-type-is-not-queryable"></a><span data-ttu-id="c92e0-102">Expression de type \<type > ne peut pas être interrogée</span><span class="sxs-lookup"><span data-stu-id="c92e0-102">Expression of type \<type> is not queryable</span></span>
<span data-ttu-id="c92e0-103">Expression de type \<type > ne peut pas être interrogée.</span><span class="sxs-lookup"><span data-stu-id="c92e0-103">Expression of type \<type> is not queryable.</span></span> <span data-ttu-id="c92e0-104">Assurez-vous que vous ne manque une importation d’espace de noms de référence ou d’assembly pour le fournisseur LINQ.</span><span class="sxs-lookup"><span data-stu-id="c92e0-104">Make sure you are not missing an assembly reference and/or namespace import for the LINQ provider.</span></span>  
  
 <span data-ttu-id="c92e0-105">Types requêtables sont définies dans le <xref:System.Linq>, <xref:System.Data.Linq>, et <xref:System.Xml.Linq> espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="c92e0-105">Queryable types are defined in the <xref:System.Linq>, <xref:System.Data.Linq>, and <xref:System.Xml.Linq> namespaces.</span></span> <span data-ttu-id="c92e0-106">Vous devez importer un ou plusieurs de ces espaces de noms pour effectuer des requêtes LINQ.</span><span class="sxs-lookup"><span data-stu-id="c92e0-106">You must import one or more of these namespaces to perform LINQ queries.</span></span>  
  
 <span data-ttu-id="c92e0-107">Le <xref:System.Linq> espace de noms vous permet aux objets de requête tels que les collections et tableaux à l’aide de LINQ.</span><span class="sxs-lookup"><span data-stu-id="c92e0-107">The <xref:System.Linq> namespace enables you to query objects such as collections and arrays by using LINQ.</span></span>  
  
 <span data-ttu-id="c92e0-108">Le <xref:System.Data.Linq> espace de noms vous permet d’interroger des jeux de données ADO.NET et des bases de données SQL Server à l’aide de LINQ.</span><span class="sxs-lookup"><span data-stu-id="c92e0-108">The <xref:System.Data.Linq> namespace enables you to query ADO.NET Datasets and SQL Server databases by using LINQ.</span></span>  
  
 <span data-ttu-id="c92e0-109">Le <xref:System.Xml.Linq> espace de noms vous permet d’interroger XML à l’aide de LINQ et à utiliser les fonctionnalités XML dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c92e0-109">The <xref:System.Xml.Linq> namespace enables you to query XML by using LINQ and to use XML features in Visual Basic.</span></span>  
  
 <span data-ttu-id="c92e0-110">**ID d’erreur :** BC36593</span><span class="sxs-lookup"><span data-stu-id="c92e0-110">**Error ID:** BC36593</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c92e0-111">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c92e0-111">To correct this error</span></span>  
  
1.  <span data-ttu-id="c92e0-112">Ajouter un `Import` instruction pour la <xref:System.Linq>, <xref:System.Data.Linq>, ou <xref:System.Xml.Linq> espace de noms à votre fichier de code.</span><span class="sxs-lookup"><span data-stu-id="c92e0-112">Add an `Import` statement for the <xref:System.Linq>, <xref:System.Data.Linq>, or <xref:System.Xml.Linq> namespace to your code file.</span></span> <span data-ttu-id="c92e0-113">Vous pouvez également importer des espaces de noms pour votre projet à l’aide de la **références** page du Concepteur de projets (**mon projet**).</span><span class="sxs-lookup"><span data-stu-id="c92e0-113">You can also import namespaces for your project by using the **References** page of the Project Designer (**My Project**).</span></span>  
  
2.  <span data-ttu-id="c92e0-114">Vérifiez que le type que vous avez identifié comme source de votre requête est un type requêtable.</span><span class="sxs-lookup"><span data-stu-id="c92e0-114">Ensure that the type that you have identified as the source of your query is a queryable type.</span></span> <span data-ttu-id="c92e0-115">Autrement dit, un type qui implémente <xref:System.Collections.Generic.IEnumerable%601> ou <xref:System.Linq.IQueryable%601>.</span><span class="sxs-lookup"><span data-stu-id="c92e0-115">That is, a type that implements <xref:System.Collections.Generic.IEnumerable%601> or <xref:System.Linq.IQueryable%601>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c92e0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c92e0-116">See also</span></span>

- <xref:System.Linq>
- <xref:System.Data.Linq>
- <xref:System.Xml.Linq>
- [<span data-ttu-id="c92e0-117">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c92e0-117">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="c92e0-118">LINQ</span><span class="sxs-lookup"><span data-stu-id="c92e0-118">LINQ</span></span>](../../../visual-basic/programming-guide/language-features/linq/index.md)
- [<span data-ttu-id="c92e0-119">XML</span><span class="sxs-lookup"><span data-stu-id="c92e0-119">XML</span></span>](../../../visual-basic/programming-guide/language-features/xml/index.md)
- [<span data-ttu-id="c92e0-120">Références et l’instruction Imports</span><span class="sxs-lookup"><span data-stu-id="c92e0-120">References and the Imports Statement</span></span>](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [<span data-ttu-id="c92e0-121">Imports (instruction) (espace de noms et type .NET)</span><span class="sxs-lookup"><span data-stu-id="c92e0-121">Imports Statement (.NET Namespace and Type)</span></span>](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [<span data-ttu-id="c92e0-122">Page Références, Concepteur de projets (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c92e0-122">References Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/references-page-project-designer-visual-basic)
