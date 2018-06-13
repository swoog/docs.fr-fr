---
title: Génération d’une solution .NET Core complète sur Windows à l’aide de Visual Studio 2017
description: Découvrez comment générer une solution .NET Core complète dans Visual Studio 2017 sous Windows.
author: bleroy
ms.author: mairaw
ms.date: 11/16/2016
ms.openlocfilehash: 52b8781cdc29ac776123402c982353ef437ce74f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33214391"
---
# <a name="building-a-complete-net-core-solution-on-windows-using-visual-studio-2017"></a><span data-ttu-id="0c3c6-103">Génération d’une solution .NET Core complète sur Windows à l’aide de Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="0c3c6-103">Building a complete .NET Core solution on Windows, using Visual Studio 2017</span></span>

<span data-ttu-id="0c3c6-104">Visual Studio 2017 fournit un environnement de développement complet pour le développement d’applications .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-104">Visual Studio 2017 provides a full-featured development environment for developing .NET Core applications.</span></span> <span data-ttu-id="0c3c6-105">Les procédures décrites dans ce document expliquent comment créer une solution .NET Core classique qui inclut des bibliothèques réutilisables, des tests et utilise des bibliothèques tierces.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-105">The procedures in this document describe the steps necessary to build a typical .NET Core solution that includes reusable libraries, testing, and using third-party libraries.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="0c3c6-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0c3c6-106">Prerequisites</span></span>

<span data-ttu-id="0c3c6-107">Suivez les instructions stipulées dans [notre page de prérequis](../windows-prerequisites.md) pour mettre à jour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-107">Follow the instructions on [our prerequisites page](../windows-prerequisites.md) to update your environment.</span></span>

## <a name="a-solution-using-only-net-core-projects"></a><span data-ttu-id="0c3c6-108">Une solution utilisant uniquement des projets .NET Core</span><span class="sxs-lookup"><span data-stu-id="0c3c6-108">A solution using only .NET Core projects</span></span>

### <a name="writing-the-library"></a><span data-ttu-id="0c3c6-109">Écriture de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c3c6-109">Writing the library</span></span>

1. <span data-ttu-id="0c3c6-110">Dans Visual Studio, sélectionnez **Fichier**, **Nouveau**, **Projet**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-110">In Visual Studio, choose **File**, **New**, **Project**.</span></span> <span data-ttu-id="0c3c6-111">Dans la boîte de dialogue **Nouveau projet**, développez le nœud **Visual C#**, choisissez le nœud **.NET Standard**, puis choisissez **Bibliothèque de classes (.NET Standard)**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-111">In the **New Project** dialog, expand the **Visual C#** node and choose the **.NET Standard** node, and then choose **Class Library (.NET Standard)**.</span></span> 

2. <span data-ttu-id="0c3c6-112">Nommez le projet « Library » et la solution « Golden ».</span><span class="sxs-lookup"><span data-stu-id="0c3c6-112">Name the project "Library" and the solution "Golden".</span></span> <span data-ttu-id="0c3c6-113">Laissez l’option **Créer le répertoire pour la solution** activée.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-113">Leave **Create directory for solution** checked.</span></span> <span data-ttu-id="0c3c6-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-114">Click **OK**.</span></span>

3. <span data-ttu-id="0c3c6-115">Dans l’Explorateur de solutions, ouvrez le menu contextuel du nœud **Dépendances**, puis choisissez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-115">In Solution Explorer, open the context menu for the **Dependencies** node and choose **Manage NuGet Packages**.</span></span>

4. <span data-ttu-id="0c3c6-116">Choisissez « nuget.org » comme **Source de package**, puis choisissez l’onglet **Parcourir**. Recherchez **Newtonsoft.Json**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-116">Choose "nuget.org" as the **Package source**, and choose the **Browse** tab. Browse for **Newtonsoft.Json**.</span></span> <span data-ttu-id="0c3c6-117">Cliquez sur **Installer** et acceptez le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-117">Click **Install**, and accept the license agreement.</span></span> <span data-ttu-id="0c3c6-118">Le package doit maintenant apparaître sous **Dependencies/NuGet** (Dépendances/NuGet) et être automatiquement restauré.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-118">The package should now appear under **Dependencies/NuGet** and be automatically restored.</span></span>

5. <span data-ttu-id="0c3c6-119">Renommer le fichier `Class1.cs` en `Thing.cs`.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-119">Rename the `Class1.cs` file to `Thing.cs`.</span></span> <span data-ttu-id="0c3c6-120">Acceptez le renommage de la classe.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-120">Accept the rename of the class.</span></span> <span data-ttu-id="0c3c6-121">Ajouter une méthode : `public int Get(int number) => Newtonsoft.Json.JsonConvert.DeserializeObject<int>($"{number}");`</span><span class="sxs-lookup"><span data-stu-id="0c3c6-121">Add a method: `public int Get(int number) => Newtonsoft.Json.JsonConvert.DeserializeObject<int>($"{number}");`</span></span>

7. <span data-ttu-id="0c3c6-122">Dans le menu **Générer** , choisissez **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-122">On the **Build** menu, choose **Build Solution**.</span></span>

   <span data-ttu-id="0c3c6-123">La solution doit se générer sans erreur.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-123">The solution should build without error.</span></span>

### <a name="writing-the-test-project"></a><span data-ttu-id="0c3c6-124">Écriture du projet de test</span><span class="sxs-lookup"><span data-stu-id="0c3c6-124">Writing the test project</span></span>

1. <span data-ttu-id="0c3c6-125">Dans l’Explorateur de solutions, ouvrez le menu contextuel du nœud **Solution** et sélectionnez **Ajouter**, **Nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-125">In Solution Explorer, open the context menu for the **Solution** node and choose **Add**, **New Project**.</span></span> <span data-ttu-id="0c3c6-126">Dans la boîte de dialogue **Nouveau projet**, sous **Visual C#**, choisissez **Projet de test unitaire (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-126">In the **New Project** dialog, under **Visual C# / .NET Core**, choose **Unit Test Project (.NET Core)**.</span></span> <span data-ttu-id="0c3c6-127">Nommez-le « TestLibrary » et cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-127">Name it "TestLibrary" and click OK.</span></span> 

2. <span data-ttu-id="0c3c6-128">Dans le projet **TestLibrary**, ouvrez le menu contextuel du nœud **Dépendances**, puis choisissez **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-128">In the **TestLibrary** project, open the context menu for the **Dependencies** node and choose **Add Reference**.</span></span> <span data-ttu-id="0c3c6-129">Cliquez sur **Projets**, puis enregistrez le projet de bibliothèque et cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-129">Click **Projects**, then check the Library project and click OK.</span></span> <span data-ttu-id="0c3c6-130">Cette opération ajoute une référence à votre bibliothèque à partir du projet de test.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-130">This adds a reference to your library from the test project.</span></span>

3. <span data-ttu-id="0c3c6-131">Renommez le fichier `UnitTest1.cs` en `LibraryTests.cs` et acceptez le changement de nom de classe.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-131">Rename the `UnitTest1.cs` file to `LibraryTests.cs` and accept the class rename.</span></span> <span data-ttu-id="0c3c6-132">Ajoutez `using Library;` au début du fichier et remplacez la méthode `TestMethod1` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="0c3c6-132">Add `using Library;` to the top of the file, and replace the `TestMethod1` method with the following code:</span></span>
    ```csharp
    [TestMethod]
    public void ThingGetsObjectValFromNumber()
    {
        Assert.AreEqual(42, new Thing().Get(42));
    }
    ```

   <span data-ttu-id="0c3c6-133">Vous devez maintenant être en mesure de générer la solution.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-133">You should now be able to build the solution.</span></span> 
   
4. <span data-ttu-id="0c3c6-134">Dans le menu **Test**, choisissez **Windows**, **Explorateur de tests** afin d’intégrer la fenêtre Explorateur de tests à votre espace de travail.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-134">On the **Test** menu, choose **Windows**, **Test Explorer** in order to get the test explorer window into your workspace.</span></span> <span data-ttu-id="0c3c6-135">Après quelques secondes, le test `ThingGetsObjectValFromNumber` doit s’afficher dans l’Explorateur de tests.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-135">After a few seconds, the `ThingGetsObjectValFromNumber` test should appear in the test explorer.</span></span> <span data-ttu-id="0c3c6-136">Choisissez **Exécuter tout**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-136">Choose **Run All**.</span></span>
   
   <span data-ttu-id="0c3c6-137">Le test doit réussir.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-137">The test should pass.</span></span>

### <a name="writing-the-console-app"></a><span data-ttu-id="0c3c6-138">Écriture de l’application console</span><span class="sxs-lookup"><span data-stu-id="0c3c6-138">Writing the console app</span></span>

1. <span data-ttu-id="0c3c6-139">Dans l’Explorateur de solutions, ouvrez le menu contextuel de la solution et ajoutez un nouveau projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-139">In Solution Explorer, open the context menu for the solution, and add a new **Console App (.NET Core)** project.</span></span> <span data-ttu-id="0c3c6-140">Nommez-le « Application ».</span><span class="sxs-lookup"><span data-stu-id="0c3c6-140">Name it "App".</span></span>

2. <span data-ttu-id="0c3c6-141">Dans le projet **App**, ouvrez le menu contextuel du nœud **Dépendances**, puis choisissez **Ajouter**, **Référence**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-141">In the **App** project, open the context menu for the **Dependencies** node and choose **Add**,  **Reference**.</span></span> 

3. <span data-ttu-id="0c3c6-142">Dans la boîte de dialogue **Gestionnaire de références**, cochez **Bibliothèque** sous le nœud **Projets**, **Solution**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-142">In the **Reference Manager** dialog, check **Library** under the **Projects**, **Solution** node, and then click **OK**</span></span>

6. <span data-ttu-id="0c3c6-143">Ouvrez le menu contextuel du nœud **App**, puis choisissez **Définir comme projet de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-143">Open the context menu for the **App** node and choose **Set as StartUp Project**.</span></span> <span data-ttu-id="0c3c6-144">Ainsi, il est possible d’appuyer sur F5 ou Ctrl+F5 pour démarrer l’application console.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-144">This ensures that hitting F5 or CTRL+F5 will start the console app.</span></span>

7. <span data-ttu-id="0c3c6-145">Ouvrez le fichier `Program.cs`, ajoutez une directive `using Library;` en haut du fichier, puis ajoutez `Console.WriteLine($"The answer is {new Thing().Get(42)}.");` à la méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-145">Open the `Program.cs` file, add a `using Library;` directive to the top of the file, and then add `Console.WriteLine($"The answer is {new Thing().Get(42)}.");` to the `Main` method.</span></span>

8. <span data-ttu-id="0c3c6-146">Définissez un point d’arrêt après la ligne que vous venez d’ajouter.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-146">Set a breakpoint after the line that you just added.</span></span>

9. <span data-ttu-id="0c3c6-147">Appuyez sur F5 pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-147">Press F5 to run the application..</span></span>

   <span data-ttu-id="0c3c6-148">L’application doit se générer sans erreur et atteindre le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0c3c6-148">The application should build without error, and should hit the breakpoint.</span></span> <span data-ttu-id="0c3c6-149">Vous pouvez également vérifier que la sortie de l’application est « The answer is 42. ».</span><span class="sxs-lookup"><span data-stu-id="0c3c6-149">You should also be able to check that the application output "The answer is 42.".</span></span>
