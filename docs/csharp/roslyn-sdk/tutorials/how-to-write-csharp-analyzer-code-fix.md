---
title: 'Tutoriel : Écrire votre premier analyseur et correctif de code'
description: Ce tutoriel fournit des instructions détaillées pour générer un analyseur et un correctif de code à l’aide du SDK .NET Compiler (API Roslyn).
ms.date: 08/01/2018
ms.custom: mvc
ms.openlocfilehash: 2959fe3008bfca972d3a164ed27d05c2a8b0e69a
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47397996"
---
# <a name="tutorial-write-your-first-analyzer-and-code-fix"></a><span data-ttu-id="9a619-103">Tutoriel : Écrire votre premier analyseur et correctif de code</span><span class="sxs-lookup"><span data-stu-id="9a619-103">Tutorial: Write your first analyzer and code fix</span></span>

<span data-ttu-id="9a619-104">Le SDK .NET Compiler Platform fournit les outils nécessaires pour créer des avertissements personnalisés qui ciblent C# ou le code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9a619-104">The .NET Compiler Platform SDK provides the tools you need to create custom warnings that target C# or Visual Basic code.</span></span> <span data-ttu-id="9a619-105">Votre **analyseur** contient le code qui reconnaît les violations de votre règle.</span><span class="sxs-lookup"><span data-stu-id="9a619-105">Your **analyzer** contains code that recognizes violations of your rule.</span></span> <span data-ttu-id="9a619-106">Votre **correctif de code** contient le code qui résout la violation.</span><span class="sxs-lookup"><span data-stu-id="9a619-106">Your **code fix** contains the code that fixes the violation.</span></span> <span data-ttu-id="9a619-107">Les règles que vous implémentez peuvent aller de la structure du code au style de codage et aux conventions d’affectation de noms, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="9a619-107">The rules you implement can be anything from code structure to coding style to naming conventions and more.</span></span> <span data-ttu-id="9a619-108">.NET Compiler Platform fournit le framework permettant d’exécuter l’analyse alors que les développeurs écrivent du code, et toutes les fonctionnalités de l’IU Visual Studio pour corriger le code : afficher des tildes dans l’éditeur, renseigner la liste d’erreurs Visual Studio, créer des suggestions « ampoule » et afficher un aperçu détaillé des corrections suggérées.</span><span class="sxs-lookup"><span data-stu-id="9a619-108">The .NET Compiler Platform provides the framework for running analysis as developers are writing code, and all the Visual Studio UI features for fixing code: showing squiggles in the editor, populating the Visual Studio Error List, creating the "light bulb" suggestions and showing the rich preview of the suggested fixes.</span></span>

<span data-ttu-id="9a619-109">Dans ce tutoriel, vous allez explorer la création d’un **analyseur** et d’un **correctif de code** associé à l’aide des API Roslyn.</span><span class="sxs-lookup"><span data-stu-id="9a619-109">In this tutorial, you'll explore the creation of an **analyzer** and an accompanying **code fix** using the Roslyn APIs.</span></span> <span data-ttu-id="9a619-110">Un analyseur consiste à effectuer une analyse du code source et signaler un problème à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a619-110">An analyzer is a way to perform source code analysis and report a problem to the user.</span></span> <span data-ttu-id="9a619-111">Un analyseur peut également fournir un correctif de code qui représente une modification du code source de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a619-111">Optionally, an analyzer can also provide a code fix that represents a modification to the user's source code.</span></span> <span data-ttu-id="9a619-112">Ce tutoriel crée un analyseur qui recherche des déclarations de variables locales qui pourraient être déclarées à l’aide du modificateur `const` mais qui ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="9a619-112">This tutorial creates an analyzer that finds local variable declarations that could be declared using the `const` modifier but are not.</span></span> <span data-ttu-id="9a619-113">Le correctif de code associé modifie ces déclarations pour ajouter le modificateur `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-113">The accompanying code fix modifies those declarations to add the `const` modifier.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9a619-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="9a619-114">Prerequisites</span></span>

* [<span data-ttu-id="9a619-115">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="9a619-115">Visual Studio 2017</span></span>](https://www.visualstudio.com/downloads)

<span data-ttu-id="9a619-116">Vous devez installer le SDK **.NET Compiler Platform** :</span><span class="sxs-lookup"><span data-stu-id="9a619-116">You'll need to install the **.NET Compiler Platform SDK**:</span></span>

[!INCLUDE[interactive-note](~/includes/roslyn-installation.md)]

<span data-ttu-id="9a619-117">Il existe plusieurs étapes pour créer et valider votre analyseur :</span><span class="sxs-lookup"><span data-stu-id="9a619-117">There are several steps to creating and validating your analyzer:</span></span>

1. <span data-ttu-id="9a619-118">Créez la solution.</span><span class="sxs-lookup"><span data-stu-id="9a619-118">Create the solution.</span></span>
1. <span data-ttu-id="9a619-119">Enregistrez le nom de l’analyseur et sa description.</span><span class="sxs-lookup"><span data-stu-id="9a619-119">Register the analyzer name and description.</span></span>
1. <span data-ttu-id="9a619-120">Créez un rapport sur les avertissements et les recommandations de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-120">Report analyzer warnings and recommendations.</span></span>
1. <span data-ttu-id="9a619-121">Implémentez le correctif de code pour accepter les recommandations.</span><span class="sxs-lookup"><span data-stu-id="9a619-121">Implement the code fix to accept recommendations.</span></span>
1. <span data-ttu-id="9a619-122">Améliorez l’analyse par le biais de tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="9a619-122">Improve the analysis through unit tests.</span></span>

## <a name="explore-the-analyzer-template"></a><span data-ttu-id="9a619-123">Explorer le modèle d’analyseur</span><span class="sxs-lookup"><span data-stu-id="9a619-123">Explore the analyzer template</span></span>

<span data-ttu-id="9a619-124">Votre analyseur signale à l’utilisateur les déclarations de variables locales qui peuvent être converties en constantes locales.</span><span class="sxs-lookup"><span data-stu-id="9a619-124">Your analyzer reports to the user any local variable declarations that can be converted to local constants.</span></span> <span data-ttu-id="9a619-125">Considérons par exemple le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-125">For example, consider the following code:</span></span>

```csharp
int x = 0;
Console.WriteLine(x);
```

<span data-ttu-id="9a619-126">Dans le code ci-dessus, une valeur constante est attribuée à `x` et n’est jamais modifiée.</span><span class="sxs-lookup"><span data-stu-id="9a619-126">In the code above, `x` is assigned a constant value and is never modified.</span></span> <span data-ttu-id="9a619-127">Elle peut être déclarée à l’aide du modificateur `const` :</span><span class="sxs-lookup"><span data-stu-id="9a619-127">It can be declared using the `const` modifier:</span></span>

```csharp
const int x = 0;
Console.WriteLine(x);
```

<span data-ttu-id="9a619-128">L’analyse pour déterminer si une variable peut être déclarée constante est impliquée, nécessitant une analyse syntaxique, une analyse constante de l’expression de l’initialiseur et une analyse du flux de données pour s’assurer que la variable n’est jamais accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="9a619-128">The analysis to determine whether a variable can be made constant is involved, requiring syntactic analysis, constant analysis of the initializer expression and dataflow analysis to ensure that the variable is never written to.</span></span> <span data-ttu-id="9a619-129">.NET Compiler Platform fournit les API qui simplifient l’exécution de cette analyse.</span><span class="sxs-lookup"><span data-stu-id="9a619-129">The .NET Compiler Platform provides APIs that make it easier to perform this analysis.</span></span> <span data-ttu-id="9a619-130">La première étape consiste à créer un nouveau projet C# **Analyseur avec correctif de code**.</span><span class="sxs-lookup"><span data-stu-id="9a619-130">The first step is to create a new C# **Analyzer with code fix** project.</span></span>

* <span data-ttu-id="9a619-131">Dans Visual Studio, choisissez **Fichier > Nouveau > Projet...** pour afficher la boîte de dialogue Nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="9a619-131">In Visual Studio, choose **File > New > Project...** to display the New Project dialog.</span></span>
* <span data-ttu-id="9a619-132">Sous **Visual C# > Extensibilité**, choisissez **Analyseur avec correctif de code (.NET Standard)**.</span><span class="sxs-lookup"><span data-stu-id="9a619-132">Under **Visual C# > Extensibility**, choose **Analyzer with code fix (.NET Standard)**.</span></span>
* <span data-ttu-id="9a619-133">Nommez votre projet « **MakeConst** », puis cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="9a619-133">Name your project "**MakeConst**" and click OK.</span></span>

<span data-ttu-id="9a619-134">Le modèle Analyseur avec correctif de code crée trois projets : un contient l’analyseur et le correctif de code, le second est un projet de test unitaire et le troisième est le projet VSIX.</span><span class="sxs-lookup"><span data-stu-id="9a619-134">The analyzer with code fix template creates three projects: one contains the analyzer and code fix, the second is a unit test project, and the third is the VSIX project.</span></span> <span data-ttu-id="9a619-135">Le projet de démarrage par défaut est le projet VSIX.</span><span class="sxs-lookup"><span data-stu-id="9a619-135">The default startup project is the VSIX project.</span></span> <span data-ttu-id="9a619-136">Appuyez sur **F5** pour démarrer le projet VSIX.</span><span class="sxs-lookup"><span data-stu-id="9a619-136">Press **F5** to start the VSIX project.</span></span> <span data-ttu-id="9a619-137">Ceci démarre une deuxième instance de Visual Studio qui a chargé votre nouvel analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-137">This starts a second instance of Visual Studio that has loaded your new analyzer.</span></span>

> [!TIP]
> <span data-ttu-id="9a619-138">Lorsque vous exécutez votre analyseur, vous démarrez une deuxième copie de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-138">When you run your analyzer, you start a second copy of Visual Studio.</span></span> <span data-ttu-id="9a619-139">Cette deuxième copie utilise un hive de Registre différent pour stocker les paramètres.</span><span class="sxs-lookup"><span data-stu-id="9a619-139">This second copy uses a different registry hive to store settings.</span></span> <span data-ttu-id="9a619-140">Cela vous permet de différencier les paramètres Visual dans les deux copies de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-140">That enables you to differentiate the visual settings in the two copies of Visual Studio.</span></span> <span data-ttu-id="9a619-141">Vous pouvez choisir un autre thème pour l’exécution expérimentale de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-141">You can pick a different theme for the experimental run of Visual Studio.</span></span> <span data-ttu-id="9a619-142">En outre, ne rendez pas vos paramètres itinérants et ne vous connectez pas à votre compte Visual Studio à l’aide de l’exécution expérimentale de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-142">In addition, don't roam your settings or login to your Visual Studio account using the experimental run of Visual Studio.</span></span> <span data-ttu-id="9a619-143">Cela permet de conserver les paramètres différents.</span><span class="sxs-lookup"><span data-stu-id="9a619-143">That keeps the settings different.</span></span>

<span data-ttu-id="9a619-144">Dans la deuxième instance de Visual Studio que vous venez de démarrer, créez un nouveau projet Application console C# (un projet .NET Core ou .NET Framework fonctionne -- les analyseurs travaillent au niveau source.) Placez le curseur sur le jeton souligné d’un trait ondulé et le texte d’avertissement fourni par un analyseur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9a619-144">In the second Visual Studio instance that you just started, create a new C# Console Application project (either .NET Core or .NET Framework project will work -- analyzers work at the source level.) Hover over the token with a wavy underline, and the warning text provided by an analyzer appears.</span></span>

<span data-ttu-id="9a619-145">Le modèle crée un analyseur qui émet un avertissement sur chaque déclaration de type dont le nom de type contient des lettres minuscules, comme indiqué dans la figure suivante :</span><span class="sxs-lookup"><span data-stu-id="9a619-145">The template creates an analyzer that reports a warning on each type declaration where the type name contains lowercase letters, as shown in the following figure:</span></span>

![Avertissement de l’analyseur](media/how-to-write-csharp-analyzer-code-fix/report-warning.png)

<span data-ttu-id="9a619-147">Le modèle fournit également un correctif de code qui modifie n’importe quel nom de type contenant des caractères minuscules en majuscules.</span><span class="sxs-lookup"><span data-stu-id="9a619-147">The template also provides a code fix that changes any type name containing lower case characters to all upper case.</span></span> <span data-ttu-id="9a619-148">Vous pouvez cliquer sur l’ampoule affichée avec l’avertissement pour voir les modifications suggérées.</span><span class="sxs-lookup"><span data-stu-id="9a619-148">You can click on the light bulb displayed with the warning to see the suggested changes.</span></span> <span data-ttu-id="9a619-149">Le fait d’accepter les modifications suggérées met à jour le nom de type et toutes les références à ce type dans la solution.</span><span class="sxs-lookup"><span data-stu-id="9a619-149">Accepting the suggested changes updates the type name and all references to that type in the solution.</span></span> <span data-ttu-id="9a619-150">Maintenant que vous avez vu l’analyseur initial en action, fermez la deuxième instance de Visual Studio et revenez à votre projet d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-150">Now that you've seen the initial analyzer in action, close the second Visual Studio instance and return to your analyzer project.</span></span>

<span data-ttu-id="9a619-151">Vous n’êtes pas obligé de démarrer une deuxième copie de Visual Studio et de créer un nouveau code pour tester chaque modification de votre analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-151">You don't have to start a second copy of Visual Studio and create new code to test every change in your analyzer.</span></span> <span data-ttu-id="9a619-152">Le modèle crée également un projet de test unitaire pour vous.</span><span class="sxs-lookup"><span data-stu-id="9a619-152">The template also creates a unit test project for you.</span></span> <span data-ttu-id="9a619-153">Ce projet contient deux tests.</span><span class="sxs-lookup"><span data-stu-id="9a619-153">That project contains two tests.</span></span> <span data-ttu-id="9a619-154">`TestMethod1` montre le format classique d’un test qui analyse le code sans déclencher un diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a619-154">`TestMethod1` shows the typical format of a test that analyzes code without triggering a diagnostic.</span></span> <span data-ttu-id="9a619-155">`TestMethod2` montre le format d’un test qui déclenche un diagnostic, puis applique un correctif de code proposé.</span><span class="sxs-lookup"><span data-stu-id="9a619-155">`TestMethod2` shows the format of a test that triggers a diagnostic, and then applies a suggested code fix.</span></span> <span data-ttu-id="9a619-156">À mesure que vous générez votre analyseur et votre correctif de code, vous écrirez des tests pour des structures de codes différentes afin de vérifier votre travail.</span><span class="sxs-lookup"><span data-stu-id="9a619-156">As you build your analyzer and code fix, you'll write tests for different code structures to verify your work.</span></span> <span data-ttu-id="9a619-157">Les tests unitaires pour les analyseurs sont beaucoup plus rapides que de les tester de manière interactive avec Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-157">Unit tests for analyzers are much quicker than testing them interactively with Visual Studio.</span></span>

> [!TIP]
> <span data-ttu-id="9a619-158">Les tests unitaires d’analyseur sont un excellent outil lorsque vous savez quelles constructions de code doivent et ne doivent pas déclencher votre analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-158">Analyzer unit tests are a great tool when you know what code constructs should and shouldn't trigger your analyzer.</span></span> <span data-ttu-id="9a619-159">Le chargement de votre analyseur dans une autre copie de Visual Studio est un excellent outil pour explorer et rechercher des constructions auxquelles vous n’avez peut-être pas encore pensé.</span><span class="sxs-lookup"><span data-stu-id="9a619-159">Loading your analyzer in another copy of Visual Studio is a great tool to explore and find constructs you may not have thought about yet.</span></span>

## <a name="create-analyzer-registrations"></a><span data-ttu-id="9a619-160">Créer des enregistrements d’analyseur</span><span class="sxs-lookup"><span data-stu-id="9a619-160">Create analyzer registrations</span></span>

<span data-ttu-id="9a619-161">Le modèle crée la classe `DiagnosticAnalyzer` initiale, dans le fichier **MakeConstAnalyzer.cs**.</span><span class="sxs-lookup"><span data-stu-id="9a619-161">The template creates the initial `DiagnosticAnalyzer` class, in the **MakeConstAnalyzer.cs** file.</span></span> <span data-ttu-id="9a619-162">Cet analyseur initial montre deux propriétés importantes de chaque analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-162">This initial analyzer shows two important properties of every analyzer.</span></span>

* <span data-ttu-id="9a619-163">Chaque analyseur de diagnostic doit fournir un attribut `[DiagnosticAnalyzer]` qui décrit le langage sur lequel il opère.</span><span class="sxs-lookup"><span data-stu-id="9a619-163">Every diagnostic analyzer must provide a `[DiagnosticAnalyzer]` attribute that describes the language it operates on.</span></span>
* <span data-ttu-id="9a619-164">Chaque analyseur de diagnostic doit dériver de la classe <xref:Microsoft.CodeAnalysis.Diagnostics.DiagnosticAnalyzer>.</span><span class="sxs-lookup"><span data-stu-id="9a619-164">Every diagnostic analyzer must derive from the <xref:Microsoft.CodeAnalysis.Diagnostics.DiagnosticAnalyzer> class.</span></span>

<span data-ttu-id="9a619-165">Le modèle montre également les fonctionnalités de base qui font partie de n’importe quel analyseur :</span><span class="sxs-lookup"><span data-stu-id="9a619-165">The template also shows the basic features that are part of any analyzer:</span></span>

1. <span data-ttu-id="9a619-166">Enregistrer les actions.</span><span class="sxs-lookup"><span data-stu-id="9a619-166">Register actions.</span></span> <span data-ttu-id="9a619-167">Les actions représentent les modifications de code qui doivent déclencher votre analyseur pour qu’il examine les violations dans le code.</span><span class="sxs-lookup"><span data-stu-id="9a619-167">The actions represent code changes that should trigger your analyzer to examine code for violations.</span></span> <span data-ttu-id="9a619-168">Lorsque Visual Studio détecte des modifications de code qui correspondent à une action enregistré, il appelle la méthode enregistrée de votre analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-168">When Visual Studio detects code edits that match a registered action, it calls your analyzer's registered method.</span></span>
1. <span data-ttu-id="9a619-169">Créer des diagnostics.</span><span class="sxs-lookup"><span data-stu-id="9a619-169">Create diagnostics.</span></span> <span data-ttu-id="9a619-170">Quand votre analyseur détecte une violation, il crée un objet de diagnostic que Visual Studio utilise pour informer l’utilisateur de la violation.</span><span class="sxs-lookup"><span data-stu-id="9a619-170">When your analyzer detects a violation, it creates a diagnostic object that Visual Studio uses to notify the user of the violation.</span></span>

<span data-ttu-id="9a619-171">Vous enregistrez des actions dans votre substitution de la méthode <xref:Microsoft.CodeAnalysis.Diagnostics.DiagnosticAnalyzer.Initialize(Microsoft.CodeAnalysis.Diagnostics.AnalysisContext)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9a619-171">You register actions in your override of <xref:Microsoft.CodeAnalysis.Diagnostics.DiagnosticAnalyzer.Initialize(Microsoft.CodeAnalysis.Diagnostics.AnalysisContext)?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="9a619-172">Dans ce tutoriel, vous allez consulter des **nœuds de syntaxe** pour rechercher des déclarations locales et voir lesquelles ont des valeurs constantes.</span><span class="sxs-lookup"><span data-stu-id="9a619-172">In this tutorial, you'll visit **syntax nodes** looking for local declarations, and see which of those have constant values.</span></span> <span data-ttu-id="9a619-173">Si une déclaration peut être une constante, votre analyseur crée et signale un diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a619-173">If a declaration could be constant, your analyzer will create and report a diagnostic.</span></span>

<span data-ttu-id="9a619-174">La première étape consiste à mettre à jour les constantes d’inscription et la méthode `Initialize` pour que ces constantes indiquent votre analyseur « Make Const ».</span><span class="sxs-lookup"><span data-stu-id="9a619-174">The first step is to update the registration constants and `Initialize` method so these constants indicate your "Make Const" analyzer.</span></span> <span data-ttu-id="9a619-175">La plupart des constantes de chaîne est définie dans le fichier de ressources de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a619-175">Most of the string constants are defined in the string resource file.</span></span> <span data-ttu-id="9a619-176">Cette pratique facilite la localisation.</span><span class="sxs-lookup"><span data-stu-id="9a619-176">You should follow that practice for easier localization.</span></span> <span data-ttu-id="9a619-177">Ouvrez le fichier **Resources.resx** pour le projet d’analyseur **MakeConst**.</span><span class="sxs-lookup"><span data-stu-id="9a619-177">Open the **Resources.resx** file for the **MakeConst** analyzer project.</span></span> <span data-ttu-id="9a619-178">Cela affiche l’éditeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="9a619-178">This displays the resource editor.</span></span> <span data-ttu-id="9a619-179">Mettez à jour les ressources de chaîne comme suit :</span><span class="sxs-lookup"><span data-stu-id="9a619-179">Update the string resources as follows:</span></span>

* <span data-ttu-id="9a619-180">Remplacez `AnalyzerTitle` par « Variable can be made constant » (La variable peut être rendue constante).</span><span class="sxs-lookup"><span data-stu-id="9a619-180">Change `AnalyzerTitle` to "Variable can be made constant".</span></span>
* <span data-ttu-id="9a619-181">Remplacez `AnalyzerMessageFormat` par « Can be made constant » (Peut être rendu constant).</span><span class="sxs-lookup"><span data-stu-id="9a619-181">Change `AnalyzerMessageFormat` to "Can be made constant".</span></span>
* <span data-ttu-id="9a619-182">Remplacez `AnalyzerDescription` par « Make constant » (Rendre constant).</span><span class="sxs-lookup"><span data-stu-id="9a619-182">Change `AnalyzerDescription` to "Make Constant".</span></span>

<span data-ttu-id="9a619-183">Modifiez aussi le menu déroulant **Modificateur d’accès** sur `public`.</span><span class="sxs-lookup"><span data-stu-id="9a619-183">Also, change the **Access Modifier** drop-down to `public`.</span></span> <span data-ttu-id="9a619-184">Ainsi, ces constantes sont plus faciles à utiliser dans les tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="9a619-184">That makes it easier to use these constants in unit tests.</span></span> <span data-ttu-id="9a619-185">Lorsque vous avez terminé, l’éditeur de ressources doit apparaître comme le montre l’illustration suivante :</span><span class="sxs-lookup"><span data-stu-id="9a619-185">When you have finished, the resource editor should appear as follow figure shows:</span></span>

![Mettre à jour les ressources de chaîne](media/how-to-write-csharp-analyzer-code-fix/update-string-resources.png)

<span data-ttu-id="9a619-187">Les modifications restantes ont lieu dans le fichier de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-187">The remaining changes are in the analyzer file.</span></span> <span data-ttu-id="9a619-188">Ouvrez **MakeConstAnalyzer.cs** dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-188">Open **MakeConstAnalyzer.cs** in Visual Studio.</span></span> <span data-ttu-id="9a619-189">Modifiez l’action enregistrée d’une action qui agit sur les symboles à une action qui agit sur la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="9a619-189">Change the registered action from one that acts on symbols to one that acts on syntax.</span></span> <span data-ttu-id="9a619-190">Dans la méthode `MakeConstAnalyzerAnalyzer.Initialize`, recherchez la ligne qui enregistre l’action sur les symboles :</span><span class="sxs-lookup"><span data-stu-id="9a619-190">In the `MakeConstAnalyzerAnalyzer.Initialize` method, find the line that registers the action on symbols:</span></span>

```csharp
context.RegisterSymbolAction(AnalyzeSymbol, SymbolKind.NamedType);
```

<span data-ttu-id="9a619-191">Remplacez-la par la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="9a619-191">Replace it with the following line:</span></span>

[!code-csharp[Register the node action](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstAnalyzer.cs#RegisterNodeAction "Register a node action")]

<span data-ttu-id="9a619-192">Après cette modification, vous pouvez supprimer la méthode `AnalyzeSymbol`.</span><span class="sxs-lookup"><span data-stu-id="9a619-192">After that change, you can delete the `AnalyzeSymbol` method.</span></span> <span data-ttu-id="9a619-193">Cet outil examine <xref:Microsoft.CodeAnalysis.CSharp.SyntaxKind.LocalDeclarationStatement?displayProperty=nameWithType>, et non les instructions <xref:Microsoft.CodeAnalysis.SymbolKind.NamedType?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9a619-193">This analyzer examines <xref:Microsoft.CodeAnalysis.CSharp.SyntaxKind.LocalDeclarationStatement?displayProperty=nameWithType>, not <xref:Microsoft.CodeAnalysis.SymbolKind.NamedType?displayProperty=nameWithType> statements.</span></span> <span data-ttu-id="9a619-194">Notez que `AnalyzeNode` est souligné par des traits ondulés rouges.</span><span class="sxs-lookup"><span data-stu-id="9a619-194">Notice that `AnalyzeNode` has red squiggles under it.</span></span> <span data-ttu-id="9a619-195">Le code que vous venez d’ajouter référence une méthode `AnalyzeNode` qui n’a pas été déclarée.</span><span class="sxs-lookup"><span data-stu-id="9a619-195">The code you just added references an `AnalyzeNode` method that hasn't been declared.</span></span> <span data-ttu-id="9a619-196">Déclarez cette méthode en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-196">Declare that method using the following code:</span></span>

```csharp
private void AnalyzeNode(SyntaxNodeAnalysisContext context)
{
}
```

<span data-ttu-id="9a619-197">Remplacez `Category` par « Usage » (Utilisation) dans **MakeConstAnalyzer.cs** comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-197">Change the `Category` to "Usage" in **MakeConstAnalyzer.cs** as shown in the following code:</span></span>

```csharp
private const string Category = "Usage";
```

## <a name="find-local-declarations-that-could-be-const"></a><span data-ttu-id="9a619-198">Rechercher des déclarations locales qui pourraient être constantes</span><span class="sxs-lookup"><span data-stu-id="9a619-198">Find local declarations that could be const</span></span>

<span data-ttu-id="9a619-199">Il est temps d’écrire la première version de la méthode `AnalyzeNode`.</span><span class="sxs-lookup"><span data-stu-id="9a619-199">It's time to write the first version of the `AnalyzeNode` method.</span></span> <span data-ttu-id="9a619-200">Elle doit rechercher une déclaration locale unique qui peut être `const` mais ne l’est pas, comme le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-200">It should look for a single local declaration that could be `const` but is not, like the following code:</span></span>

```csharp
int x = 0;
Console.WriteLine(x);
```

<span data-ttu-id="9a619-201">La première étape consiste à rechercher les déclarations locales.</span><span class="sxs-lookup"><span data-stu-id="9a619-201">The first step is to find local declarations.</span></span> <span data-ttu-id="9a619-202">Ajoutez le code suivant à `AnalyzeNode` dans **MakeConstAnalyzer.cs** :</span><span class="sxs-lookup"><span data-stu-id="9a619-202">Add the following code to `AnalyzeNode` in **MakeConstAnalyzer.cs**:</span></span>

```csharp
var localDeclaration = (LocalDeclarationStatementSyntax)context.Node;
```

<span data-ttu-id="9a619-203">Ce cast réussit toujours, car votre analyseur a enregistré les modifications apportées aux déclarations locales, et uniquement les déclarations locales.</span><span class="sxs-lookup"><span data-stu-id="9a619-203">This cast always succeeds because your analyzer registered for changes to local declarations, and only local declarations.</span></span> <span data-ttu-id="9a619-204">Aucun autre type de nœud ne déclenche un appel à votre méthode `AnalyzeNode`.</span><span class="sxs-lookup"><span data-stu-id="9a619-204">No other node type triggers a call to your `AnalyzeNode` method.</span></span> <span data-ttu-id="9a619-205">Ensuite, vérifiez la présence de modificateurs `const` dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="9a619-205">Next, check the declaration for any `const` modifiers.</span></span> <span data-ttu-id="9a619-206">Si vous en trouvez, retournez immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9a619-206">If you find them, return immediately.</span></span> <span data-ttu-id="9a619-207">Le code suivant recherche les modificateurs `const` sur la déclaration locale :</span><span class="sxs-lookup"><span data-stu-id="9a619-207">The following code looks for any `const` modifiers on the local declaration:</span></span>

```csharp
// make sure the declaration isn't already const:
if (localDeclaration.Modifiers.Any(SyntaxKind.ConstKeyword))
{
    return;
}
```

<span data-ttu-id="9a619-208">Enfin, vous devez vérifier que la variable peut être `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-208">Finally, you need to check that the variable could be `const`.</span></span> <span data-ttu-id="9a619-209">Cela signifie de s’assurer qu’elle n’est jamais assignée après son initialisation.</span><span class="sxs-lookup"><span data-stu-id="9a619-209">That means making sure it is never assigned after it is initialized.</span></span>

<span data-ttu-id="9a619-210">Vous allez effectuer une analyse sémantique à l’aide de <xref:Microsoft.CodeAnalysis.Diagnostics.SyntaxNodeAnalysisContext>.</span><span class="sxs-lookup"><span data-stu-id="9a619-210">You'll perform some semantic analysis using the <xref:Microsoft.CodeAnalysis.Diagnostics.SyntaxNodeAnalysisContext>.</span></span> <span data-ttu-id="9a619-211">Vous utilisez l’argument `context` pour déterminer si la déclaration de variable locale peut être rendue `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-211">You use the `context` argument to determine whether the local variable declaration can be made `const`.</span></span> <span data-ttu-id="9a619-212"><xref:Microsoft.CodeAnalysis.SemanticModel?displayProperty=nameWithType> représente toutes les informations sémantiques dans un fichier source unique.</span><span class="sxs-lookup"><span data-stu-id="9a619-212">A <xref:Microsoft.CodeAnalysis.SemanticModel?displayProperty=nameWithType> represents of all semantic information in a single source file.</span></span> <span data-ttu-id="9a619-213">Vous pouvez en apprendre plus dans l’article qui traite des [modèles sémantiques](../work-with-semantics.md).</span><span class="sxs-lookup"><span data-stu-id="9a619-213">You can learn more in the article that covers [semantic models](../work-with-semantics.md).</span></span> <span data-ttu-id="9a619-214">Vous allez utiliser <xref:Microsoft.CodeAnalysis.SemanticModel?displayProperty=nameWithType> pour effectuer une analyse de flux de données sur l’instruction de déclaration locale.</span><span class="sxs-lookup"><span data-stu-id="9a619-214">You'll use the <xref:Microsoft.CodeAnalysis.SemanticModel?displayProperty=nameWithType> to perform data flow analysis on the local declaration statement.</span></span> <span data-ttu-id="9a619-215">Ensuite, vous utilisez les résultats de cette analyse de flux de données pour vous assurer que la variable locale n’est pas écrite avec une nouvelle valeur ailleurs.</span><span class="sxs-lookup"><span data-stu-id="9a619-215">Then, you use the results of this data flow analysis to ensure that the local variable isn't written with a new value anywhere else.</span></span> <span data-ttu-id="9a619-216">Appelez la méthode d’extension <xref:Microsoft.CodeAnalysis.ModelExtensions.GetDeclaredSymbol%2A> pour récupérer <xref:Microsoft.CodeAnalysis.ILocalSymbol> pour la variable et vérifiez qu’il n’est pas contenu avec la collection <xref:Microsoft.CodeAnalysis.DataFlowAnalysis.WrittenOutside%2A?displayProperty=nameWithType> de l’analyse de flux de données.</span><span class="sxs-lookup"><span data-stu-id="9a619-216">Call the <xref:Microsoft.CodeAnalysis.ModelExtensions.GetDeclaredSymbol%2A> extension method to retrieve the <xref:Microsoft.CodeAnalysis.ILocalSymbol> for the variable and check that it isn't contained with the <xref:Microsoft.CodeAnalysis.DataFlowAnalysis.WrittenOutside%2A?displayProperty=nameWithType> collection of the data flow analysis.</span></span> <span data-ttu-id="9a619-217">Ajoutez le code suivant à la fin de la méthode `AnalyzeNode` :</span><span class="sxs-lookup"><span data-stu-id="9a619-217">Add the following code to the end of the `AnalyzeNode` method:</span></span>

```csharp
// Perform data flow analysis on the local declaration.
var dataFlowAnalysis = context.SemanticModel.AnalyzeDataFlow(localDeclaration);

// Retrieve the local symbol for each variable in the local declaration
// and ensure that it is not written outside of the data flow analysis region.
var variable = localDeclaration.Declaration.Variables.Single();
var variableSymbol = context.SemanticModel.GetDeclaredSymbol(variable);
if (dataFlowAnalysis.WrittenOutside.Contains(variableSymbol))
{
    return;
}
```

<span data-ttu-id="9a619-218">Le code qui vient d’être ajouté garantit que la variable n’est pas modifiée et peut par conséquent devenir `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-218">The code just added ensures that the variable isn't modified, and can therefore be made `const`.</span></span> <span data-ttu-id="9a619-219">Il est temps de générer le diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a619-219">It's time to raise the diagnostic.</span></span> <span data-ttu-id="9a619-220">Ajoutez le code suivant comme dernière ligne dans `AnalyzeNode` :</span><span class="sxs-lookup"><span data-stu-id="9a619-220">Add the following code as the last line in `AnalyzeNode`:</span></span>

```csharp
context.ReportDiagnostic(Diagnostic.Create(Rule, context.Node.GetLocation()));
```

<span data-ttu-id="9a619-221">Vous pouvez vérifier votre progression en appuyant sur **F5** pour exécuter votre analyseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-221">You can check your progress by pressing **F5** to run your analyzer.</span></span> <span data-ttu-id="9a619-222">Vous pouvez charger l’application console que vous avez créée précédemment et ajouter le code de test suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-222">You can load the console application you created earlier and then add the following test code:</span></span>

```csharp
int x = 0;
Console.WriteLine(x);
```

<span data-ttu-id="9a619-223">L’ampoule doit apparaître et votre analyseur doit signaler un diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a619-223">The light bulb should appear, and your analyzer should report a diagnostic.</span></span> <span data-ttu-id="9a619-224">Toutefois, l’ampoule utilise toujours le correctif de code généré par le modèle et vous indique qu’il peut être converti en majuscules.</span><span class="sxs-lookup"><span data-stu-id="9a619-224">However, the light bulb still uses the template generated code fix, and tells you it can be made upper case.</span></span> <span data-ttu-id="9a619-225">La section suivante explique comment écrire le correctif de code.</span><span class="sxs-lookup"><span data-stu-id="9a619-225">The next section explains how to write the code fix.</span></span>

## <a name="write-the-code-fix"></a><span data-ttu-id="9a619-226">Écrire le correctif de code</span><span class="sxs-lookup"><span data-stu-id="9a619-226">Write the code fix</span></span>

<span data-ttu-id="9a619-227">Un analyseur peut fournir un ou plusieurs correctifs de code.</span><span class="sxs-lookup"><span data-stu-id="9a619-227">An analyzer can provide one or more code fixes.</span></span> <span data-ttu-id="9a619-228">Un correctif de code définit une modification qui traite le problème signalé.</span><span class="sxs-lookup"><span data-stu-id="9a619-228">A code fix defines an edit that addresses the reported issue.</span></span> <span data-ttu-id="9a619-229">Pour l’analyseur que vous avez créé, vous pouvez fournir un correctif de code qui insère le mot clé const :</span><span class="sxs-lookup"><span data-stu-id="9a619-229">For the analyzer that you created, you can provide a code fix that inserts the const keyword:</span></span>

```csharp
const int x = 0;
Console.WriteLine(x);
```

<span data-ttu-id="9a619-230">L’utilisateur le choisit à partir de l’IU ampoule dans l’éditeur et Visual Studio modifie le code.</span><span class="sxs-lookup"><span data-stu-id="9a619-230">The user chooses it from the light bulb UI in the editor and Visual Studio changes the code.</span></span>

<span data-ttu-id="9a619-231">Ouvrez le fichier **MakeConstCodeFixProvider.cs** ajouté par le modèle.</span><span class="sxs-lookup"><span data-stu-id="9a619-231">Open the **MakeConstCodeFixProvider.cs** file added by the template.</span></span>  <span data-ttu-id="9a619-232">Ce correctif de code est déjà associé à l’ID de diagnostic produit par votre analyseur de diagnostic, mais il n’implémente pas encore la transformation de code adéquate.</span><span class="sxs-lookup"><span data-stu-id="9a619-232">This code fix is already wired up to the Diagnostic ID produced by your diagnostic analyzer, but it doesn't yet implement the right code transform.</span></span> <span data-ttu-id="9a619-233">Tout d’abord, vous devez supprimer une partie du code du modèle.</span><span class="sxs-lookup"><span data-stu-id="9a619-233">First you should remove some of the template code.</span></span> <span data-ttu-id="9a619-234">Remplacez la chaîne de titre par « Make constant » :</span><span class="sxs-lookup"><span data-stu-id="9a619-234">Change the title string to "Make constant":</span></span>

[!code-csharp[Update the CodeFix title](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#CodeFixTitle "Update the CodeFix title")]

<span data-ttu-id="9a619-235">Ensuite, supprimez la méthode `MakeUppercaseAsync`.</span><span class="sxs-lookup"><span data-stu-id="9a619-235">Next, delete the `MakeUppercaseAsync` method.</span></span> <span data-ttu-id="9a619-236">Elle n’est plus applicable.</span><span class="sxs-lookup"><span data-stu-id="9a619-236">It no longer applies.</span></span>

<span data-ttu-id="9a619-237">Tous les correctifs de code dérivent de <xref:Microsoft.CodeAnalysis.CodeFixes.CodeFixProvider>.</span><span class="sxs-lookup"><span data-stu-id="9a619-237">All code fixes derive from <xref:Microsoft.CodeAnalysis.CodeFixes.CodeFixProvider>.</span></span> <span data-ttu-id="9a619-238">Ils substituent tous <xref:Microsoft.CodeAnalysis.CodeFixes.CodeFixProvider.RegisterCodeFixesAsync(Microsoft.CodeAnalysis.CodeFixes.CodeFixContext)?displayProperty=nameWithType> pour signaler les correctifs de code disponibles.</span><span class="sxs-lookup"><span data-stu-id="9a619-238">They all override <xref:Microsoft.CodeAnalysis.CodeFixes.CodeFixProvider.RegisterCodeFixesAsync(Microsoft.CodeAnalysis.CodeFixes.CodeFixContext)?displayProperty=nameWithType> to report available code fixes.</span></span> <span data-ttu-id="9a619-239">Dans `RegisterCodeFixesAsync`, remplacez le type de nœud ancêtre que vous recherchez par <xref:Microsoft.CodeAnalysis.CSharp.Syntax.LocalDeclarationStatementSyntax> pour faire correspondre le diagnostic :</span><span class="sxs-lookup"><span data-stu-id="9a619-239">In `RegisterCodeFixesAsync`, change the ancestor node type you're searching for to a <xref:Microsoft.CodeAnalysis.CSharp.Syntax.LocalDeclarationStatementSyntax> to match the diagnostic:</span></span>

[!code-csharp[Find local declaration node](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#FindDeclarationNode  "Find the local declaration node that raised the diagnostic")]

<span data-ttu-id="9a619-240">Ensuite, modifiez la dernière ligne pour enregistrer un correctif de code.</span><span class="sxs-lookup"><span data-stu-id="9a619-240">Next, change the last line to register a code fix.</span></span> <span data-ttu-id="9a619-241">Votre correctif crée un nouveau document obtenu en ajoutant le modificateur `const` à une déclaration existante :</span><span class="sxs-lookup"><span data-stu-id="9a619-241">Your fix will create a new document that results from adding the `const` modifier to an existing declaration:</span></span>  

[!code-csharp[Register the new code fix](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#RegisterCodeFix  "Register the new code fix")]

<span data-ttu-id="9a619-242">Notez les traits de soulignement ondulés rouges dans le code que vous venez d’ajouter sur le symbole `MakeConstAsync`.</span><span class="sxs-lookup"><span data-stu-id="9a619-242">You'll notice red squiggles in the code you just added on the symbol `MakeConstAsync`.</span></span> <span data-ttu-id="9a619-243">Ajoutez une déclaration pour `MakeConstAsync` comme le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-243">Add a declaration for `MakeConstAsync` like the following code:</span></span>

```csharp
private async Task<Document> MakeConstAsync(Document document,
   LocalDeclarationStatementSyntax localDeclaration,
   CancellationToken cancellationToken)
{
}
```

<span data-ttu-id="9a619-244">Votre nouvelle méthode `MakeConstAsync` transformera <xref:Microsoft.CodeAnalysis.Document> qui représente le fichier source de l’utilisateur en un nouveau <xref:Microsoft.CodeAnalysis.Document> qui contient à présent une déclaration `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-244">Your new `MakeConstAsync` method will transform the <xref:Microsoft.CodeAnalysis.Document> representing the user's source file into a new <xref:Microsoft.CodeAnalysis.Document> that now contains a `const` declaration.</span></span>

<span data-ttu-id="9a619-245">Vous créez un nouveau jeton de mot clé `const` à insérer au début de l’instruction de déclaration.</span><span class="sxs-lookup"><span data-stu-id="9a619-245">You create a new `const` keyword token to insert at the front of the declaration statement.</span></span> <span data-ttu-id="9a619-246">Veillez tout d’abord à supprimer les trivia de début dans le premier jeton de l’instruction de déclaration et à les associer au jeton `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-246">Be careful to first remove any leading trivia from the first token of the declaration statement and attach it to the `const` token.</span></span> <span data-ttu-id="9a619-247">Ajoutez le code suivant à la méthode `MakeConstAsync` :</span><span class="sxs-lookup"><span data-stu-id="9a619-247">Add the following code to the `MakeConstAsync` method:</span></span>

[!code-csharp[Create a new const keyword token](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#CreateConstToken  "Create the new const keyword token")]

<span data-ttu-id="9a619-248">Ensuite, ajoutez le jeton `const` dans la déclaration à l’aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-248">Next, add the `const` token to the declaration using the following code:</span></span>

```csharp
// Insert the const token into the modifiers list, creating a new modifiers list.
var newModifiers = trimmedLocal.Modifiers.Insert(0, constToken);
// Produce the new local declaration.
var newLocal = trimmedLocal
    .WithModifiers(newModifiers)
    .WithDeclaration(localDeclaration.Declaration);
```

<span data-ttu-id="9a619-249">Ensuite, mettez en forme la nouvelle déclaration en fonction des règles de mise en forme en C#.</span><span class="sxs-lookup"><span data-stu-id="9a619-249">Next, format the new declaration to match C# formatting rules.</span></span> <span data-ttu-id="9a619-250">La mise en forme de vos modifications pour correspondre au code existant crée une meilleure expérience.</span><span class="sxs-lookup"><span data-stu-id="9a619-250">Formatting your changes to match existing code creates a better experience.</span></span> <span data-ttu-id="9a619-251">Ajoutez l’instruction suivante immédiatement après le code existant :</span><span class="sxs-lookup"><span data-stu-id="9a619-251">Add the following statement immediately after the existing code:</span></span>

[!code-csharp[Format the new declaration](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#FormatLocal  "Format the new declaration")]

<span data-ttu-id="9a619-252">Un nouvel espace de noms est requis pour ce code.</span><span class="sxs-lookup"><span data-stu-id="9a619-252">A new namespace is required for this code.</span></span> <span data-ttu-id="9a619-253">Ajoutez l’instruction `using` suivante en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="9a619-253">Add the following `using` statement to the top of the file:</span></span>

```csharp
using Microsoft.CodeAnalysis.Formatting;
```

<span data-ttu-id="9a619-254">L’étape finale consiste à apporter votre modification.</span><span class="sxs-lookup"><span data-stu-id="9a619-254">The final step is to make your edit.</span></span> <span data-ttu-id="9a619-255">Ce processus comprend trois étapes :</span><span class="sxs-lookup"><span data-stu-id="9a619-255">There are three steps to this process:</span></span>

1. <span data-ttu-id="9a619-256">Obtenir un handle pour le document existant.</span><span class="sxs-lookup"><span data-stu-id="9a619-256">Get a handle to the existing document.</span></span>
1. <span data-ttu-id="9a619-257">Créer un document en remplaçant la déclaration existante par la nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="9a619-257">Create a new document by replacing the existing declaration with the new declaration.</span></span>
1. <span data-ttu-id="9a619-258">Retourner le nouveau document.</span><span class="sxs-lookup"><span data-stu-id="9a619-258">Return the new document.</span></span>

<span data-ttu-id="9a619-259">Ajoutez le code suivant à la fin de la méthode `MakeConstAsync` :</span><span class="sxs-lookup"><span data-stu-id="9a619-259">Add the following code to the end of the `MakeConstAsync` method:</span></span>

[!code-csharp[replace the declaration](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#ReplaceDocument  "Generate a new document by replacing the declaration")]

<span data-ttu-id="9a619-260">Votre correctif de code est prêt à être testé.</span><span class="sxs-lookup"><span data-stu-id="9a619-260">Your code fix is ready to try.</span></span>  <span data-ttu-id="9a619-261">Appuyez sur F5 pour exécuter le projet d’analyseur dans une deuxième instance de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-261">Press F5 to run the analyzer project in a second instance of Visual Studio.</span></span> <span data-ttu-id="9a619-262">Dans la deuxième instance de Visual Studio, créez un projet Application console C# et ajoutez quelques déclarations de variables locales initialisées avec des valeurs constantes à la méthode Main.</span><span class="sxs-lookup"><span data-stu-id="9a619-262">In the second Visual Studio instance, create a new C# Console Application project and add a few local variable declarations initialized with constant values to the Main method.</span></span> <span data-ttu-id="9a619-263">Vous verrez que ces éléments sont signalés en tant qu’avertissements comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9a619-263">You'll see that they are reported as warnings as below.</span></span>

![Avertissements Can make const](media/how-to-write-csharp-analyzer-code-fix/make-const-warning.png)

<span data-ttu-id="9a619-265">Vous avez bien progressé.</span><span class="sxs-lookup"><span data-stu-id="9a619-265">You've made a lot of progress.</span></span> <span data-ttu-id="9a619-266">Des traits de soulignement ondulés s’affichent sous les déclarations qui peuvent devenir `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-266">There are squiggles under the declarations that can be made `const`.</span></span> <span data-ttu-id="9a619-267">Mais il reste encore du travail.</span><span class="sxs-lookup"><span data-stu-id="9a619-267">But there is still work to do.</span></span> <span data-ttu-id="9a619-268">Cela fonctionne si vous ajoutez `const` aux déclarations qui commencent par `i`, puis `j` et enfin `k`.</span><span class="sxs-lookup"><span data-stu-id="9a619-268">This works fine if you add `const` to the declarations starting with `i`, then `j` and finally `k`.</span></span> <span data-ttu-id="9a619-269">Mais, si vous ajoutez le modificateur `const` dans un ordre différent, en commençant par `k`, votre analyseur crée des erreurs : `k` ne peut pas être déclaré `const`, sauf si `i` et `j` sont tous deux déjà `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-269">But, if you add the `const` modifier i a different order, starting with `k`, your analyzer creates errors: `k` can't be declared `const`, unless `i` and `j` are both already `const`.</span></span> <span data-ttu-id="9a619-270">Vous devez effectuer d’autres analyses afin de vous assurer que vous gérez les différentes façons dont les variables peuvent être déclarées et initialisées.</span><span class="sxs-lookup"><span data-stu-id="9a619-270">You've got to do more analysis to ensure you handle the different ways variables can be declared and initialized.</span></span>

## <a name="build-data-driven-tests"></a><span data-ttu-id="9a619-271">Générer des tests pilotés par les données</span><span class="sxs-lookup"><span data-stu-id="9a619-271">Build data driven tests</span></span>

<span data-ttu-id="9a619-272">Votre analyseur et votre correctif de code travaillent sur un cas simple d’une déclaration unique qui peut être devenir constante.</span><span class="sxs-lookup"><span data-stu-id="9a619-272">Your analyzer and code fix work on a simple case of a single declaration that can be made const.</span></span> <span data-ttu-id="9a619-273">Il existe de nombreuses instructions de déclaration possibles où cette implémentation commet des erreurs.</span><span class="sxs-lookup"><span data-stu-id="9a619-273">There are numerous possible declaration statements where this implementation makes mistakes.</span></span> <span data-ttu-id="9a619-274">Vous allez traiter ces cas en travaillant avec la bibliothèque de tests unitaires écrite par le modèle.</span><span class="sxs-lookup"><span data-stu-id="9a619-274">You'll address these cases by working with the unit test library written by the template.</span></span> <span data-ttu-id="9a619-275">C’est beaucoup plus rapide que d’ouvrir plusieurs fois une deuxième copie de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a619-275">It's much faster than repeatedly opening a second copy of Visual Studio.</span></span>

<span data-ttu-id="9a619-276">Ouvrez le fichier **MakeConstUnitTests.cs** dans le projet de test unitaire.</span><span class="sxs-lookup"><span data-stu-id="9a619-276">Open the **MakeConstUnitTests.cs** file in the unit test project.</span></span> <span data-ttu-id="9a619-277">Le modèle a créé deux tests qui suivent les deux modèles courants pour un test unitaire d’analyseur et de correctif de code.</span><span class="sxs-lookup"><span data-stu-id="9a619-277">The template created two tests that follow the two common patterns for an analyzer and code fix unit test.</span></span> <span data-ttu-id="9a619-278">`TestMethod1` montre le modèle pour un test qui garantit que l’analyseur ne signale pas un diagnostic lorsqu’il ne le devrait pas.</span><span class="sxs-lookup"><span data-stu-id="9a619-278">`TestMethod1` shows the pattern for a test that ensures the analyzer doesn't report a diagnostic when it shouldn't.</span></span> <span data-ttu-id="9a619-279">`TestMethod2` montre le modèle pour créer un rapport de diagnostic et exécuter le correctif de code.</span><span class="sxs-lookup"><span data-stu-id="9a619-279">`TestMethod2` shows the pattern for reporting a diagnostic and running the code fix.</span></span>

<span data-ttu-id="9a619-280">Le code de presque chaque test pour votre analyseur suit un de ces deux modèles.</span><span class="sxs-lookup"><span data-stu-id="9a619-280">The code for almost every test for your analyzer follows one of these two patterns.</span></span> <span data-ttu-id="9a619-281">Pour la première étape, vous pouvez revoir ces tests en tant que tests pilotés par les données.</span><span class="sxs-lookup"><span data-stu-id="9a619-281">For the first step, you can rework these tests as data driven tests.</span></span> <span data-ttu-id="9a619-282">Ensuite, il sera facile de créer de nouveaux tests en ajoutant de nouvelles constantes de chaîne pour représenter les différentes entrées de test.</span><span class="sxs-lookup"><span data-stu-id="9a619-282">Then, it will be easy to create new tests by adding new string constants to represent different test inputs.</span></span>

<span data-ttu-id="9a619-283">Pour plus d’efficacité, la première étape consiste à refactoriser les deux tests en tests pilotés par des données.</span><span class="sxs-lookup"><span data-stu-id="9a619-283">For efficiency, the first step is to refactor the two tests into data driven tests.</span></span> <span data-ttu-id="9a619-284">Ensuite, il vous suffit de définir quelques constantes de chaîne pour chaque nouveau test.</span><span class="sxs-lookup"><span data-stu-id="9a619-284">Then, you only need to define a couple string constants for each new test.</span></span> <span data-ttu-id="9a619-285">Lors de la refactorisation, renommez les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="9a619-285">While your refactoring, rename both methods to better names.</span></span> <span data-ttu-id="9a619-286">Remplacez `TestMethod1` par ce test qui garantit qu’aucun diagnostic n’est déclenché :</span><span class="sxs-lookup"><span data-stu-id="9a619-286">Replace `TestMethod1` with this test that ensures no diagnostic is raised:</span></span>

```csharp
[DataTestMethod]
[DataRow("")]
public void WhenTestCodeIsValidNoDiagnosticIsTriggered(string testCode)
{
    VerifyCSharpDiagnostic(testCode);
}
```

<span data-ttu-id="9a619-287">Vous pouvez créer une nouvelle ligne de données pour ce test en définissant un fragment de code qui ne doit pas entraîner votre diagnostic à déclencher un avertissement.</span><span class="sxs-lookup"><span data-stu-id="9a619-287">You can create a new data row for this test by defining any code fragment that should not cause your diagnostic to trigger a warning.</span></span> <span data-ttu-id="9a619-288">Cette surcharge de passes `VerifyCSharpDiagnostic` lorsqu’il n’y a aucun diagnostic déclenché pour le fragment de code source.</span><span class="sxs-lookup"><span data-stu-id="9a619-288">This overload of `VerifyCSharpDiagnostic` passes when there are no diagnostics triggered for the source code fragment.</span></span>  

<span data-ttu-id="9a619-289">Ensuite, remplacez `TestMethod2` par ce test qui garantit qu’un diagnostic est déclenché et un correctif de code appliqué pour le fragment de code source :</span><span class="sxs-lookup"><span data-stu-id="9a619-289">Next, replace `TestMethod2` with this test that ensures a diagnostic is raised and a code fix applied for the source code fragment:</span></span>

```csharp
[DataTestMethod]
[DataRow(LocalIntCouldBeConstant, LocalIntCouldBeConstantFixed, 10, 13)]
public void WhenDiagosticIsRaisedFixUpdatesCode(
    string test,
    string fixTest,
    int line,
    int column)
{
    var expected = new DiagnosticResult
    {
        Id = MakeConstAnalyzer.DiagnosticId,
        Message = new LocalizableResourceString(nameof(MakeConst.Resources.AnalyzerMessageFormat), MakeConst.Resources.ResourceManager, typeof(MakeConst.Resources)).ToString(),
        Severity = DiagnosticSeverity.Warning,
        Locations =
            new[] {
                    new DiagnosticResultLocation("Test0.cs", line, column)
                }
    };

    VerifyCSharpDiagnostic(test, expected);

    VerifyCSharpFix(test, fixTest);
}
```

<span data-ttu-id="9a619-290">Le code précédent a apporté également quelques modifications au code qui génère le résultat de diagnostic attendu.</span><span class="sxs-lookup"><span data-stu-id="9a619-290">The preceding code also made a couple changes to the code that builds the expected diagnostic result.</span></span> <span data-ttu-id="9a619-291">Il utilise les constantes publiques enregistrées dans l’analyseur `MakeConst`.</span><span class="sxs-lookup"><span data-stu-id="9a619-291">It uses the public constants registered in the `MakeConst` analyzer.</span></span> <span data-ttu-id="9a619-292">En outre, il utilise deux constantes de chaîne pour la source d’entrée et corrigée.</span><span class="sxs-lookup"><span data-stu-id="9a619-292">In addition, it uses two string constants for the input and fixed source.</span></span> <span data-ttu-id="9a619-293">Ajoutez les constantes de chaîne suivantes à la classe `UnitTest` :</span><span class="sxs-lookup"><span data-stu-id="9a619-293">Add the following string constants to the `UnitTest` class:</span></span>

[!code-csharp[string constants for fix test](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#FirstFixTest "string constants for fix test")]

<span data-ttu-id="9a619-294">Exécutez ces deux tests pour vous assurer qu’ils réussissent.</span><span class="sxs-lookup"><span data-stu-id="9a619-294">Run these two tests to make sure they pass.</span></span> <span data-ttu-id="9a619-295">Dans Visual Studio, ouvrez **l’Explorateur de tests** en sélectionnant **Test** > **Windows** > **Explorateur de tests**.</span><span class="sxs-lookup"><span data-stu-id="9a619-295">In Visual Studio, open the **Test Explorer** by selecting **Test** > **Windows** > **Test Explorer**.</span></span>  <span data-ttu-id="9a619-296">Appuyez sur le lien **Exécuter tout**.</span><span class="sxs-lookup"><span data-stu-id="9a619-296">The press the **Run All** link.</span></span>

## <a name="create-tests-for-valid-declarations"></a><span data-ttu-id="9a619-297">Créer des tests pour les déclarations valides</span><span class="sxs-lookup"><span data-stu-id="9a619-297">Create tests for valid declarations</span></span>

<span data-ttu-id="9a619-298">En règle générale, les analyseurs doivent s’arrêter aussi rapidement que possible, en effectuant un minimum de travail.</span><span class="sxs-lookup"><span data-stu-id="9a619-298">As a general rule, analyzers should exit as quickly as possible, doing minimal work.</span></span> <span data-ttu-id="9a619-299">Visual Studio appelle les analyseurs enregistrés lorsque l’utilisateur modifie le code.</span><span class="sxs-lookup"><span data-stu-id="9a619-299">Visual Studio calls registered analyzers as the user edits code.</span></span> <span data-ttu-id="9a619-300">La réactivité est essentielle.</span><span class="sxs-lookup"><span data-stu-id="9a619-300">Responsiveness is a key requirement.</span></span> <span data-ttu-id="9a619-301">Il existe plusieurs cas de test pour le code qui ne doivent pas déclencher votre diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a619-301">There are several test cases for code that should not raise your diagnostic.</span></span> <span data-ttu-id="9a619-302">Votre analyseur a déjà géré l’un de ces tests, le cas où une variable est assignée après avoir été initialisée.</span><span class="sxs-lookup"><span data-stu-id="9a619-302">Your analyzer already handles one of those tests, the case where a variable is assigned after being initialized.</span></span> <span data-ttu-id="9a619-303">Ajoutez la constante de chaîne suivante à vos tests pour représenter ce cas :</span><span class="sxs-lookup"><span data-stu-id="9a619-303">Add the following string constant to your tests to represent that case:</span></span>

[!code-csharp[variable assigned](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#VariableAssigned "a variable that is assigned after being initialized won't raise the diagnostic")]

<span data-ttu-id="9a619-304">Ensuite, ajoutez une ligne de données pour ce test, comme indiqué dans l’extrait de code ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9a619-304">Then, add a data row for this test as shown in the snippet below:</span></span>

```csharp
[DataTestMethod]
[DataRow(""),
 DataRow(VariableAssigned)]
public void WhenTestCodeIsValidNoDiagnosticIsTriggered(string testCode)
```

<span data-ttu-id="9a619-305">Ce test réussit également.</span><span class="sxs-lookup"><span data-stu-id="9a619-305">This test passes as well.</span></span> <span data-ttu-id="9a619-306">Ensuite, ajoutez des constantes pour les conditions que vous n’avez pas encore gérées :</span><span class="sxs-lookup"><span data-stu-id="9a619-306">Next, add constants for conditions you haven't handled yet:</span></span>

* <span data-ttu-id="9a619-307">Déclarations qui sont déjà `const`, car elles sont déjà constantes :</span><span class="sxs-lookup"><span data-stu-id="9a619-307">Declarations that are already `const`, because they are already const:</span></span>

   [!code-csharp[already const declaration](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#AlreadyConst "a declaration that is already const should not raise the diagnostic")]

* <span data-ttu-id="9a619-308">Déclarations sans initialiseur, car il n’existe aucune valeur à utiliser :</span><span class="sxs-lookup"><span data-stu-id="9a619-308">Declarations that have no initializer, because there is no value to use:</span></span>

   [!code-csharp[declarations that have no initializer](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#NoInitializer "a declaration that has no initializer should not raise the diagnostic")]

* <span data-ttu-id="9a619-309">Déclarations où l’initialiseur n’est pas une constante, car elles ne peuvent pas être des constantes de compilation :</span><span class="sxs-lookup"><span data-stu-id="9a619-309">Declarations where the initializer is not a constant, because they can't be compile-time constants:</span></span>

   [!code-csharp[declarations where the initializer isn't const](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#InitializerNotConstant "a declaration where the initializer is not a compile-time constant should not raise the diagnostic")]

<span data-ttu-id="9a619-310">Cela peut être encore plus compliqué, car C# accepte que plusieurs déclarations forment une seule instruction.</span><span class="sxs-lookup"><span data-stu-id="9a619-310">It can be even more complicated because C# allows multiple declarations as one statement.</span></span> <span data-ttu-id="9a619-311">Prenez en compte la constante de chaîne de cas de test suivante :</span><span class="sxs-lookup"><span data-stu-id="9a619-311">Consider the following test case string constant:</span></span>

[!code-csharp[multiple initializers](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#MultipleInitializers "A declaration can be made constant only if all variables in that statement can be made constant")]

<span data-ttu-id="9a619-312">La variable `i` peut devenir constante, mais la variable `j` ne le peut pas.</span><span class="sxs-lookup"><span data-stu-id="9a619-312">The variable `i` can be made constant, but the variable `j` cannot.</span></span> <span data-ttu-id="9a619-313">Par conséquent, cette instruction ne peut pas devenir une déclaration constante.</span><span class="sxs-lookup"><span data-stu-id="9a619-313">Therefore, this statement cannot be made a const declaration.</span></span> <span data-ttu-id="9a619-314">Ajouter les déclarations `DataRow` pour tous ces tests :</span><span class="sxs-lookup"><span data-stu-id="9a619-314">Add the `DataRow` declarations for all these tests:</span></span>

```csharp
[DataTestMethod]
[DataRow(""),
    DataRow(VariableAssigned),
    DataRow(AlreadyConst),
    DataRow(NoInitializer),
    DataRow(InitializerNotConstant),
    DataRow(MultipleInitializers)]
public void WhenTestCodeIsValidNoDiagnosticIsTriggered(string testCode)
```

<span data-ttu-id="9a619-315">Réexécutez vos tests, et vous verrez ces nouveaux cas de test échouent.</span><span class="sxs-lookup"><span data-stu-id="9a619-315">Run your tests again, and you'll see these new test cases fail.</span></span>

## <a name="update-your-analyzer-to-ignore-correct-declarations"></a><span data-ttu-id="9a619-316">Mettre à jour votre analyseur afin d’ignorer les déclarations correctes</span><span class="sxs-lookup"><span data-stu-id="9a619-316">Update your analyzer to ignore correct declarations</span></span>

<span data-ttu-id="9a619-317">Vous avez besoin de certaines améliorations dans la méthode `AnalyzeNode` de votre analyseur pour éliminer le code correspondant à ces conditions.</span><span class="sxs-lookup"><span data-stu-id="9a619-317">You need some enhancements to your analyzer's `AnalyzeNode` method to filter out code that matches these conditions.</span></span> <span data-ttu-id="9a619-318">Ce sont toutes des conditions associées, donc des modifications similaires résoudront toutes ces conditions.</span><span class="sxs-lookup"><span data-stu-id="9a619-318">They are all related conditions, so similar changes will fix all these conditions.</span></span> <span data-ttu-id="9a619-319">Dans `AnalyzeNode`, effectuez les changements suivants :</span><span class="sxs-lookup"><span data-stu-id="9a619-319">Make the following changes to `AnalyzeNode`:</span></span>

* <span data-ttu-id="9a619-320">Votre analyse sémantique a examiné une déclaration de variable unique.</span><span class="sxs-lookup"><span data-stu-id="9a619-320">Your semantic analysis examined a single variable declaration.</span></span> <span data-ttu-id="9a619-321">Ce code doit se trouver dans une boucle `foreach` qui examine toutes les variables déclarées dans la même instruction.</span><span class="sxs-lookup"><span data-stu-id="9a619-321">This code needs to be in a `foreach` loop that examines all the variables declared in the same statement.</span></span>
* <span data-ttu-id="9a619-322">Chaque variable déclarée doit avoir un initialiseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-322">Each declared variable needs to have an initializer.</span></span>
* <span data-ttu-id="9a619-323">L’initialiseur de chaque variable déclarée doit être une constante de compilation.</span><span class="sxs-lookup"><span data-stu-id="9a619-323">Each declared variable's initializer must be a compile-time constant.</span></span>

<span data-ttu-id="9a619-324">Dans votre méthode `AnalyzeNode`, remplacez l’analyse sémantique d’origine :</span><span class="sxs-lookup"><span data-stu-id="9a619-324">In your `AnalyzeNode` method, replace the original semantic analysis:</span></span>

```csharp
// Perform data flow analysis on the local declaration.
var dataFlowAnalysis = context.SemanticModel.AnalyzeDataFlow(localDeclaration);

// Retrieve the local symbol for each variable in the local declaration
// and ensure that it is not written outside of the data flow analysis region.
var variable = localDeclaration.Declaration.Variables.Single();
var variableSymbol = context.SemanticModel.GetDeclaredSymbol(variable);
if (dataFlowAnalysis.WrittenOutside.Contains(variableSymbol))
{
    return;
}
```

<span data-ttu-id="9a619-325">par l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-325">with the following code snippet:</span></span>

```csharp
// Ensure that all variables in the local declaration have initializers that
// are assigned with constant values.
foreach (var variable in localDeclaration.Declaration.Variables)
{
    var initializer = variable.Initializer;
    if (initializer == null)
    {
        return;
    }

    var constantValue = context.SemanticModel.GetConstantValue(initializer.Value);
    if (!constantValue.HasValue)
    {
        return;
    }
}

// Perform data flow analysis on the local declaration.
var dataFlowAnalysis = context.SemanticModel.AnalyzeDataFlow(localDeclaration);

foreach (var variable in localDeclaration.Declaration.Variables)
{
    // Retrieve the local symbol for each variable in the local declaration
    // and ensure that it is not written outside of the data flow analysis region.
    var variableSymbol = context.SemanticModel.GetDeclaredSymbol(variable);
    if (dataFlowAnalysis.WrittenOutside.Contains(variableSymbol))
    {
        return;
    }
}
```

<span data-ttu-id="9a619-326">La première boucle `foreach` examine chaque déclaration de variable à l’aide de l’analyse syntaxique.</span><span class="sxs-lookup"><span data-stu-id="9a619-326">The first `foreach` loop examines each variable declaration using syntactic analysis.</span></span> <span data-ttu-id="9a619-327">La première vérification garantit que la variable a un initialiseur.</span><span class="sxs-lookup"><span data-stu-id="9a619-327">The first check guarantees that the variable has an initializer.</span></span> <span data-ttu-id="9a619-328">La deuxième vérification garantit que l’initialiseur est une constante.</span><span class="sxs-lookup"><span data-stu-id="9a619-328">The second check guarantees that the initializer is a constant.</span></span> <span data-ttu-id="9a619-329">La deuxième boucle contient l’analyse sémantique d’origine.</span><span class="sxs-lookup"><span data-stu-id="9a619-329">The second loop has the original semantic analysis.</span></span> <span data-ttu-id="9a619-330">Les vérifications sémantiques sont dans une boucle distincte, car elles ont un impact plus important sur les performances.</span><span class="sxs-lookup"><span data-stu-id="9a619-330">The semantic checks are in a separate loop because it has a greater impact on performance.</span></span> <span data-ttu-id="9a619-331">Réexécutez vos tests. Ils doivent tous réussir.</span><span class="sxs-lookup"><span data-stu-id="9a619-331">Run your tests again, and you should see them all pass.</span></span>

## <a name="add-the-final-polish"></a><span data-ttu-id="9a619-332">Ajouter la touche finale</span><span class="sxs-lookup"><span data-stu-id="9a619-332">Add the final polish</span></span>

<span data-ttu-id="9a619-333">Vous avez presque terminé.</span><span class="sxs-lookup"><span data-stu-id="9a619-333">You're almost done.</span></span> <span data-ttu-id="9a619-334">Il existe quelques conditions de plus que votre analyseur doit gérer.</span><span class="sxs-lookup"><span data-stu-id="9a619-334">There are a few more conditions for your analyzer to handle.</span></span> <span data-ttu-id="9a619-335">Visual Studio appelle les analyseurs lorsque l’utilisateur écrit du code.</span><span class="sxs-lookup"><span data-stu-id="9a619-335">Visual Studio calls analyzers while the user is writing code.</span></span> <span data-ttu-id="9a619-336">Souvent, votre analyseur sera appelé lorsque du code ne se compile pas.</span><span class="sxs-lookup"><span data-stu-id="9a619-336">It's often the case that your analyzer will be called for code that doesn't compile.</span></span> <span data-ttu-id="9a619-337">La méthode `AnalyzeNode` de votre analyseur de diagnostic ne vérifie pas si la valeur de constante est convertible en type de variable.</span><span class="sxs-lookup"><span data-stu-id="9a619-337">The diagnostic analyzer's `AnalyzeNode` method does not check to see if the constant value is convertible to the variable type.</span></span> <span data-ttu-id="9a619-338">Par conséquent, l’implémentation actuelle convertit sans problème une déclaration incorrecte comme int i = « abc » en une constante locale.</span><span class="sxs-lookup"><span data-stu-id="9a619-338">So, the current implementation will happily convert an incorrect declaration such as int i = "abc"' to a local constant.</span></span> <span data-ttu-id="9a619-339">Ajoutez une constante de chaîne source pour cette condition :</span><span class="sxs-lookup"><span data-stu-id="9a619-339">Add a source string constant for that condition:</span></span>

[!code-csharp[Mismatched types don't raise diagnostics](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#DeclarationIsInvalid "When the variable type and the constant type don't match, there's no diagnostic")]

<span data-ttu-id="9a619-340">En outre, les types de référence ne sont pas gérés correctement.</span><span class="sxs-lookup"><span data-stu-id="9a619-340">In addition, reference types are not handled properly.</span></span> <span data-ttu-id="9a619-341">La seule valeur de constante autorisée pour un type de référence est `null`, sauf dans le cas de <xref:System.String?displayPropert=nameWIthType>, qui autorise des littéraux de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a619-341">The only constant value allowed for a reference type is `null`, except in this case of <xref:System.String?displayPropert=nameWIthType>, which allows string literals.</span></span> <span data-ttu-id="9a619-342">En d’autres termes, `const string s = "abc"` est légal, mais pas `const object s = "abc"`.</span><span class="sxs-lookup"><span data-stu-id="9a619-342">In other words, `const string s = "abc"` is legal, but `const object s = "abc"` is not.</span></span> <span data-ttu-id="9a619-343">Cet extrait de code vérifie cette condition :</span><span class="sxs-lookup"><span data-stu-id="9a619-343">This code snippet verifies that condition:</span></span>

[!code-csharp[Reference types don't raise diagnostics](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#DeclarationIsntString "When the variable type is a reference type other than string, there's no diagnostic")]

<span data-ttu-id="9a619-344">Pour être exhaustif, vous devez ajouter un autre test afin de vous assurer que vous pouvez créer une déclaration de constante pour une chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a619-344">To be thorough, you need to add another test to make sure that you can create a constant declaration for a string.</span></span> <span data-ttu-id="9a619-345">L’extrait de code suivant définit le code qui déclenche le diagnostic et le code une fois que le correctif a été appliqué :</span><span class="sxs-lookup"><span data-stu-id="9a619-345">The following snippet defines both the code that raises the diagnostic, and the code after the fix has been applied:</span></span>

[!code-csharp[string reference types raise diagnostics](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#ConstantIsString "When the variable type is string, it can be constant")]

<span data-ttu-id="9a619-346">Enfin, si une variable est déclarée avec le mot clé `var`, le correctif de code fait la mauvaise chose et génère une déclaration `const var`, qui n’est pas prise en charge par le langage C#.</span><span class="sxs-lookup"><span data-stu-id="9a619-346">Finally, if a variable is declared with the `var` keyword, the code fix does the wrong thing and generates a `const var` declaration, which is not supported by the C# language.</span></span> <span data-ttu-id="9a619-347">Pour corriger ce bogue, le correctif de code doit remplacer le mot clé `var` par le nom du type déduit :</span><span class="sxs-lookup"><span data-stu-id="9a619-347">To fix this bug, the code fix must replace the `var` keyword with the inferred type's name:</span></span>

[!code-csharp[var references need to use the inferred types](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#VarDeclarations "Declarations made using var must have the type replaced with the inferred type")]

<span data-ttu-id="9a619-348">Ces modifications mettent à jour les déclarations de ligne de données pour les deux tests.</span><span class="sxs-lookup"><span data-stu-id="9a619-348">These changes update the data row declarations for both tests.</span></span> <span data-ttu-id="9a619-349">Le code suivant montre ces tests avec tous les attributs de ligne de données :</span><span class="sxs-lookup"><span data-stu-id="9a619-349">The following code shows these tests with all data row attributes:</span></span>

[!code-csharp[The finished tests](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst.Test/MakeConstUnitTests.cs#FinishedTests "The finished tests for the make const analyzer")]

<span data-ttu-id="9a619-350">Heureusement, tous les bogues ci-dessus peuvent être gérés à l’aide des mêmes techniques que celles que vous venez d’apprendre.</span><span class="sxs-lookup"><span data-stu-id="9a619-350">Fortunately, all of the above bugs can be addressed using the same techniques that you just learned.</span></span>

<span data-ttu-id="9a619-351">Pour corriger le premier bogue, commencez par ouvrir **DiagnosticAnalyzer.cs** et recherchez la boucle foreach où chacun des initialiseurs de la déclaration locale est vérifié pour s’assurer que des valeurs constantes leur sont attribués.</span><span class="sxs-lookup"><span data-stu-id="9a619-351">To fix the first bug, first open **DiagnosticAnalyzer.cs** and locate the foreach loop where each of the local declaration's initializers are checked to ensure that they're assigned with constant values.</span></span> <span data-ttu-id="9a619-352">Immédiatement _avant_ la première boucle foreach, appelez `context.SemanicModel.GetTypeInfo()` pour récupérer des informations détaillées sur le type déclaré de la déclaration locale :</span><span class="sxs-lookup"><span data-stu-id="9a619-352">Immediately _before_ the first foreach loop, call `context.SemanicModel.GetTypeInfo()` to retrieve detailed information about the declared type of the local declaration:</span></span>

```csharp
var variableTypeName = localDeclaration.Declaration.Type;
var variableType = context.SemanticModel.GetTypeInfo(variableTypeName).ConvertedType;
```

<span data-ttu-id="9a619-353">Ensuite, dans votre boucle `foreach`, vérifiez chaque initialiseur pour vous assurer qu’il peut être converti dans le type de variable.</span><span class="sxs-lookup"><span data-stu-id="9a619-353">Then, inside your `foreach` loop, check each initializer to make sure it's convertible to the variable type.</span></span> <span data-ttu-id="9a619-354">Ajoutez la vérification suivante après avoir vérifié que l’initialiseur est une constante :</span><span class="sxs-lookup"><span data-stu-id="9a619-354">Add the following check after ensuring that the initializer is a constant:</span></span>

```csharp
// Ensure that the initializer value can be converted to the type of the
// local declaration without a user-defined conversion.
var conversion = context.SemanticModel.ClassifyConversion(initializer.Value, variableType);
if (!conversion.Exists || conversion.IsUserDefined)
{
    return;
}
```

<span data-ttu-id="9a619-355">La modification suivante s’appuie sur la précédente.</span><span class="sxs-lookup"><span data-stu-id="9a619-355">The next change builds upon the last one.</span></span> <span data-ttu-id="9a619-356">Avant l’accolade fermante de la première boucle foreach, ajoutez le code suivant pour vérifier le type de la déclaration locale si la constante est une chaîne ou une valeur null.</span><span class="sxs-lookup"><span data-stu-id="9a619-356">Before the closing curly brace of the first foreach loop, add the following code to check the type of the local declaration when the constant is a string or null.</span></span>

```csharp
// Special cases:
//  * If the constant value is a string, the type of the local declaration
//    must be System.String.
//  * If the constant value is null, the type of the local declaration must
//    be a reference type.
if (constantValue.Value is string)
{
    if (variableType.SpecialType != SpecialType.System_String)
    {
        return;
    }
}
else if (variableType.IsReferenceType && constantValue.Value != null)
{
    return;
}
```

<span data-ttu-id="9a619-357">Vous devez écrire un peu plus de code dans votre fournisseur de correctif de code pour remplacer le mot clé var' par le nom de type correct.</span><span class="sxs-lookup"><span data-stu-id="9a619-357">You must write a bit more code in your code fix provider to replace the var' keyword with the correct type name.</span></span> <span data-ttu-id="9a619-358">Revenez dans **CodeFixProvider.cs**.</span><span class="sxs-lookup"><span data-stu-id="9a619-358">Return to **CodeFixProvider.cs**.</span></span> <span data-ttu-id="9a619-359">Le code que vous ajouterez effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a619-359">The code you'll add does the following steps:</span></span>

* <span data-ttu-id="9a619-360">Vérifiez si la déclaration est une déclaration `var`, et dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="9a619-360">Check if the declaration is a `var` declaration, and if it is:</span></span>
* <span data-ttu-id="9a619-361">Créez un nouveau type pour le type déduit.</span><span class="sxs-lookup"><span data-stu-id="9a619-361">Create a new type for the inferred type.</span></span>
* <span data-ttu-id="9a619-362">Assurez-vous que la déclaration de type n’est pas un alias.</span><span class="sxs-lookup"><span data-stu-id="9a619-362">Make sure the type declaration is not an alias.</span></span> <span data-ttu-id="9a619-363">Le cas échéant, il est permis de déclarer `const var`.</span><span class="sxs-lookup"><span data-stu-id="9a619-363">If so, it is legal to declare `const var`.</span></span>
* <span data-ttu-id="9a619-364">Assurez-vous que `var` n’est pas un nom de type dans ce programme.</span><span class="sxs-lookup"><span data-stu-id="9a619-364">Make sure that `var` isn't a type name in this program.</span></span> <span data-ttu-id="9a619-365">(Dans ce cas, `const var` est autorisé).</span><span class="sxs-lookup"><span data-stu-id="9a619-365">(If so, `const var` is legal).</span></span>
* <span data-ttu-id="9a619-366">Simplifier le nom de type complet</span><span class="sxs-lookup"><span data-stu-id="9a619-366">Simplify the full type name</span></span>

<span data-ttu-id="9a619-367">On dirait que beaucoup de code est nécessaire pour cela.</span><span class="sxs-lookup"><span data-stu-id="9a619-367">That sounds like a lot of code.</span></span> <span data-ttu-id="9a619-368">Ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="9a619-368">It's not.</span></span> <span data-ttu-id="9a619-369">Remplacez la ligne qui déclare et initialise `newLocal` par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="9a619-369">Replace the line that declares and initializes `newLocal` with the following code.</span></span> <span data-ttu-id="9a619-370">Il se place immédiatement après l’initialisation de `newModifiers` :</span><span class="sxs-lookup"><span data-stu-id="9a619-370">It goes immediately after the initialization of `newModifiers`:</span></span>

[!code-csharp[Replace Var designations](~/samples/csharp/roslyn-sdk/Tutorials/MakeConst/MakeConst/MakeConstCodeFixProvider.cs#ReplaceVar "Replace a var designation with the explicit type")]

<span data-ttu-id="9a619-371">Vous devez ajouter une instruction `using` pour utiliser le type <xref:Microsoft.CodeAnalysis.Simplification.Simplifier> :</span><span class="sxs-lookup"><span data-stu-id="9a619-371">You'll need to add one `using` statement to use the <xref:Microsoft.CodeAnalysis.Simplification.Simplifier> type:</span></span>

```csharp
using Microsoft.CodeAnalysis.Simplification;
```

<span data-ttu-id="9a619-372">Exécutez vos tests. Ils doivent tous réussir.</span><span class="sxs-lookup"><span data-stu-id="9a619-372">Run your tests, and they should all pass.</span></span> <span data-ttu-id="9a619-373">Félicitez-vous en exécutant votre analyseur terminé.</span><span class="sxs-lookup"><span data-stu-id="9a619-373">Congratulate yourself by running your finished analyzer.</span></span> <span data-ttu-id="9a619-374">Appuyez sur Ctrl+F5 pour exécuter le projet d’analyseur dans une deuxième instance de Visual Studio avec l’extension Préversion Roslyn chargée.</span><span class="sxs-lookup"><span data-stu-id="9a619-374">Press Ctrl+F5 to run the analyzer project in a second instance of Visual Studio with the Roslyn Preview extension loaded.</span></span>

* <span data-ttu-id="9a619-375">Dans la deuxième instance de Visual Studio, créez un projet Application console C# et ajoutez `int x = "abc";` à la méthode Main.</span><span class="sxs-lookup"><span data-stu-id="9a619-375">In the second Visual Studio instance, create a new C# Console Application project and add `int x = "abc";` to the Main method.</span></span> <span data-ttu-id="9a619-376">Grâce à la correction du premier bogue, aucun avertissement ne doit être signalé pour cette déclaration de variable locale (même s’il existe une erreur du compilateur comme prévu).</span><span class="sxs-lookup"><span data-stu-id="9a619-376">Thanks to the first bug fix, no warning should be reported for this local variable declaration (though there's a compiler error as expected).</span></span>
* <span data-ttu-id="9a619-377">Ensuite, ajoutez `object s = "abc";` à la méthode Main.</span><span class="sxs-lookup"><span data-stu-id="9a619-377">Next, add `object s = "abc";` to the Main method.</span></span> <span data-ttu-id="9a619-378">En raison de la correction du deuxième bogue, aucun avertissement ne doit être signalé.</span><span class="sxs-lookup"><span data-stu-id="9a619-378">Because of the second bug fix, no warning should be reported.</span></span>
* <span data-ttu-id="9a619-379">Enfin, ajoutez une autre variable locale qui utilise le mot clé `var`.</span><span class="sxs-lookup"><span data-stu-id="9a619-379">Finally, add another local variable that uses the `var` keyword.</span></span> <span data-ttu-id="9a619-380">Un avertissement est signalé et une suggestion apparaît en dessous à gauche.</span><span class="sxs-lookup"><span data-stu-id="9a619-380">You'll see that a warning is reported and a suggestion appears beneath to the left.</span></span>
* <span data-ttu-id="9a619-381">Déplacez le signe d’insertion de l’éditeur sur le trait de soulignement ondulé et appuyez sur Ctrl+.</span><span class="sxs-lookup"><span data-stu-id="9a619-381">Move the editor caret over the squiggly underline and press Ctrl+.</span></span> <span data-ttu-id="9a619-382">pour afficher le correctif de code suggéré.</span><span class="sxs-lookup"><span data-stu-id="9a619-382">to display the suggested code fix.</span></span> <span data-ttu-id="9a619-383">Lors de la sélection de votre correctif de code, notez que le mot clé ' var' est désormais géré correctement.</span><span class="sxs-lookup"><span data-stu-id="9a619-383">Upon selecting your code fix, note that the var' keyword is now handled correctly.</span></span>

<span data-ttu-id="9a619-384">Enfin, ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9a619-384">Finally, add the following code:</span></span>

```csharp
int i = 2;
int j = 32;
int k = i + j;
```

<span data-ttu-id="9a619-385">Après ces modifications, vous obtenez des traits de soulignement ondulés rouges uniquement sur les deux premières variables.</span><span class="sxs-lookup"><span data-stu-id="9a619-385">After these changes, you get red squiggles only on the first two variables.</span></span> <span data-ttu-id="9a619-386">Ajoutez `const` à `i` et à `j`, et vous obtenez un nouvel avertissement sur `k`, car cet élément peut désormais devenir `const`.</span><span class="sxs-lookup"><span data-stu-id="9a619-386">Add `const` to both `i` and `j`, and you get a new warning on `k` because it can now be `const`.</span></span>

<span data-ttu-id="9a619-387">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="9a619-387">Congratulations!</span></span> <span data-ttu-id="9a619-388">Vous avez créé votre première extension .NET Compiler Platform qui effectue une analyse de code à la volée pour détecter un problème et fournit une solution rapide pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="9a619-388">You've created your first .NET Compiler Platform extension that performs on-the-fly code analysis to detect an issue and provides a quick fix to correct it.</span></span> <span data-ttu-id="9a619-389">Tout au long du processus, vous avez découvert la plupart des API de code qui font partie du SDK .NET Compiler Platform (API Roslyn).</span><span class="sxs-lookup"><span data-stu-id="9a619-389">Along the way, you've learned many of the code APIs that are part of the .NET Compiler Platform SDK (Roslyn APIs).</span></span> <span data-ttu-id="9a619-390">Vous pouvez comparer votre travail avec [l’exemple terminé](https://github.com/dotnet/samples/tree/master/csharp/roslyn-sdk/Tutorials/MakeConst) dans notre référentiel GitHub d’exemples.</span><span class="sxs-lookup"><span data-stu-id="9a619-390">You can check your work against the [completed sample](https://github.com/dotnet/samples/tree/master/csharp/roslyn-sdk/Tutorials/MakeConst) in our samples GitHub repository.</span></span> <span data-ttu-id="9a619-391">Vous pouvez également télécharger le [fichier zip contenant le projet terminé](https://github.com/dotnet/samples/blob/master/csharp/roslyn-sdk/Tutorials/MakeConst.zip)</span><span class="sxs-lookup"><span data-stu-id="9a619-391">Or you can download [zip file of the completed project](https://github.com/dotnet/samples/blob/master/csharp/roslyn-sdk/Tutorials/MakeConst.zip)</span></span>

## <a name="other-resources"></a><span data-ttu-id="9a619-392">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="9a619-392">Other resources</span></span>

- [<span data-ttu-id="9a619-393">Bien démarrer avec l’analyse de la syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a619-393">Get started with syntax analysis</span></span>](../get-started/syntax-analysis.md)
- [<span data-ttu-id="9a619-394">Bien démarrer avec l’analyse sémantique</span><span class="sxs-lookup"><span data-stu-id="9a619-394">Get started with semantic analysis</span></span>](../get-started/semantic-analysis.md)