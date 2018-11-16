---
title: Créer un projet LINQ to DataSet dans Visual Studio
ms.date: 08/15/2018
ms.assetid: 49ba6cb0-cdd2-4571-aeaa-25bf0f40e9b3
ms.openlocfilehash: 22763d3b9581d09d7bdda0c09480f8d36bb8e2ec
ms.sourcegitcommit: 4bca8f7e172fd019ef437a4803bf5895c6bc4781
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "50980727"
---
# <a name="how-to-create-a-linq-to-dataset-project-in-visual-studio"></a><span data-ttu-id="241b1-102">Comment : créer un projet LINQ to DataSet dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="241b1-102">How to: Create a LINQ to DataSet project In Visual Studio</span></span>

<span data-ttu-id="241b1-103">Les différents types de projets LINQ nécessitent certains espaces de noms importés (Visual Basic) et les références d’assembly ou [à l’aide de](../../../csharp/language-reference/keywords/using-directive.md) directives (c#).</span><span class="sxs-lookup"><span data-stu-id="241b1-103">The different types of LINQ projects require certain assembly references and imported namespaces (Visual Basic) or [using](../../../csharp/language-reference/keywords/using-directive.md) directives (C#).</span></span> <span data-ttu-id="241b1-104">La configuration minimale requise pour LINQ est une référence à *System.Core.dll* et un `using` directive pour <xref:System.Linq>.</span><span class="sxs-lookup"><span data-stu-id="241b1-104">The minimum requirement for LINQ is a reference to *System.Core.dll* and a `using` directive for <xref:System.Linq>.</span></span>

<span data-ttu-id="241b1-105">Ces exigences sont fournis par défaut si vous créez un projet d’application de console c# dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="241b1-105">These requirements are supplied by default if you create a new C# console app project in Visual Studio 2017.</span></span> <span data-ttu-id="241b1-106">Si vous mettez à niveau un projet à partir d’une version antérieure de Visual Studio, vous devrez peut-être fournir manuellement ces références liées à LINQ.</span><span class="sxs-lookup"><span data-stu-id="241b1-106">If you're upgrading a project from an earlier version of Visual Studio, you might have to supply these LINQ-related references manually.</span></span>

<span data-ttu-id="241b1-107">LINQ to DataSet nécessite deux références supplémentaires à *System.Data.dll* et *System.Data.DataSetExtensions.dll*.</span><span class="sxs-lookup"><span data-stu-id="241b1-107">LINQ to DataSet requires two additional references to *System.Data.dll* and *System.Data.DataSetExtensions.dll*.</span></span>

> [!NOTE]
> <span data-ttu-id="241b1-108">Si vous générez à partir d’une invite de commandes, vous devez référencer manuellement les DLL liées à LINQ dans *%ProgramFiles%\Reference Assemblies\Microsoft\Framework\v3.5*.</span><span class="sxs-lookup"><span data-stu-id="241b1-108">If you're building from a command prompt, you must manually reference the LINQ-related DLLs in *%ProgramFiles%\Reference Assemblies\Microsoft\Framework\v3.5*.</span></span>

## <a name="to-enable-linq-to-dataset-functionality"></a><span data-ttu-id="241b1-109">Pour activer les fonctionnalités LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="241b1-109">To enable LINQ to DataSet functionality</span></span>

<span data-ttu-id="241b1-110">Suivez ces étapes pour activer LINQ aux fonctionnalités de jeu de données dans un projet existant.</span><span class="sxs-lookup"><span data-stu-id="241b1-110">Follow these steps to enable LINQ to DataSet functionality in an existing project.</span></span>

1. <span data-ttu-id="241b1-111">Ajouter des références aux **System.Core**, **System.Data**, et **System.Data.DataSetExtensions**.</span><span class="sxs-lookup"><span data-stu-id="241b1-111">Add references to **System.Core**, **System.Data**, and **System.Data.DataSetExtensions**.</span></span>

   <span data-ttu-id="241b1-112">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **références** nœud et sélectionnez **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="241b1-112">In **Solution Explorer**, right-click on the **References** node and select **Add Reference**.</span></span> <span data-ttu-id="241b1-113">Dans le **Gestionnaire de références** boîte de dialogue, sélectionnez **System.Core**, **System.Data**, et **System.Data.DataSetExtensions**.</span><span class="sxs-lookup"><span data-stu-id="241b1-113">In the **Reference Manager** dialog box, select **System.Core**, **System.Data**, and **System.Data.DataSetExtensions**.</span></span> <span data-ttu-id="241b1-114">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="241b1-114">Select **OK**.</span></span>

1. <span data-ttu-id="241b1-115">Ajouter [à l’aide de](../../../csharp/language-reference/keywords/using-directive.md) directives (ou [instructions Imports](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) en Visual Basic) pour **System.Data** et **System.Linq**.</span><span class="sxs-lookup"><span data-stu-id="241b1-115">Add [using](../../../csharp/language-reference/keywords/using-directive.md) directives (or [Imports statements](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) in Visual Basic) for **System.Data** and **System.Linq**.</span></span>

   ```csharp
   using System.Data;
   using System.Linq;
   ```

1. <span data-ttu-id="241b1-116">Si vous le souhaitez, ajoutez un `using` directive (ou `Imports` instruction) pour **System.Data.Common** ou **System.Data.SqlClient**, en fonction de comment vous connectez à la base de données.</span><span class="sxs-lookup"><span data-stu-id="241b1-116">Optionally, add a `using` directive (or `Imports` statement) for **System.Data.Common** or **System.Data.SqlClient**, depending on how you connect to the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="241b1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="241b1-117">See also</span></span>

- [<span data-ttu-id="241b1-118">Bien démarrer avec LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="241b1-118">Get started with LINQ to DataSet</span></span>](../../../../docs/framework/data/adonet/getting-started-linq-to-dataset.md)
