---
title: "Procédure pas à pas : création d'une application extensible"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [.NET Framework], add-in pipeline
- host-side adapters for add-ins [.NET Framework]
- add-in pipeline [.NET Framework], creating
- add-in-side adapter [.NET Framework]
- contracts for add-in pipelines [.NET Framework]
ms.assetid: 694a33c5-a040-450d-aed5-ac49fc88ce61
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d2aaeaffaf3abbe1e8efcdb57d40e6ae60f89b5
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43552333"
---
# <a name="walkthrough-creating-an-extensible-application"></a><span data-ttu-id="f5ba9-102">Procédure pas à pas : création d'une application extensible</span><span class="sxs-lookup"><span data-stu-id="f5ba9-102">Walkthrough: Creating an Extensible Application</span></span>
<span data-ttu-id="f5ba9-103">Cette procédure pas à pas décrit comment créer un pipeline pour un complément qui effectue des fonctions de calculatrice simple.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-103">This walkthrough describes how to create a pipeline for an add-in that performs simple calculator functions.</span></span> <span data-ttu-id="f5ba9-104">S’il ne présente pas un scénario réel ; au lieu de cela, il illustre les fonctionnalités de base d’un pipeline et la façon dont un complément peut fournir des services pour un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-104">It does not demonstrate a real-world scenario; rather, it demonstrates the basic functionality of a pipeline and how an add-in can provide services for a host.</span></span>  
  
 <span data-ttu-id="f5ba9-105">Cette procédure pas à pas décrit les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-105">This walkthrough describes the following tasks:</span></span>  
  
-   <span data-ttu-id="f5ba9-106">Création d’une solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-106">Creating a Visual Studio solution.</span></span>  
  
-   <span data-ttu-id="f5ba9-107">Création de la structure de répertoires du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-107">Creating the pipeline directory structure.</span></span>  
  
-   <span data-ttu-id="f5ba9-108">Création du contrat et les vues.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-108">Creating the contract and views.</span></span>  
  
-   <span data-ttu-id="f5ba9-109">Création de l’adaptateur côté complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-109">Creating the add-in-side adapter.</span></span>  
  
-   <span data-ttu-id="f5ba9-110">Création de l’adaptateur côté hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-110">Creating the host-side adapter.</span></span>  
  
-   <span data-ttu-id="f5ba9-111">Création de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-111">Creating the host.</span></span>  
  
-   <span data-ttu-id="f5ba9-112">Création du complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-112">Creating the add-in.</span></span>  
  
-   <span data-ttu-id="f5ba9-113">Déploiement du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-113">Deploying the pipeline.</span></span>  
  
-   <span data-ttu-id="f5ba9-114">L’application hôte en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-114">Running the host application.</span></span>  
  
 <span data-ttu-id="f5ba9-115">Ce pipeline passe uniquement des types sérialisables (<xref:System.Double> et <xref:System.String>), entre l’hôte et le complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-115">This pipeline passes only serializable types (<xref:System.Double> and <xref:System.String>), between the host and the add-in.</span></span> <span data-ttu-id="f5ba9-116">Pour obtenir un exemple qui montre comment passer des collections de types de données complexes, consultez [procédure pas à pas : passage de Collections entre hôtes et compléments](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-116">For an example that shows how to pass collections of complex data types, see [Walkthrough: Passing Collections Between Hosts and Add-Ins](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5).</span></span>  
  
 <span data-ttu-id="f5ba9-117">Le contrat pour ce pipeline définit un modèle d’objet de quatre opérations arithmétiques : ajouter, soustraire, multiplier et diviser.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-117">The contract for this pipeline defines an object model of four arithmetic operations: add, subtract, multiply, and divide.</span></span> <span data-ttu-id="f5ba9-118">L’hôte fournit le complément une équation à calculer, telles que 2 + 2, et le complément retourne le résultat à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-118">The host provides the add-in with an equation to calculate, such as 2 + 2, and the add-in returns the result to the host.</span></span>  
  
 <span data-ttu-id="f5ba9-119">La version 2 de la calculatrice de complément fournit des possibilités de calcul plus et montre le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-119">Version 2 of the calculator add-in provides more calculating possibilities and demonstrates versioning.</span></span> <span data-ttu-id="f5ba9-120">Il est décrit dans [procédure pas à pas : activation de la compatibilité descendante lorsque votre hôte change](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-120">It is described in [Walkthrough: Enabling Backward Compatibility as Your Host Changes](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="f5ba9-121">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f5ba9-121">Prerequisites</span></span>  
 <span data-ttu-id="f5ba9-122">Les éléments suivants sont nécessaires pour effectuer cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-122">You need the following to complete this walkthrough:</span></span>  
  
-   <span data-ttu-id="f5ba9-123">Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-123">Visual Studio.</span></span>  
  
## <a name="creating-a-visual-studio-solution"></a><span data-ttu-id="f5ba9-124">Création d’une Solution Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f5ba9-124">Creating a Visual Studio Solution</span></span>  
 <span data-ttu-id="f5ba9-125">Utiliser une solution dans Visual Studio pour contenir les projets de vos segments de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-125">Use a solution in Visual Studio to contain the projects of your pipeline segments.</span></span>  
  
#### <a name="to-create-the-pipeline-solution"></a><span data-ttu-id="f5ba9-126">Pour créer la solution de pipeline</span><span class="sxs-lookup"><span data-stu-id="f5ba9-126">To create the pipeline solution</span></span>  
  
1.  <span data-ttu-id="f5ba9-127">Dans Visual Studio, créez un projet nommé `Calc1Contract`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-127">In Visual Studio, create a new project named `Calc1Contract`.</span></span> <span data-ttu-id="f5ba9-128">Baser sur le **bibliothèque de classes** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-128">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-129">Nommez la solution `CalculatorV1`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-129">Name the solution `CalculatorV1`.</span></span>  
  
## <a name="creating-the-pipeline-directory-structure"></a><span data-ttu-id="f5ba9-130">Créer la Structure de répertoires du Pipeline</span><span class="sxs-lookup"><span data-stu-id="f5ba9-130">Creating the Pipeline Directory Structure</span></span>  
 <span data-ttu-id="f5ba9-131">Le modèle de complément nécessite les assemblys du segment de pipeline à placer dans une structure de répertoires spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-131">The add-in model requires the pipeline segment assemblies to be placed in a specified directory structure.</span></span> <span data-ttu-id="f5ba9-132">Pour plus d’informations sur la structure du pipeline, consultez [spécifications du développement de pipelines](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-132">For more information about the pipeline structure, see [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
#### <a name="to-create-the-pipeline-directory-structure"></a><span data-ttu-id="f5ba9-133">Pour créer la structure de répertoires du pipeline</span><span class="sxs-lookup"><span data-stu-id="f5ba9-133">To create the pipeline directory structure</span></span>  
  
1.  <span data-ttu-id="f5ba9-134">Créez un dossier d’application n’importe où sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-134">Create an application folder anywhere on your computer.</span></span>  
  
2.  <span data-ttu-id="f5ba9-135">Dans ce dossier, créez la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-135">In that folder, create the following structure:</span></span>  
  
    ```  
    Pipeline  
      AddIns  
        CalcV1  
        CalcV2  
      AddInSideAdapters  
      AddInViews  
      Contracts  
      HostSideAdapters  
    ```  
  
     <span data-ttu-id="f5ba9-136">Il n’est pas nécessaire de placer la structure de dossiers de pipeline dans votre dossier d’application ; Il a été fait ici uniquement pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-136">It is not necessary to put the pipeline folder structure in your application folder; it is done here only for convenience.</span></span> <span data-ttu-id="f5ba9-137">À l’étape appropriée, la procédure pas à pas explique comment modifier le code si la structure de dossiers de pipeline se trouve dans un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-137">At the appropriate step, the walkthrough explains how to change the code if the pipeline folder structure is in a different location.</span></span> <span data-ttu-id="f5ba9-138">Consultez la section traitant des spécifications du répertoire de pipelines dans [spécifications du développement de pipelines](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-138">See the discussion of pipeline directory requirements in [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="f5ba9-139">Le `CalcV2` dossier n’est pas utilisé dans cette procédure pas à pas ; il est un espace réservé pour [procédure pas à pas : activation de la compatibilité descendante lorsque votre hôte change](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-139">The `CalcV2` folder is not used in this walkthrough; it is a placeholder for [Walkthrough: Enabling Backward Compatibility as Your Host Changes](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848).</span></span>  
  
## <a name="creating-the-contract-and-views"></a><span data-ttu-id="f5ba9-140">Création du contrat et les vues</span><span class="sxs-lookup"><span data-stu-id="f5ba9-140">Creating the Contract and Views</span></span>  
 <span data-ttu-id="f5ba9-141">Le segment de contrat pour ce pipeline définit la `ICalc1Contract` interface qui définit quatre méthodes : `add`, `subtract`, `multiply`, et `divide`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-141">The contract segment for this pipeline defines the `ICalc1Contract` interface, which defines four methods: `add`, `subtract`, `multiply`, and `divide`.</span></span>  
  
#### <a name="to-create-the-contract"></a><span data-ttu-id="f5ba9-142">Pour créer le contrat</span><span class="sxs-lookup"><span data-stu-id="f5ba9-142">To create the contract</span></span>  
  
1.  <span data-ttu-id="f5ba9-143">Dans la solution Visual Studio nommée `CalculatorV1`, ouvrez le `Calc1Contract` projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-143">In the Visual Studio solution named `CalculatorV1`, open the `Calc1Contract` project.</span></span>  
  
2.  <span data-ttu-id="f5ba9-144">Dans **l’Explorateur de solutions**, ajoutez des références aux assemblys suivants à la `Calc1Contract` projet :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-144">In **Solution Explorer**, add references to the following assemblies to the `Calc1Contract` project:</span></span>  
  
     <span data-ttu-id="f5ba9-145">System.AddIn.Contract.dll</span><span class="sxs-lookup"><span data-stu-id="f5ba9-145">System.AddIn.Contract.dll</span></span>  
  
     <span data-ttu-id="f5ba9-146">System.AddIn.dll</span><span class="sxs-lookup"><span data-stu-id="f5ba9-146">System.AddIn.dll</span></span>  
  
3.  <span data-ttu-id="f5ba9-147">Dans **l’Explorateur de solutions**, excluez la classe par défaut qui est ajoutée au nouveau **bibliothèque de classes** projets.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-147">In **Solution Explorer**, exclude the default class that is added to new **Class Library** projects.</span></span>  
  
4.  <span data-ttu-id="f5ba9-148">Dans **l’Explorateur de solutions**, ajouter un nouvel élément au projet, à l’aide de la **Interface** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-148">In **Solution Explorer**, add a new item to the project, using the **Interface** template.</span></span> <span data-ttu-id="f5ba9-149">Dans le **ajouter un nouvel élément** boîte de dialogue, nom de l’interface `ICalc1Contract`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-149">In the **Add New Item** dialog box, name the interface `ICalc1Contract`.</span></span>  
  
5.  <span data-ttu-id="f5ba9-150">Dans le fichier d’interface, ajoutez des références d’espace de noms aux <xref:System.AddIn.Contract> et <xref:System.AddIn.Pipeline>.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-150">In the interface file, add namespace references to <xref:System.AddIn.Contract> and <xref:System.AddIn.Pipeline>.</span></span>  
  
6.  <span data-ttu-id="f5ba9-151">Utilisez le code suivant pour terminer ce segment de contrat.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-151">Use the following code to complete this contract segment.</span></span> <span data-ttu-id="f5ba9-152">Notez que cette interface doit avoir le <xref:System.AddIn.Pipeline.AddInContractAttribute> attribut.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-152">Note that this interface must have the <xref:System.AddIn.Pipeline.AddInContractAttribute> attribute.</span></span>  
  
     [!code-csharp[AddInP1Contract#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Contract/cs/ICalc1Contract.cs#1)]
     [!code-vb[AddInP1Contract#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Contract/vb/ICalc1Contract.vb#1)]  
  
7.  <span data-ttu-id="f5ba9-153">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-153">Optionally, build the Visual Studio solution.</span></span> <span data-ttu-id="f5ba9-154">La solution ne peut pas être exécutée jusqu'à ce que la dernière procédure, mais la générer après que chaque procédure garantit que chaque projet est corriger.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-154">The solution cannot be run until the final procedure, but building it after each procedure ensures that each project is correct.</span></span>  
  
 <span data-ttu-id="f5ba9-155">Étant donné que la vue de complément et la vue hôte du complément ont généralement le même code, en particulier dans la première version d’un complément, vous pouvez facilement créer des vues en même temps.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-155">Because the add-in view and the host view of the add-in usually have the same code, especially in the first version of an add-in, you can easily create the views at the same time.</span></span> <span data-ttu-id="f5ba9-156">Ils diffèrent selon qu’un seul facteur : la vue de complément nécessite le <xref:System.AddIn.Pipeline.AddInBaseAttribute> d’attributs, tandis que la vue hôte du complément-ne nécessite pas tous les attributs.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-156">They differ by only one factor: the add-in view requires the <xref:System.AddIn.Pipeline.AddInBaseAttribute> attribute, while the host view of the add-in does not require any attributes.</span></span>  
  
#### <a name="to-create-the-add-in-view"></a><span data-ttu-id="f5ba9-157">Pour créer la vue de complément</span><span class="sxs-lookup"><span data-stu-id="f5ba9-157">To create the add-in view</span></span>  
  
1.  <span data-ttu-id="f5ba9-158">Ajouter un nouveau projet nommé `Calc1AddInView` à la `CalculatorV1` solution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-158">Add a new project named `Calc1AddInView` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="f5ba9-159">Baser sur le **bibliothèque de classes** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-159">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-160">Dans **l’Explorateur de solutions**, ajoutez une référence à System.AddIn.dll à la `Calc1AddInView` projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-160">In **Solution Explorer**, add a reference to System.AddIn.dll to the `Calc1AddInView` project.</span></span>  
  
3.  <span data-ttu-id="f5ba9-161">Dans **l’Explorateur de solutions**, excluez la classe par défaut qui est ajoutée au nouveau **bibliothèque de classes** des projets et ajouter un nouvel élément au projet, à l’aide de la **Interface** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-161">In **Solution Explorer**, exclude the default class that is added to new **Class Library** projects, and add a new item to the project, using the **Interface** template.</span></span> <span data-ttu-id="f5ba9-162">Dans le **ajouter un nouvel élément** boîte de dialogue, nom de l’interface `ICalculator`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-162">In the **Add New Item** dialog box, name the interface `ICalculator`.</span></span>  
  
4.  <span data-ttu-id="f5ba9-163">Dans le fichier d’interface, ajoutez une référence d’espace de noms à <xref:System.AddIn.Pipeline>.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-163">In the interface file, add a namespace reference to <xref:System.AddIn.Pipeline>.</span></span>  
  
5.  <span data-ttu-id="f5ba9-164">Utilisez le code suivant pour terminer cette vue de complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-164">Use the following code to complete this add-in view.</span></span> <span data-ttu-id="f5ba9-165">Notez que cette interface doit avoir le <xref:System.AddIn.Pipeline.AddInBaseAttribute> attribut.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-165">Note that this interface must have the <xref:System.AddIn.Pipeline.AddInBaseAttribute> attribute.</span></span>  
  
     [!code-csharp[AddInP1AddInViews#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInViews/cs/Calc1AddInView.cs#1)]
     [!code-vb[AddInP1AddInViews#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInViews/vb/Calc1AddInView.vb#1)]  
  
6.  <span data-ttu-id="f5ba9-166">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-166">Optionally, build the Visual Studio solution.</span></span>  
  
#### <a name="to-create-the-host-view-of-the-add-in"></a><span data-ttu-id="f5ba9-167">Pour créer la vue hôte du complément-</span><span class="sxs-lookup"><span data-stu-id="f5ba9-167">To create the host view of the add-in</span></span>  
  
1.  <span data-ttu-id="f5ba9-168">Ajouter un nouveau projet nommé `Calc1HVA` à la `CalculatorV1` solution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-168">Add a new project named `Calc1HVA` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="f5ba9-169">Baser sur le **bibliothèque de classes** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-169">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-170">Dans **l’Explorateur de solutions**, excluez la classe par défaut qui est ajoutée au nouveau **bibliothèque de classes** des projets et ajouter un nouvel élément au projet, à l’aide de la **Interface** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-170">In **Solution Explorer**, exclude the default class that is added to new **Class Library** projects, and add a new item to the project, using the **Interface** template.</span></span> <span data-ttu-id="f5ba9-171">Dans le **ajouter un nouvel élément** boîte de dialogue, nom de l’interface `ICalculator`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-171">In the **Add New Item** dialog box, name the interface `ICalculator`.</span></span>  
  
3.  <span data-ttu-id="f5ba9-172">Dans le fichier d’interface, utilisez le code suivant pour terminer la vue hôte du complément en.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-172">In the interface file, use the following code to complete the host view of the add-in.</span></span>  
  
     [!code-csharp[AddInP1HVA#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HVA/cs/calc1hva.cs#1)]
     [!code-vb[AddInP1HVA#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HVA/vb/Calc1HVA.vb#1)]  
  
4.  <span data-ttu-id="f5ba9-173">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-173">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-add-in-side-adapter"></a><span data-ttu-id="f5ba9-174">Création de l’adaptateur côté complément</span><span class="sxs-lookup"><span data-stu-id="f5ba9-174">Creating the Add-in-side Adapter</span></span>  
 <span data-ttu-id="f5ba9-175">Cet adaptateur côté complément se compose d’un adaptateur vue-en-contrat.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-175">This add-in-side adapter consists of one view-to-contract adapter.</span></span> <span data-ttu-id="f5ba9-176">Ce segment de pipeline convertit les types à partir de la vue de complément du contrat.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-176">This pipeline segment converts the types from the add-in view to the contract.</span></span>  
  
 <span data-ttu-id="f5ba9-177">Dans ce pipeline, le complément fournit un service à l’hôte, et les types de flux à partir du complément à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-177">In this pipeline, the add-in provides a service to the host, and the types flow from the add-in to the host.</span></span> <span data-ttu-id="f5ba9-178">Car aucun type de flux de l’hôte vers le complément, vous n’avez pas à inclure un adaptateur contrat-en-vue sur le côté complément de ce pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-178">Because no types flow from the host to the add-in, you do not have to include a contract-to-view adapter on the add-in side of this pipeline.</span></span>  
  
#### <a name="to-create-the-add-in-side-adapter"></a><span data-ttu-id="f5ba9-179">Pour créer l’adaptateur côté complément</span><span class="sxs-lookup"><span data-stu-id="f5ba9-179">To create the add-in-side adapter</span></span>  
  
1.  <span data-ttu-id="f5ba9-180">Ajouter un nouveau projet nommé `Calc1AddInSideAdapter` à la `CalculatorV1` solution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-180">Add a new project named `Calc1AddInSideAdapter` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="f5ba9-181">Baser sur le **bibliothèque de classes** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-181">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-182">Dans **l’Explorateur de solutions**, ajoutez des références aux assemblys suivants à la `Calc1AddInSideAdapter` projet :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-182">In **Solution Explorer**, add references to the following assemblies to the `Calc1AddInSideAdapter` project:</span></span>  
  
     <span data-ttu-id="f5ba9-183">System.AddIn.dll</span><span class="sxs-lookup"><span data-stu-id="f5ba9-183">System.AddIn.dll</span></span>  
  
     <span data-ttu-id="f5ba9-184">System.AddIn.Contract.dll</span><span class="sxs-lookup"><span data-stu-id="f5ba9-184">System.AddIn.Contract.dll</span></span>  
  
3.  <span data-ttu-id="f5ba9-185">Ajouter des références de projet pour les projets pour les segments de pipeline adjacents :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-185">Add project references to the projects for the adjacent pipeline segments:</span></span>  
  
     `Calc1AddInView`  
  
     `Calc1Contract`  
  
4.  <span data-ttu-id="f5ba9-186">Sélectionnez chaque référence de projet, puis, dans **propriétés** définir **copie locale** à **False**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-186">Select each project reference, and in **Properties** set **Copy Local** to **False**.</span></span> <span data-ttu-id="f5ba9-187">Dans Visual Basic, utilisez la **références** onglet de **propriétés du projet** pour définir **copie locale** à **False** pour les deux références de projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-187">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False** for the two project references.</span></span>  
  
5.  <span data-ttu-id="f5ba9-188">Renommer la classe du projet par défaut `CalculatorViewToContractAddInSideAdapter`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-188">Rename the project's default class `CalculatorViewToContractAddInSideAdapter`.</span></span>  
  
6.  <span data-ttu-id="f5ba9-189">Dans le fichier de classe, ajoutez des références d’espace de noms à <xref:System.AddIn.Pipeline>.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-189">In the class file, add namespace references to <xref:System.AddIn.Pipeline>.</span></span>  
  
7.  <span data-ttu-id="f5ba9-190">Dans le fichier de classe, ajoutez des références d’espace de noms pour les segments adjacents : `CalcAddInViews` et `CalculatorContracts`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-190">In the class file, add namespace references for the adjacent segments: `CalcAddInViews` and `CalculatorContracts`.</span></span> <span data-ttu-id="f5ba9-191">(En Visual Basic, ces références d’espace de noms sont `Calc1AddInView.CalcAddInViews` et `Calc1Contract.CalculatorContracts`, sauf si vous avez désactivé les espaces de noms par défaut dans vos projets Visual Basic.)</span><span class="sxs-lookup"><span data-stu-id="f5ba9-191">(In Visual Basic, these namespace references are `Calc1AddInView.CalcAddInViews` and `Calc1Contract.CalculatorContracts`, unless you have turned off the default namespaces in your Visual Basic projects.)</span></span>  
  
8.  <span data-ttu-id="f5ba9-192">Appliquer le <xref:System.AddIn.Pipeline.AddInAdapterAttribute> attribut le `CalculatorViewToContractAddInSideAdapter` (classe), pour l’identifier comme l’adaptateur côté complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-192">Apply the <xref:System.AddIn.Pipeline.AddInAdapterAttribute> attribute to the `CalculatorViewToContractAddInSideAdapter` class, to identify it as the add-in-side adapter.</span></span>  
  
9. <span data-ttu-id="f5ba9-193">Rendre le `CalculatorViewToContractAddInSideAdapter` héritent de la classe <xref:System.AddIn.Pipeline.ContractBase>, qui fournit une implémentation par défaut de la <xref:System.AddIn.Contract.IContract> interface et implémenter l’interface de contrat pour le pipeline, `ICalc1Contract`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-193">Make the `CalculatorViewToContractAddInSideAdapter` class inherit <xref:System.AddIn.Pipeline.ContractBase>, which provides a default implementation of the <xref:System.AddIn.Contract.IContract> interface, and implement the contract interface for the pipeline, `ICalc1Contract`.</span></span>  
  
10. <span data-ttu-id="f5ba9-194">Ajoutez un constructeur public qui accepte un `ICalculator`, il met en cache dans un champ privé et appelle le constructeur de classe de base.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-194">Add a public constructor that accepts an `ICalculator`, caches it in a private field, and calls the base class constructor.</span></span>  
  
11. <span data-ttu-id="f5ba9-195">Pour implémenter les membres de `ICalc1Contract`, appelez simplement les membres correspondants de la `ICalculator` instance qui est passée au constructeur et retourne les résultats.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-195">To implement the members of `ICalc1Contract`, simply call the corresponding members of the `ICalculator` instance that is passed to the constructor, and return the results.</span></span> <span data-ttu-id="f5ba9-196">Il s’adapte à la vue (`ICalculator`) au contrat (`ICalc1Contract`).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-196">This adapts the view (`ICalculator`) to the contract (`ICalc1Contract`).</span></span>  
  
     <span data-ttu-id="f5ba9-197">Le code suivant montre l’adaptateur côté complément terminé.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-197">The following code shows the completed add-in-side adapter.</span></span>  
  
     [!code-csharp[AddInP1AddInSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInSideAdapters/cs/Calc1ViewToContractAddInSideAdapter.cs#1)]
     [!code-vb[AddInP1AddInSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInSideAdapters/vb/Calc1ViewToContractAddInSideAdapter.vb#1)]  
  
12. <span data-ttu-id="f5ba9-198">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-198">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-host-side-adapter"></a><span data-ttu-id="f5ba9-199">Création de l’adaptateur côté hôte</span><span class="sxs-lookup"><span data-stu-id="f5ba9-199">Creating the Host-side Adapter</span></span>  
 <span data-ttu-id="f5ba9-200">Cet adaptateur côté hôte se compose d’un adaptateur contrat-en-vue.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-200">This host-side adapter consists of one contract-to-view adapter.</span></span> <span data-ttu-id="f5ba9-201">Ce segment adapte le contrat à la vue hôte du complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-201">This segment adapts the contract to the host view of the add-in.</span></span>  
  
 <span data-ttu-id="f5ba9-202">Dans ce pipeline, le complément fournit un service à l’hôte et le flux de types à partir du complément à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-202">In this pipeline, the add-in provides a service to the host and the types flow from the add-in to the host.</span></span> <span data-ttu-id="f5ba9-203">Car aucun type de flux de l’hôte vers le complément, vous n’avez pas à inclure un adaptateur vue-en-contrat.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-203">Because no types flow from the host to the add-in, you do not have to include a view-to-contract adapter.</span></span>  
  
 <span data-ttu-id="f5ba9-204">Pour implémenter la gestion de la durée de vie, utilisez un <xref:System.AddIn.Pipeline.ContractHandle> objet à attacher un jeton de durée de vie au contrat.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-204">To implement lifetime management, use a <xref:System.AddIn.Pipeline.ContractHandle> object to attach a lifetime token to the contract.</span></span> <span data-ttu-id="f5ba9-205">Vous devez conserver une référence à ce handle dans l’ordre pour la gestion de durée de vie fonctionne.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-205">You must keep a reference to this handle in order for lifetime management to work.</span></span> <span data-ttu-id="f5ba9-206">Une fois le jeton est appliqué, aucune programmation supplémentaire n’est nécessaire, car le système de complément peut supprimer les objets lorsqu’ils ne sont plus utilisés et les rendre disponibles pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-206">After the token is applied, no additional programming is required because the add-in system can dispose of objects when they are no longer being used and make them available for garbage collection.</span></span> <span data-ttu-id="f5ba9-207">Pour plus d’informations, consultez [Lifetime Management](https://msdn.microsoft.com/library/57a9c87e-394c-4fef-89f2-aa4223a2aeb5).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-207">For more information, see [Lifetime Management](https://msdn.microsoft.com/library/57a9c87e-394c-4fef-89f2-aa4223a2aeb5).</span></span>  
  
#### <a name="to-create-the-host-side-adapter"></a><span data-ttu-id="f5ba9-208">Pour créer l’adaptateur côté hôte</span><span class="sxs-lookup"><span data-stu-id="f5ba9-208">To create the host-side adapter</span></span>  
  
1.  <span data-ttu-id="f5ba9-209">Ajouter un nouveau projet nommé `Calc1HostSideAdapter` à la `CalculatorV1` solution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-209">Add a new project named `Calc1HostSideAdapter` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="f5ba9-210">Baser sur le **bibliothèque de classes** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-210">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-211">Dans **l’Explorateur de solutions**, ajoutez des références aux assemblys suivants à la `Calc1HostSideAdapter` projet :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-211">In **Solution Explorer**, add references to the following assemblies to the `Calc1HostSideAdapter` project:</span></span>  
  
     <span data-ttu-id="f5ba9-212">System.AddIn.dll</span><span class="sxs-lookup"><span data-stu-id="f5ba9-212">System.AddIn.dll</span></span>  
  
     <span data-ttu-id="f5ba9-213">System.AddIn.Contract.dll</span><span class="sxs-lookup"><span data-stu-id="f5ba9-213">System.AddIn.Contract.dll</span></span>  
  
3.  <span data-ttu-id="f5ba9-214">Ajouter des références de projet pour les projets pour les segments adjacents :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-214">Add project references to the projects for the adjacent segments:</span></span>  
  
     `Calc1Contract`  
  
     `Calc1HVA`  
  
4.  <span data-ttu-id="f5ba9-215">Sélectionnez chaque référence de projet, puis, dans **propriétés** définir **copie locale** à **False**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-215">Select each project reference, and in **Properties** set **Copy Local** to **False**.</span></span> <span data-ttu-id="f5ba9-216">Dans Visual Basic, utilisez la **références** onglet de **propriétés du projet** pour définir **copie locale** à **False** pour les deux références de projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-216">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False** for the two project references.</span></span>  
  
5.  <span data-ttu-id="f5ba9-217">Renommer la classe du projet par défaut `CalculatorContractToViewHostSideAdapter`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-217">Rename the project's default class `CalculatorContractToViewHostSideAdapter`.</span></span>  
  
6.  <span data-ttu-id="f5ba9-218">Dans le fichier de classe, ajoutez des références d’espace de noms à <xref:System.AddIn.Pipeline>.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-218">In the class file, add namespace references to <xref:System.AddIn.Pipeline>.</span></span>  
  
7.  <span data-ttu-id="f5ba9-219">Dans le fichier de classe, ajoutez des références d’espace de noms pour les segments adjacents : `CalcHVAs` et `CalculatorContracts`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-219">In the class file, add namespace references for the adjacent segments: `CalcHVAs` and `CalculatorContracts`.</span></span> <span data-ttu-id="f5ba9-220">(En Visual Basic, ces références d’espace de noms sont `Calc1HVA.CalcHVAs` et `Calc1Contract.CalculatorContracts`, sauf si vous avez désactivé les espaces de noms par défaut dans vos projets Visual Basic.)</span><span class="sxs-lookup"><span data-stu-id="f5ba9-220">(In Visual Basic, these namespace references are `Calc1HVA.CalcHVAs` and `Calc1Contract.CalculatorContracts`, unless you have turned off the default namespaces in your Visual Basic projects.)</span></span>  
  
8.  <span data-ttu-id="f5ba9-221">Appliquer le <xref:System.AddIn.Pipeline.HostAdapterAttribute> attribut le `CalculatorContractToViewHostSideAdapter` (classe), pour l’identifier comme le segment d’adaptateur côté hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-221">Apply the <xref:System.AddIn.Pipeline.HostAdapterAttribute> attribute to the `CalculatorContractToViewHostSideAdapter` class, to identify it as the host-side adapter segment.</span></span>  
  
9. <span data-ttu-id="f5ba9-222">Rendre le `CalculatorContractToViewHostSideAdapter` classe implémente l’interface qui représente la vue hôte du complément- : `Calc1HVAs.ICalculator` (`Calc1HVA.CalcHVAs.ICalculator` en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-222">Make the `CalculatorContractToViewHostSideAdapter` class implement the interface that represents the host view of the add-in: `Calc1HVAs.ICalculator` (`Calc1HVA.CalcHVAs.ICalculator` in Visual Basic).</span></span>  
  
10. <span data-ttu-id="f5ba9-223">Ajoutez un constructeur public qui accepte le type de contrat de pipeline, `ICalc1Contract`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-223">Add a public constructor that accepts the pipeline contract type, `ICalc1Contract`.</span></span> <span data-ttu-id="f5ba9-224">Le constructeur doit mettre en cache la référence au contrat.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-224">The constructor must cache the reference to the contract.</span></span> <span data-ttu-id="f5ba9-225">Il doit également créer et mettre en cache un nouveau <xref:System.AddIn.Pipeline.ContractHandle> pour le contrat, pour gérer la durée de vie de la macro complémentaire.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-225">It must also create and cache a new <xref:System.AddIn.Pipeline.ContractHandle> for the contract, to manage the lifetime of the add-in.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="f5ba9-226">Le <xref:System.AddIn.Pipeline.ContractHandle> est essentiel à la gestion de la durée de vie.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-226">The <xref:System.AddIn.Pipeline.ContractHandle> is critical to lifetime management.</span></span> <span data-ttu-id="f5ba9-227">Si vous ne parvenez pas à conserver une référence à la <xref:System.AddIn.Pipeline.ContractHandle> de l’objet, le garbage collection récupère et le pipeline s’arrêtera lorsque votre programme n’attend pas cela.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-227">If you fail to keep a reference to the <xref:System.AddIn.Pipeline.ContractHandle> object, garbage collection will reclaim it, and the pipeline will shut down when your program does not expect it.</span></span> <span data-ttu-id="f5ba9-228">Cela peut entraîner des erreurs qui sont difficiles à diagnostiquer, tel que <xref:System.AppDomainUnloadedException>.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-228">This can lead to errors that are difficult to diagnose, such as <xref:System.AppDomainUnloadedException>.</span></span> <span data-ttu-id="f5ba9-229">Arrêt étant une phase normale de la durée de vie d’un pipeline, il n’existe aucun moyen pour le code de gestion de durée de vie détecter que cette condition est une erreur.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-229">Shutdown is a normal stage in the life of a pipeline, so there is no way for the lifetime management code to detect that this condition is an error.</span></span>  
  
11. <span data-ttu-id="f5ba9-230">Pour implémenter les membres de `ICalculator`, appelez simplement les membres correspondants de la `ICalc1Contract` instance qui est passée au constructeur et retourne les résultats.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-230">To implement the members of `ICalculator`, simply call the corresponding members of the `ICalc1Contract` instance that is passed to the constructor, and return the results.</span></span> <span data-ttu-id="f5ba9-231">Cela s’adapte le contrat (`ICalc1Contract`) à la vue (`ICalculator`).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-231">This adapts the contract (`ICalc1Contract`) to the view (`ICalculator`).</span></span>  
  
     <span data-ttu-id="f5ba9-232">Le code suivant montre l’adaptateur côté hôte terminé.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-232">The following code shows the completed host-side adapter.</span></span>  
  
     [!code-csharp[AddInP1HostSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HostSideAdapters/cs/Calc1ContractToViewHostSideAdapter.cs#1)]
     [!code-vb[AddInP1HostSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HostSideAdapters/vb/Calc1ContractToViewHostSideAdapter.vb#1)]  
  
12. <span data-ttu-id="f5ba9-233">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-233">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-host"></a><span data-ttu-id="f5ba9-234">Création de l’hôte</span><span class="sxs-lookup"><span data-stu-id="f5ba9-234">Creating the Host</span></span>  
 <span data-ttu-id="f5ba9-235">Une application hôte interagit avec le complément via la vue hôte du complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-235">A host application interacts with the add-in through the host view of the add-in.</span></span> <span data-ttu-id="f5ba9-236">Il utilise des méthodes d’activation et de découverte de complément fournies par le <xref:System.AddIn.Hosting.AddInStore> et <xref:System.AddIn.Hosting.AddInToken> classes pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-236">It uses add-in discovery and activation methods provided by the <xref:System.AddIn.Hosting.AddInStore> and <xref:System.AddIn.Hosting.AddInToken> classes to do the following:</span></span>  
  
-   <span data-ttu-id="f5ba9-237">Mettre à jour le cache des informations de pipeline et de complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-237">Update the cache of pipeline and add-in information.</span></span>  
  
-   <span data-ttu-id="f5ba9-238">Rechercher des compléments du type de vue d’hôte, `ICalculator`, sous le répertoire racine de pipeline spécifié.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-238">Find add-ins of the host view type, `ICalculator`, under the specified pipeline root directory.</span></span>  
  
-   <span data-ttu-id="f5ba9-239">Inviter l’utilisateur à spécifier le complément à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-239">Prompt the user to specify which add-in to use.</span></span>  
  
-   <span data-ttu-id="f5ba9-240">Activer le complément sélectionné dans un nouveau domaine d’application avec un niveau de confiance de sécurité spécifié.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-240">Activate the selected add-in in a new application domain with a specified security trust level.</span></span>  
  
-   <span data-ttu-id="f5ba9-241">Exécutez personnalisé `RunCalculator` (méthode), qui appelle méthodes du complément comme spécifié par la vue hôte du complément-.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-241">Run the custom `RunCalculator` method, which calls the add-in's methods as specified by the host view of the add-in.</span></span>  
  
#### <a name="to-create-the-host"></a><span data-ttu-id="f5ba9-242">Pour créer l’hôte</span><span class="sxs-lookup"><span data-stu-id="f5ba9-242">To create the host</span></span>  
  
1.  <span data-ttu-id="f5ba9-243">Ajouter un nouveau projet nommé `Calc1Host` à la `CalculatorV1` solution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-243">Add a new project named `Calc1Host` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="f5ba9-244">Baser sur le **Application Console** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-244">Base it on the **Console Application** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-245">Dans **l’Explorateur de solutions**, ajoutez une référence à l’assembly System.AddIn.dll à la `Calc1Host` projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-245">In **Solution Explorer**, add a reference to the System.AddIn.dll assembly to the `Calc1Host` project.</span></span>  
  
3.  <span data-ttu-id="f5ba9-246">Ajouter une référence de projet à la `Calc1HVA` projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-246">Add a project reference to the `Calc1HVA` project.</span></span> <span data-ttu-id="f5ba9-247">Sélectionnez la référence de projet, puis, dans **propriétés** définir **copie locale** à **False**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-247">Select the project reference, and in **Properties** set **Copy Local** to **False**.</span></span> <span data-ttu-id="f5ba9-248">Dans Visual Basic, utilisez la **références** onglet de **propriétés du projet** pour définir **copie locale** à **False**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-248">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False**.</span></span>  
  
4.  <span data-ttu-id="f5ba9-249">Renommez le fichier de classe (module en Visual Basic) `MathHost1`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-249">Rename the class file (module in Visual Basic) `MathHost1`.</span></span>  
  
5.  <span data-ttu-id="f5ba9-250">Dans Visual Basic, utilisez la **Application** onglet de la **propriétés du projet** boîte de dialogue pour définir **objet de démarrage** à **Sub Main**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-250">In Visual Basic, use the **Application** tab of the **Project Properties** dialog box to set **Startup object** to **Sub Main**.</span></span>  
  
6.  <span data-ttu-id="f5ba9-251">Dans le fichier de classe ou le module, ajoutez une référence d’espace de noms à <xref:System.AddIn.Hosting>.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-251">In the class or module file, add a namespace reference to <xref:System.AddIn.Hosting>.</span></span>  
  
7.  <span data-ttu-id="f5ba9-252">Dans le fichier de classe ou le module, ajoutez une référence d’espace de noms pour la vue hôte du complément en : `CalcHVAs`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-252">In the class or module file, add a namespace reference for the host view of the add-in: `CalcHVAs`.</span></span> <span data-ttu-id="f5ba9-253">(En Visual Basic, cette référence d’espace de noms est `Calc1HVA.CalcHVAs`, sauf si vous avez désactivé les espaces de noms par défaut dans vos projets Visual Basic.)</span><span class="sxs-lookup"><span data-stu-id="f5ba9-253">(In Visual Basic, this namespace reference is `Calc1HVA.CalcHVAs`, unless you have turned off the default namespaces in your Visual Basic projects.)</span></span>  
  
8.  <span data-ttu-id="f5ba9-254">Dans **l’Explorateur de solutions**, sélectionnez la solution et à partir de la **projet** menu Choisissez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-254">In **Solution Explorer**, select the solution and from the **Project** menu choose **Properties**.</span></span> <span data-ttu-id="f5ba9-255">Dans le **Pages de propriétés de Solution** boîte de dialogue, définissez la **projet de démarrage unique** à ce projet d’application hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-255">In the **Solution Property Pages** dialog box, set the **Single Startup Project** to be this host application project.</span></span>  
  
9. <span data-ttu-id="f5ba9-256">Dans le fichier de classe ou un module, utilisez la <xref:System.AddIn.Hosting.AddInStore.Update%2A?displayProperty=nameWithType> méthode pour mettre à jour le cache.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-256">In the class or module file, use the <xref:System.AddIn.Hosting.AddInStore.Update%2A?displayProperty=nameWithType> method to update the cache.</span></span> <span data-ttu-id="f5ba9-257">Utiliser le <xref:System.AddIn.Hosting.AddInStore.FindAddIn%2A?displayProperty=nameWithType> méthode pour obtenir une collection de jetons et le <xref:System.AddIn.Hosting.AddInToken.Activate%2A?displayProperty=nameWithType> méthode permettant d’activer un complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-257">Use the <xref:System.AddIn.Hosting.AddInStore.FindAddIn%2A?displayProperty=nameWithType> method to get a collection of tokens, and use the <xref:System.AddIn.Hosting.AddInToken.Activate%2A?displayProperty=nameWithType> method to activate an add-in.</span></span>  
  
     <span data-ttu-id="f5ba9-258">Le code suivant montre l’application hôte terminée.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-258">The following code shows the completed host application.</span></span>  
  
     [!code-csharp[AddInP1Host#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Host/cs/MathHost1.cs#1)]
     [!code-vb[AddInP1Host#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Host/vb/MathHost1.vb#1)]  
  
    > [!NOTE]
    >  <span data-ttu-id="f5ba9-259">Ce code suppose que la structure de dossiers de pipeline se trouve dans le dossier d’application.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-259">This code assumes that the pipeline folder structure is located in the application folder.</span></span> <span data-ttu-id="f5ba9-260">Si vous avez localisé ailleurs, modifiez la ligne de code qui définit le `addInRoot` variable, afin que la variable contient le chemin d’accès à votre structure de répertoires du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-260">If you located it elsewhere, change the line of code that sets the `addInRoot` variable, so that the variable contains the path to your pipeline directory structure.</span></span>  
  
     <span data-ttu-id="f5ba9-261">Le code utilise un `ChooseCalculator` méthode pour répertorier les jetons et inviter l’utilisateur à choisir un complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-261">The code uses a `ChooseCalculator` method to list the tokens and to prompt the user to choose an add-in.</span></span> <span data-ttu-id="f5ba9-262">Le `RunCalculator` méthode invite l’utilisateur pour les expressions mathématiques simples, analyse les expressions à l’aide de la `Parser` classe et affiche les résultats retournés par le complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-262">The `RunCalculator` method prompts the user for simple math expressions, parses the expressions using the `Parser` class, and displays the results returned by the add-in.</span></span>  
  
10. <span data-ttu-id="f5ba9-263">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-263">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-add-in"></a><span data-ttu-id="f5ba9-264">Création du complément</span><span class="sxs-lookup"><span data-stu-id="f5ba9-264">Creating the Add-In</span></span>  
 <span data-ttu-id="f5ba9-265">Un complément implémente les méthodes spécifiées par la vue de complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-265">An add-in implements the methods specified by the add-in view.</span></span> <span data-ttu-id="f5ba9-266">Ce complément implémente la `Add`, `Subtract`, `Multiply`, et `Divide` operations et renvoie les résultats à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-266">This add-in implements the `Add`, `Subtract`, `Multiply`, and `Divide` operations and returns the results to the host.</span></span>  
  
#### <a name="to-create-the-add-in"></a><span data-ttu-id="f5ba9-267">Pour créer le complément</span><span class="sxs-lookup"><span data-stu-id="f5ba9-267">To create the add-in</span></span>  
  
1.  <span data-ttu-id="f5ba9-268">Ajouter un nouveau projet nommé `AddInCalcV1` à la `CalculatorV1` solution.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-268">Add a new project named `AddInCalcV1` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="f5ba9-269">Baser sur le **bibliothèque de classes** modèle.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-269">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="f5ba9-270">Dans **l’Explorateur de solutions**, ajoutez une référence à l’assembly System.AddIn.dll au projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-270">In **Solution Explorer**, add a reference to the System.AddIn.dll assembly to the project.</span></span>  
  
3.  <span data-ttu-id="f5ba9-271">Ajouter une référence de projet à la `Calc1AddInView` projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-271">Add a project reference to the `Calc1AddInView` project.</span></span> <span data-ttu-id="f5ba9-272">Sélectionnez la référence de projet, puis, dans **propriétés**, affectez la valeur **copie locale** à **False**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-272">Select the project reference, and in **Properties**, set **Copy Local** to **False**.</span></span> <span data-ttu-id="f5ba9-273">Dans Visual Basic, utilisez la **références** onglet de **propriétés du projet** pour définir **copie locale** à **False** pour la référence de projet.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-273">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False** for the project reference.</span></span>  
  
4.  <span data-ttu-id="f5ba9-274">Renommez la classe `AddInCalcV1`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-274">Rename the class `AddInCalcV1`.</span></span>  
  
5.  <span data-ttu-id="f5ba9-275">Dans le fichier de classe, ajoutez une référence d’espace de noms à <xref:System.AddIn> et le segment de vue de complément : `CalcAddInViews` (`Calc1AddInView.CalcAddInViews` en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-275">In the class file, add a namespace reference to <xref:System.AddIn> and the add-in view segment: `CalcAddInViews` (`Calc1AddInView.CalcAddInViews` in Visual Basic).</span></span>  
  
6.  <span data-ttu-id="f5ba9-276">Appliquer le <xref:System.AddIn.AddInAttribute> attribut le `AddInCalcV1` (classe), pour identifier la classe comme un complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-276">Apply the <xref:System.AddIn.AddInAttribute> attribute to the `AddInCalcV1` class, to identify the class as an add-in.</span></span>  
  
7.  <span data-ttu-id="f5ba9-277">Rendre le `AddInCalcV1` classe implémente l’interface qui représente la vue de complément : `CalcAddInViews.ICalculator` (`Calc1AddInView.CalcAddInViews.ICalculator` en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-277">Make the `AddInCalcV1` class implement the interface that represents the add-in view: `CalcAddInViews.ICalculator` (`Calc1AddInView.CalcAddInViews.ICalculator` in Visual Basic).</span></span>  
  
8.  <span data-ttu-id="f5ba9-278">Implémenter les membres de `ICalculator` en retournant les résultats des calculs appropriés.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-278">Implement the members of `ICalculator` by returning the results of the appropriate calculations.</span></span>  
  
     <span data-ttu-id="f5ba9-279">Le code suivant montre le complément terminé.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-279">The following code shows the completed add-in.</span></span>  
  
     [!code-csharp[AddInP1AddInCalcV1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInCalcV1/cs/AddInCalcV1.cs#1)]
     [!code-vb[AddInP1AddInCalcV1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInCalcV1/vb/AddInCalcV1.vb#1)]  
  
9. <span data-ttu-id="f5ba9-280">Si vous le souhaitez, générer la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-280">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="deploying-the-pipeline"></a><span data-ttu-id="f5ba9-281">Déploiement du Pipeline</span><span class="sxs-lookup"><span data-stu-id="f5ba9-281">Deploying the Pipeline</span></span>  
 <span data-ttu-id="f5ba9-282">Vous êtes maintenant prêt à créer et déployer les segments de complément dans la structure de répertoires du pipeline requis.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-282">You are now ready to build and deploy the add-in segments to the required pipeline directory structure.</span></span>  
  
#### <a name="to-deploy-the-segments-to-the-pipeline"></a><span data-ttu-id="f5ba9-283">Pour déployer les segments dans le pipeline</span><span class="sxs-lookup"><span data-stu-id="f5ba9-283">To deploy the segments to the pipeline</span></span>  
  
1.  <span data-ttu-id="f5ba9-284">Pour chaque projet dans la solution, utilisez le **Build** onglet de **propriétés du projet** (le **compiler** onglet dans Visual Basic) pour définir la valeur de la **chemin de sortie**  (le **chemin de sortie de génération** en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-284">For each project in the solution, use the **Build** tab of **Project Properties** (the **Compile** tab in Visual Basic) to set the value of the **Output path** (the **Build output path** in Visual Basic).</span></span> <span data-ttu-id="f5ba9-285">Si vous avez nommé votre dossier d’application `MyApp`, par exemple, vos projets seraient générés dans les dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="f5ba9-285">If you named your application folder `MyApp`, for example, your projects would build into the following folders:</span></span>  
  
    |<span data-ttu-id="f5ba9-286">Projet</span><span class="sxs-lookup"><span data-stu-id="f5ba9-286">Project</span></span>|<span data-ttu-id="f5ba9-287">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f5ba9-287">Path</span></span>|  
    |-------------|----------|  
    |<span data-ttu-id="f5ba9-288">AddInCalcV1</span><span class="sxs-lookup"><span data-stu-id="f5ba9-288">AddInCalcV1</span></span>|<span data-ttu-id="f5ba9-289">MyApp\Pipeline\AddIns\CalcV1</span><span class="sxs-lookup"><span data-stu-id="f5ba9-289">MyApp\Pipeline\AddIns\CalcV1</span></span>|  
    |<span data-ttu-id="f5ba9-290">Calc1AddInSideAdapter</span><span class="sxs-lookup"><span data-stu-id="f5ba9-290">Calc1AddInSideAdapter</span></span>|<span data-ttu-id="f5ba9-291">MyApp\Pipeline\AddInSideAdapters</span><span class="sxs-lookup"><span data-stu-id="f5ba9-291">MyApp\Pipeline\AddInSideAdapters</span></span>|  
    |<span data-ttu-id="f5ba9-292">Calc1AddInView</span><span class="sxs-lookup"><span data-stu-id="f5ba9-292">Calc1AddInView</span></span>|<span data-ttu-id="f5ba9-293">MyApp\Pipeline\AddInViews</span><span class="sxs-lookup"><span data-stu-id="f5ba9-293">MyApp\Pipeline\AddInViews</span></span>|  
    |<span data-ttu-id="f5ba9-294">Calc1Contract</span><span class="sxs-lookup"><span data-stu-id="f5ba9-294">Calc1Contract</span></span>|<span data-ttu-id="f5ba9-295">MyApp\Pipeline\Contracts</span><span class="sxs-lookup"><span data-stu-id="f5ba9-295">MyApp\Pipeline\Contracts</span></span>|  
    |<span data-ttu-id="f5ba9-296">Calc1Host</span><span class="sxs-lookup"><span data-stu-id="f5ba9-296">Calc1Host</span></span>|<span data-ttu-id="f5ba9-297">MyApp</span><span class="sxs-lookup"><span data-stu-id="f5ba9-297">MyApp</span></span>|  
    |<span data-ttu-id="f5ba9-298">Calc1HostSideAdapter</span><span class="sxs-lookup"><span data-stu-id="f5ba9-298">Calc1HostSideAdapter</span></span>|<span data-ttu-id="f5ba9-299">MyApp\Pipeline\HostSideAdapters</span><span class="sxs-lookup"><span data-stu-id="f5ba9-299">MyApp\Pipeline\HostSideAdapters</span></span>|  
    |<span data-ttu-id="f5ba9-300">Calc1HVA</span><span class="sxs-lookup"><span data-stu-id="f5ba9-300">Calc1HVA</span></span>|<span data-ttu-id="f5ba9-301">MyApp</span><span class="sxs-lookup"><span data-stu-id="f5ba9-301">MyApp</span></span>|  
  
    > [!NOTE]
    >  <span data-ttu-id="f5ba9-302">Si vous avez décidé de placer votre structure de dossiers de pipeline dans un emplacement autre que votre dossier d’application, vous devez modifier les chemins d’accès indiquées dans le tableau en conséquence.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-302">If you decided to put your pipeline folder structure in a location other than your application folder, you must modify the paths shown in the table accordingly.</span></span> <span data-ttu-id="f5ba9-303">Consultez la section traitant des spécifications du répertoire de pipelines dans [spécifications du développement de pipelines](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-303">See the discussion of pipeline directory requirements in [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
2.  <span data-ttu-id="f5ba9-304">Générez la solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-304">Build the Visual Studio solution.</span></span>  
  
3.  <span data-ttu-id="f5ba9-305">Vérifiez les répertoires d’application et du pipeline pour vous assurer que les assemblys ont été copiés dans les répertoires appropriés et qu’aucune copie supplémentaire des assemblys ont été installés dans les dossiers incorrects.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-305">Check the application and pipeline directories to ensure that the assemblies were copied to the correct directories and that no extra copies of assemblies were installed in the wrong folders.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="f5ba9-306">Si vous n’avez pas modifié **copie locale** à **False** pour le `Calc1AddInView` projet référence dans le `AddInCalcV1` projet, problèmes du contexte du chargeur empêchera le complément qui se trouve.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-306">If you did not change **Copy Local** to **False** for the `Calc1AddInView` project reference in the `AddInCalcV1` project, loader context problems will prevent the add-in from being located.</span></span>  
  
     <span data-ttu-id="f5ba9-307">Pour plus d’informations sur le déploiement vers le pipeline, consultez [spécifications du développement de pipelines](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span><span class="sxs-lookup"><span data-stu-id="f5ba9-307">For information about deploying to the pipeline, see [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
## <a name="running-the-host-application"></a><span data-ttu-id="f5ba9-308">Exécution de l’Application hôte</span><span class="sxs-lookup"><span data-stu-id="f5ba9-308">Running the Host Application</span></span>  
 <span data-ttu-id="f5ba9-309">Vous êtes maintenant prêt à exécuter l’hôte et d’interagir avec le complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-309">You are now ready to run the host and interact with the add-in.</span></span>  
  
#### <a name="to-run-the-host-application"></a><span data-ttu-id="f5ba9-310">Pour exécuter l’application hôte</span><span class="sxs-lookup"><span data-stu-id="f5ba9-310">To run the host application</span></span>  
  
1.  <span data-ttu-id="f5ba9-311">À l’invite de commandes, accédez au répertoire de l’application et exécutez l’application hôte, `Calc1Host.exe`.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-311">At the command prompt, go to the application directory and run the host application, `Calc1Host.exe`.</span></span>  
  
2.  <span data-ttu-id="f5ba9-312">L’hôte recherche tous les compléments disponibles de son type et vous invite à sélectionner un complément.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-312">The host finds all available add-ins of its type and prompts you to select an add-in.</span></span> <span data-ttu-id="f5ba9-313">Entrez **1** pour le complément disponible uniquement.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-313">Enter **1** for the only available add-in.</span></span>  
  
3.  <span data-ttu-id="f5ba9-314">Entrez une équation de la Calculatrice, telle que **2 + 2**.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-314">Enter an equation for the calculator, such as **2 + 2**.</span></span> <span data-ttu-id="f5ba9-315">Il doit y avoir des espaces entre les nombres et l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-315">There must be spaces between the numbers and the operator.</span></span>  
  
4.  <span data-ttu-id="f5ba9-316">Type **quitter** et appuyez sur la **entrée** touche pour fermer l’application.</span><span class="sxs-lookup"><span data-stu-id="f5ba9-316">Type **exit** and press the **Enter** key to close the application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5ba9-317">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5ba9-317">See Also</span></span>  
 [<span data-ttu-id="f5ba9-318">Procédure pas à pas : Activation de la compatibilité descendante lorsque votre hôte change</span><span class="sxs-lookup"><span data-stu-id="f5ba9-318">Walkthrough: Enabling Backward Compatibility as Your Host Changes</span></span>](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)  
 [<span data-ttu-id="f5ba9-319">Procédure pas à pas : Passage de Collections entre hôtes et compléments</span><span class="sxs-lookup"><span data-stu-id="f5ba9-319">Walkthrough: Passing Collections Between Hosts and Add-Ins</span></span>](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)  
 [<span data-ttu-id="f5ba9-320">Spécifications du développement de pipelines</span><span class="sxs-lookup"><span data-stu-id="f5ba9-320">Pipeline Development Requirements</span></span>](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)  
 [<span data-ttu-id="f5ba9-321">Contrats, vues et adaptateurs</span><span class="sxs-lookup"><span data-stu-id="f5ba9-321">Contracts, Views, and Adapters</span></span>](https://msdn.microsoft.com/library/a6460173-9507-4b87-8c07-d4ee245d715c)  
 [<span data-ttu-id="f5ba9-322">Développement de pipeline</span><span class="sxs-lookup"><span data-stu-id="f5ba9-322">Pipeline Development</span></span>](../../../docs/framework/add-ins/pipeline-development.md)
