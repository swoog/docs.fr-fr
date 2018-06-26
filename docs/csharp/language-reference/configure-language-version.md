---
title: Sélectionner la version du langage C# - Guide C#
description: Configurer le compilateur pour effectuer la validation de la syntaxe à l’aide d’une version de compilateur spécifique
ms.date: 05/24/2018
ms.openlocfilehash: 9b91e62168ced0f373e1a55def8b279dc64833d8
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36207909"
---
# <a name="select-the-c-language-version"></a><span data-ttu-id="895c2-103">Sélectionner la version du langage C#</span><span class="sxs-lookup"><span data-stu-id="895c2-103">Select the C# language version</span></span>

<span data-ttu-id="895c2-104">Par défaut, le compilateur C# utilise la dernière version principale du langage.</span><span class="sxs-lookup"><span data-stu-id="895c2-104">The C# compiler defaults to the latest major version of the language that has been released.</span></span> <span data-ttu-id="895c2-105">Vous pouvez choisir de compiler n’importe quel projet à l’aide d’une nouvelle version intermédiaire du langage.</span><span class="sxs-lookup"><span data-stu-id="895c2-105">You may choose to compile any project using a new point release of the language.</span></span> <span data-ttu-id="895c2-106">En choisissant une version plus récente du langage, vous permettez à votre projet d’utiliser les dernières fonctionnalités de langage.</span><span class="sxs-lookup"><span data-stu-id="895c2-106">Choosing a newer version of the language enables your project to make use of the latest language features.</span></span> <span data-ttu-id="895c2-107">Dans d’autres scénarios, vous devrez peut-être vérifier qu’un projet est correctement compilé en cas d’utilisation d’une ancienne version de langage.</span><span class="sxs-lookup"><span data-stu-id="895c2-107">In other scenarios, you may need to validate that a project compiles cleanly when using an older version of the language.</span></span>

<span data-ttu-id="895c2-108">Cette fonctionnalité dissocie la décision d’installer de nouvelles versions du kit SDK et des outils dans votre environnement de développement de la décision d’incorporer de nouvelles fonctionnalités de langage dans un projet.</span><span class="sxs-lookup"><span data-stu-id="895c2-108">This capability decouples the decision to install new versions of the SDK and tools in your development environment from the decision to incorporate new language features in a project.</span></span> <span data-ttu-id="895c2-109">Vous pouvez installer la dernière version du SDK et des outils sur votre ordinateur de build.</span><span class="sxs-lookup"><span data-stu-id="895c2-109">You can install the latest SDK and tools on your build machine.</span></span> <span data-ttu-id="895c2-110">Chaque projet peut être configuré pour utiliser une version spécifique du langage pour sa build.</span><span class="sxs-lookup"><span data-stu-id="895c2-110">Each project can be configured to use a specific version of the language for its build.</span></span>

<span data-ttu-id="895c2-111">Il existe plusieurs façons de définir la version du langage :</span><span class="sxs-lookup"><span data-stu-id="895c2-111">There are several ways to set the language version:</span></span>

- <span data-ttu-id="895c2-112">Utilisez l’[action rapide Visual Studio](#visual-studio-quick-action).</span><span class="sxs-lookup"><span data-stu-id="895c2-112">Rely on a [Visual Studio quick action](#visual-studio-quick-action).</span></span>
- <span data-ttu-id="895c2-113">Définissez la version du langage dans l’[IU Visual Studio](#set-the-language-version-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="895c2-113">Set the language version in the [Visual Studio UI](#set-the-language-version-in-visual-studio).</span></span>
- <span data-ttu-id="895c2-114">Modifiez manuellement votre [fichier **.csproj**](#edit-the-csproj-file).</span><span class="sxs-lookup"><span data-stu-id="895c2-114">Manually edit your [**.csproj** file](#edit-the-csproj-file).</span></span>
- <span data-ttu-id="895c2-115">Définissez la version du langage [pour plusieurs projets d’un sous-répertoire](#configure-multiple-projects).</span><span class="sxs-lookup"><span data-stu-id="895c2-115">Set the language version [for multiple projects in a subdirectory](#configure-multiple-projects).</span></span>
- <span data-ttu-id="895c2-116">Configurez l’[option de compilateur `-langversion`](#set-the-langversion-compiler-option).</span><span class="sxs-lookup"><span data-stu-id="895c2-116">Configure the [`-langversion` compiler option](#set-the-langversion-compiler-option).</span></span>

## <a name="visual-studio-quick-action"></a><span data-ttu-id="895c2-117">Action rapide Visual Studio</span><span class="sxs-lookup"><span data-stu-id="895c2-117">Visual Studio quick action</span></span>

<span data-ttu-id="895c2-118">Visual Studio vous aide à déterminer la version de langage dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="895c2-118">Visual Studio helps you determine the language version you need.</span></span> <span data-ttu-id="895c2-119">Si vous utilisez une fonctionnalité de langage qui n’est pas disponible pour la version configurée, Visual Studio affiche un correctif potentiel pour mettre à jour la version de langage du projet.</span><span class="sxs-lookup"><span data-stu-id="895c2-119">If you use a language feature that is not available for the currently configured version, Visual Studio shows a potential fix to update the language version for the project.</span></span>

## <a name="set-the-language-version-in-visual-studio"></a><span data-ttu-id="895c2-120">Définir la version du langage dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="895c2-120">Set the language version in Visual Studio</span></span>

<span data-ttu-id="895c2-121">Vous pouvez définir la version dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="895c2-121">You can set the version in Visual Studio.</span></span> <span data-ttu-id="895c2-122">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le nœud de projet, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="895c2-122">Right-click on the project node in Solution Explorer and select **Properties**.</span></span> <span data-ttu-id="895c2-123">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="895c2-123">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="895c2-124">Dans la liste déroulante, sélectionnez la version.</span><span class="sxs-lookup"><span data-stu-id="895c2-124">In the dropdown, select the version.</span></span> <span data-ttu-id="895c2-125">L’image suivante montre le paramètre "latest" :</span><span class="sxs-lookup"><span data-stu-id="895c2-125">The following image shows the "latest" setting:</span></span>

![Capture d’écran des paramètres de build avancés où vous pouvez spécifier la version du langage](./media/configure-language-version/advanced-build-settings.png)

> [!NOTE]
> <span data-ttu-id="895c2-127">Si vous utilisez l’IDE Visual Studio pour mettre à jour vos fichiers csproj, il crée des nœuds distincts pour chaque configuration de build.</span><span class="sxs-lookup"><span data-stu-id="895c2-127">If you use the Visual Studio IDE to update your csproj files, the IDE creates separate nodes for each build configuration.</span></span> <span data-ttu-id="895c2-128">Vous définissez généralement la même valeur dans toutes les configurations de build, mais vous devez la définir explicitement pour chaque configuration de build ou sélectionner « Toutes les configurations » quand vous modifiez ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="895c2-128">You'll typically set the value the same in all build configurations, but you need to set it explicitly for each build configuration, or select "All Configurations" when you modify this setting.</span></span> <span data-ttu-id="895c2-129">Vous voyez alors ceci dans votre fichier csproj :</span><span class="sxs-lookup"><span data-stu-id="895c2-129">You'll see the following in your csproj file:</span></span>
>
>```xml
> <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
>  <LangVersion>latest</LangVersion>
></PropertyGroup>
>
> <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
>  <LangVersion>latest</LangVersion>
> </PropertyGroup>
> ```
>

## <a name="edit-the-csproj-file"></a><span data-ttu-id="895c2-130">Modifier le fichier csproj</span><span class="sxs-lookup"><span data-stu-id="895c2-130">Edit the csproj file</span></span>

<span data-ttu-id="895c2-131">Vous pouvez définir la version du langage dans votre fichier **.csproj**.</span><span class="sxs-lookup"><span data-stu-id="895c2-131">You can set the language version in your **.csproj** file.</span></span> <span data-ttu-id="895c2-132">Ajoutez un élément tel que celui-ci :</span><span class="sxs-lookup"><span data-stu-id="895c2-132">Add an element like the following:</span></span>

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="895c2-133">La valeur `latest` utilise la dernière version mineure du langage C#.</span><span class="sxs-lookup"><span data-stu-id="895c2-133">The value `latest` uses the latest minor version of the C# language.</span></span> <span data-ttu-id="895c2-134">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="895c2-134">Valid values are:</span></span>

|<span data-ttu-id="895c2-135">Value</span><span class="sxs-lookup"><span data-stu-id="895c2-135">Value</span></span>|<span data-ttu-id="895c2-136">Signification</span><span class="sxs-lookup"><span data-stu-id="895c2-136">Meaning</span></span>|
|------------|-------------|
|<span data-ttu-id="895c2-137">default</span><span class="sxs-lookup"><span data-stu-id="895c2-137">default</span></span>|<span data-ttu-id="895c2-138">Le compilateur accepte toute la syntaxe de langage valide de la dernière version principale qu’il peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="895c2-138">The compiler accepts all valid language syntax from the latest major version that it can support.</span></span>|
|<span data-ttu-id="895c2-139">ISO-1</span><span class="sxs-lookup"><span data-stu-id="895c2-139">ISO-1</span></span>|<span data-ttu-id="895c2-140">Le compilateur accepte uniquement la syntaxe incluse dans ISO/IEC 23270:2003 C# (1.0/1.2)</span><span class="sxs-lookup"><span data-stu-id="895c2-140">The compiler accepts only syntax that is included in ISO/IEC 23270:2003 C# (1.0/1.2)</span></span> |
|<span data-ttu-id="895c2-141">ISO-2</span><span class="sxs-lookup"><span data-stu-id="895c2-141">ISO-2</span></span>|<span data-ttu-id="895c2-142">Le compilateur accepte uniquement la syntaxe incluse dans ISO/IEC 23270:2006 C# (2.0)</span><span class="sxs-lookup"><span data-stu-id="895c2-142">The compiler accepts only syntax that is included in ISO/IEC 23270:2006 C# (2.0)</span></span> |
|<span data-ttu-id="895c2-143">3</span><span class="sxs-lookup"><span data-stu-id="895c2-143">3</span></span>|<span data-ttu-id="895c2-144">Le compilateur accepte uniquement la syntaxe incluse dans C# 3.0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-144">The compiler accepts only syntax that is included in C# 3.0 or lower.</span></span>|
|<span data-ttu-id="895c2-145">4</span><span class="sxs-lookup"><span data-stu-id="895c2-145">4</span></span>|<span data-ttu-id="895c2-146">Le compilateur accepte uniquement la syntaxe incluse dans C# 4.0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-146">The compiler accepts only syntax that is included in C# 4.0 or lower.</span></span>|
|<span data-ttu-id="895c2-147">5</span><span class="sxs-lookup"><span data-stu-id="895c2-147">5</span></span>|<span data-ttu-id="895c2-148">Le compilateur accepte uniquement la syntaxe incluse dans C# 5.0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-148">The compiler accepts only syntax that is included in C# 5.0 or lower.</span></span>|
|<span data-ttu-id="895c2-149">6</span><span class="sxs-lookup"><span data-stu-id="895c2-149">6</span></span>|<span data-ttu-id="895c2-150">Le compilateur accepte uniquement la syntaxe incluse dans C# 6.0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-150">The compiler accepts only syntax that is included in C# 6.0 or lower.</span></span>|
|<span data-ttu-id="895c2-151">7</span><span class="sxs-lookup"><span data-stu-id="895c2-151">7</span></span>|<span data-ttu-id="895c2-152">Le compilateur accepte uniquement la syntaxe incluse dans C# 7.0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-152">The compiler accepts only syntax that is included in C# 7.0 or lower.</span></span>|
|<span data-ttu-id="895c2-153">7.1</span><span class="sxs-lookup"><span data-stu-id="895c2-153">7.1</span></span>|<span data-ttu-id="895c2-154">Le compilateur accepte uniquement la syntaxe incluse dans C# 7.1 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-154">The compiler accepts only syntax that is included in C# 7.1 or lower.</span></span>|
|<span data-ttu-id="895c2-155">7.2</span><span class="sxs-lookup"><span data-stu-id="895c2-155">7.2</span></span>|<span data-ttu-id="895c2-156">Le compilateur accepte uniquement la syntaxe incluse dans C# 7.2 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-156">The compiler accepts only syntax that is included in C# 7.2 or lower.</span></span>|
|<span data-ttu-id="895c2-157">7.3</span><span class="sxs-lookup"><span data-stu-id="895c2-157">7.3</span></span>|<span data-ttu-id="895c2-158">Le compilateur accepte uniquement la syntaxe incluse dans C# 7.3 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="895c2-158">The compiler accepts only syntax that is included in C# 7.3 or lower.</span></span>|
|<span data-ttu-id="895c2-159">latest</span><span class="sxs-lookup"><span data-stu-id="895c2-159">latest</span></span>|<span data-ttu-id="895c2-160">Le compilateur accepte toute la syntaxe de langage valide qu’il peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="895c2-160">The compiler accepts all valid language syntax that it can support.</span></span>|

<span data-ttu-id="895c2-161">Les chaînes spéciales `default` et `latest` correspondent aux dernières versions de langage principale (C# 7.0) et mineure (C# 7.3) installées sur la machine de build.</span><span class="sxs-lookup"><span data-stu-id="895c2-161">The special strings `default` and `latest` resolve to the latest major (C# 7.0) and minor (C# 7.3) language versions installed on the build machine, respectively.</span></span>

## <a name="configure-multiple-projects"></a><span data-ttu-id="895c2-162">Configurer plusieurs projets</span><span class="sxs-lookup"><span data-stu-id="895c2-162">Configure multiple projects</span></span>

<span data-ttu-id="895c2-163">Vous pouvez créer un fichier **Directory.build.props** contenant l’élément `<LangVersion>` pour configurer plusieurs répertoires.</span><span class="sxs-lookup"><span data-stu-id="895c2-163">You can create a **Directory.build.props** file that contains the `<LangVersion>` element to configure multiple directories.</span></span> <span data-ttu-id="895c2-164">En règle générale, vous faites cela dans votre répertoire de solution.</span><span class="sxs-lookup"><span data-stu-id="895c2-164">You typically do that in your solution directory.</span></span> <span data-ttu-id="895c2-165">Ajoutez ce qui suit à un fichier **Directory.build.props** dans votre répertoire de solution :</span><span class="sxs-lookup"><span data-stu-id="895c2-165">Add the following to a **Directory.build.props** file in your solution directory:</span></span>

```xml
<Project>
 <PropertyGroup>
   <LangVersion>7.3</LangVersion>
 </PropertyGroup>
</Project>
```

<span data-ttu-id="895c2-166">Désormais, les builds de chaque sous-répertoire du répertoire contenant ce fichier vont utiliser la syntaxe C# version 7.3.</span><span class="sxs-lookup"><span data-stu-id="895c2-166">Now, builds in every subdirectory of the directory containing that file will use C# version 7.3 syntax.</span></span> <span data-ttu-id="895c2-167">Pour plus d’informations, consultez l’article sur [Personnaliser votre build](/visualstudio/msbuild/customize-your-build).</span><span class="sxs-lookup"><span data-stu-id="895c2-167">For more information, see the article on [Customize your build](/visualstudio/msbuild/customize-your-build).</span></span>

## <a name="set-the-langversion-compiler-option"></a><span data-ttu-id="895c2-168">Définir l’option de compilateur langversion</span><span class="sxs-lookup"><span data-stu-id="895c2-168">Set the langversion compiler option</span></span>

<span data-ttu-id="895c2-169">Vous pouvez utiliser l’option de ligne de commande `-langversion`.</span><span class="sxs-lookup"><span data-stu-id="895c2-169">You can use the `-langversion` command-line option.</span></span> <span data-ttu-id="895c2-170">Pour plus d’informations, consultez l’article sur l’option de compilateur [-langversion](../language-reference/compiler-options/langversion-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="895c2-170">For more information, see the article on the [-langversion](../language-reference/compiler-options/langversion-compiler-option.md) compiler option.</span></span> <span data-ttu-id="895c2-171">Vous pouvez voir une liste des valeurs valides en tapant `csc -langversion:?`.</span><span class="sxs-lookup"><span data-stu-id="895c2-171">You can see a list of the valid values by typing  `csc -langversion:?`.</span></span>
