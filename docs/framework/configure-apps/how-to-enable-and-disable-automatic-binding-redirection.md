---
title: 'Comment : activer et désactiver la redirection de liaison automatique'
ms.date: 09/12/2018
helpviewer_keywords:
- side-by-side execution, assembly binding redirection
- assemblies [.NET Framework], binding redirection
ms.assetid: 5fca42f3-bdce-4b81-a704-61e42c89d3ba
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: cf38bd753127e40c61512411c7aa2ebbbd7687db
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45746924"
---
# <a name="how-to-enable-and-disable-automatic-binding-redirection"></a><span data-ttu-id="49cb4-102">Comment : activer et désactiver la redirection de liaison automatique</span><span class="sxs-lookup"><span data-stu-id="49cb4-102">How to: Enable and Disable Automatic Binding Redirection</span></span>

<span data-ttu-id="49cb4-103">Lorsque vous compilez des applications dans Visual Studio qui ciblent le [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] et versions ultérieures, les redirections de liaison peuvent être automatiquement ajoutées au fichier de configuration d’application pour remplacer l’unification d’assembly.</span><span class="sxs-lookup"><span data-stu-id="49cb4-103">When you compile apps in Visual Studio that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] and later versions, binding redirects may be automatically added to the app configuration file to override assembly unification.</span></span> <span data-ttu-id="49cb4-104">Les redirections de liaison sont ajoutées si votre application ou ses composants font référence à plusieurs versions du même assembly, même si vous spécifiez manuellement des redirections de liaison dans le fichier de configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="49cb4-104">Binding redirects are added if your app or its components reference more than one version of the same assembly, even if you manually specify binding redirects in the configuration file for your app.</span></span> <span data-ttu-id="49cb4-105">La fonctionnalité de redirection de liaison automatique affecte les applications web et les applications de bureau traditionnelles qui ciblent le [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] ou une version ultérieure, bien que le comportement est légèrement différent pour une application web.</span><span class="sxs-lookup"><span data-stu-id="49cb4-105">The automatic binding redirection feature affects traditional desktop apps and web apps that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] or a later version, although the behavior is slightly different for a web app.</span></span> <span data-ttu-id="49cb4-106">Vous pouvez activer une redirection de liaison automatique si vos applications existantes ciblent des versions antérieures du .NET Framework, ou vous pouvez désactiver cette fonctionnalité si vous souhaitez conserver les redirections de liaison créées manuellement.</span><span class="sxs-lookup"><span data-stu-id="49cb4-106">You can enable automatic binding redirection if you have existing apps that target previous versions of the .NET Framework, or you can disable this feature if you want to keep manually authored binding redirects.</span></span>

## <a name="disable-automatic-binding-redirects-in-desktop-apps"></a><span data-ttu-id="49cb4-107">Désactiver les redirections de liaison automatiques dans les applications de bureau</span><span class="sxs-lookup"><span data-stu-id="49cb4-107">Disable automatic binding redirects in desktop apps</span></span>

<span data-ttu-id="49cb4-108">Les redirections de liaison automatiques sont activées par défaut pour les applications de bureau traditionnelles qui ciblent [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="49cb4-108">Automatic binding redirects are enabled by default for traditional desktop apps that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] and later versions.</span></span> <span data-ttu-id="49cb4-109">Les redirections de liaison sont ajoutées au fichier de configuration de sortie (app.config) lorsque l'application est compilée et remplace l'unification d'assemblys qui pourrait se produire, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="49cb4-109">The binding redirects are added to the output configuration (app.config) file when the app is compiled and overrides the assembly unification that might otherwise take place.</span></span> <span data-ttu-id="49cb4-110">Le fichier source app.config n'est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="49cb4-110">The source app.config file is not modified.</span></span> <span data-ttu-id="49cb4-111">Vous pouvez désactiver cette fonctionnalité en modifiant le fichier projet pour l’application.</span><span class="sxs-lookup"><span data-stu-id="49cb4-111">You can disable this feature by modifying the project file for the app.</span></span>

1. <span data-ttu-id="49cb4-112">Ouvrez le fichier de projet pour la modification à l’aide d’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="49cb4-112">Open the project file for editing using one of the following methods:</span></span>

   - <span data-ttu-id="49cb4-113">Dans Visual Studio, sélectionnez le projet dans **l’Explorateur de solutions**, puis choisissez **ouvrir le dossier dans l’Explorateur de fichiers** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="49cb4-113">In Visual Studio, select the project in **Solution Explorer**, and then choose **Open Folder in File Explorer** from the shortcut menu.</span></span> <span data-ttu-id="49cb4-114">Dans l’Explorateur de fichiers, recherchez le fichier de projet (.csproj ou .vbproj) et ouvrez-le dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="49cb4-114">In File Explorer, find the project (.csproj or .vbproj) file and open it in Notepad.</span></span>
   - <span data-ttu-id="49cb4-115">Dans Visual Studio, dans **l’Explorateur de solutions**, cliquez sur le projet et choisissez **décharger le projet**.</span><span class="sxs-lookup"><span data-stu-id="49cb4-115">In Visual Studio, in **Solution Explorer**, right-click the project and choose **Unload Project**.</span></span> <span data-ttu-id="49cb4-116">Cliquez de nouveau sur le projet déchargé, puis choisissez **modifier [NomProjet.csproj]**.</span><span class="sxs-lookup"><span data-stu-id="49cb4-116">Right-click the unloaded project again, and then choose **Edit [projectname.csproj]**.</span></span>

2. <span data-ttu-id="49cb4-117">Dans le fichier projet, recherchez l'entrée de propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="49cb4-117">In the project file, find the following property entry:</span></span>

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

3. <span data-ttu-id="49cb4-118">Remplacez `true` par `false` :</span><span class="sxs-lookup"><span data-stu-id="49cb4-118">Change `true` to `false`:</span></span>

   ```xml
   <AutoGenerateBindingRedirects>false</AutoGenerateBindingRedirects>
   ```

## <a name="enable-automatic-binding-redirects-manually"></a><span data-ttu-id="49cb4-119">Activer manuellement des redirections de liaison automatiques</span><span class="sxs-lookup"><span data-stu-id="49cb4-119">Enable automatic binding redirects manually</span></span>

<span data-ttu-id="49cb4-120">Vous pouvez activer les redirections de liaison automatiques dans les applications existantes qui ciblent des versions antérieures du .NET Framework, ou dans les cas où vous n’êtes pas automatiquement invité à ajouter une redirection.</span><span class="sxs-lookup"><span data-stu-id="49cb4-120">You can enable automatic binding redirects in existing apps that target older versions of the .NET Framework, or in cases where you're not automatically prompted to add a redirect.</span></span> <span data-ttu-id="49cb4-121">Si vous ciblez une version plus récente du framework mais ne pas automatiquement invité à ajouter une redirection, vous obtiendrez probablement un résultat de build qui suggère de que remapper les assemblys.</span><span class="sxs-lookup"><span data-stu-id="49cb4-121">If you're targeting a newer version of the framework but do not get automatically prompted to add a redirect, you'll likely get build output that suggests you remap assemblies.</span></span>

1. <span data-ttu-id="49cb4-122">Ouvrez le fichier de projet pour la modification à l’aide d’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="49cb4-122">Open the project file for editing using one of the following methods:</span></span>

   - <span data-ttu-id="49cb4-123">Dans Visual Studio, sélectionnez le projet dans **l’Explorateur de solutions**, puis choisissez **ouvrir le dossier dans l’Explorateur de fichiers** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="49cb4-123">In Visual Studio, select the project in **Solution Explorer**, and then choose **Open Folder in File Explorer** from the shortcut menu.</span></span> <span data-ttu-id="49cb4-124">Dans l’Explorateur de fichiers, recherchez le fichier de projet (.csproj ou .vbproj) et ouvrez-le dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="49cb4-124">In File Explorer, find the project (.csproj or .vbproj) file and open it in Notepad.</span></span>
   - <span data-ttu-id="49cb4-125">Dans Visual Studio, dans **l’Explorateur de solutions**, cliquez sur le projet et choisissez **décharger le projet**.</span><span class="sxs-lookup"><span data-stu-id="49cb4-125">In Visual Studio, in **Solution Explorer**, right-click the project and choose **Unload Project**.</span></span> <span data-ttu-id="49cb4-126">Cliquez de nouveau sur le projet déchargé, puis choisissez **modifier [NomProjet.csproj]**.</span><span class="sxs-lookup"><span data-stu-id="49cb4-126">Right-click the unloaded project again, and then choose **Edit [projectname.csproj]**.</span></span>

2. <span data-ttu-id="49cb4-127">Ajoutez l’élément suivant pour le premier groupe de propriétés de configuration (sous le \<PropertyGroup > balise) :</span><span class="sxs-lookup"><span data-stu-id="49cb4-127">Add the following element to the first configuration property group (under the \<PropertyGroup> tag):</span></span>

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

   <span data-ttu-id="49cb4-128">Voici un exemple de fichier de projet avec l’élément inséré :</span><span class="sxs-lookup"><span data-stu-id="49cb4-128">The following shows an example project file with the element inserted:</span></span>

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <Project ToolsVersion="12.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <Import Project="$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props" Condition="Exists('$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props')" />
       <PropertyGroup>
         <Configuration Condition=" '$(Configuration)' == ''     ">Debug</Configuration>
         <Platform Condition=" '$(Platform)' == '' ">AnyCPU</Platform>
         <ProjectGuid>{123334}</ProjectGuid>
         ...
         <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
       </PropertyGroup>
     ...
   </Project>
   ```

3. <span data-ttu-id="49cb4-129">Compilez votre application.</span><span class="sxs-lookup"><span data-stu-id="49cb4-129">Compile your app.</span></span>

## <a name="enable-automatic-binding-redirects-in-web-apps"></a><span data-ttu-id="49cb4-130">Activer les redirections de liaison automatiques dans les applications web</span><span class="sxs-lookup"><span data-stu-id="49cb4-130">Enable automatic binding redirects in web apps</span></span>

<span data-ttu-id="49cb4-131">Les redirections de liaison automatiques sont implémentées différemment pour les applications web.</span><span class="sxs-lookup"><span data-stu-id="49cb4-131">Automatic binding redirects are implemented differently for web apps.</span></span> <span data-ttu-id="49cb4-132">Comme le fichier de configuration source (web.config) doit être modifié pour les applications web, les redirections de liaison ne sont pas automatiquement ajoutées au fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="49cb4-132">Because the source configuration (web.config) file must be modified for web apps, binding redirects are not automatically added to the configuration file.</span></span> <span data-ttu-id="49cb4-133">Toutefois, Visual Studio vous informe des éventuels conflits de liaison et vous pouvez ajouter des redirections de liaison pour résoudre ces conflits.</span><span class="sxs-lookup"><span data-stu-id="49cb4-133">However, Visual Studio notifies you of binding conflicts, and you can add binding redirects to resolve the conflicts.</span></span> <span data-ttu-id="49cb4-134">Étant donné que vous êtes toujours invité à ajouter des redirections de liaison, vous n’avez pas besoin de désactiver explicitement cette fonctionnalité pour une application web.</span><span class="sxs-lookup"><span data-stu-id="49cb4-134">Because you're always prompted to add binding redirects, you don't need to explicitly disable this feature for a web app.</span></span>

<span data-ttu-id="49cb4-135">Pour ajouter des redirections de liaison à un fichier web.config :</span><span class="sxs-lookup"><span data-stu-id="49cb4-135">To add binding redirects to a web.config file:</span></span>

1. <span data-ttu-id="49cb4-136">Dans Visual Studio, compilez l'application et vérifiez les avertissements sur la génération.</span><span class="sxs-lookup"><span data-stu-id="49cb4-136">In Visual Studio, compile the app, and check for build warnings.</span></span>

   <span data-ttu-id="49cb4-137">![Générer l’avertissement pour les conflits de référence d’assembly](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")</span><span class="sxs-lookup"><span data-stu-id="49cb4-137">![Build warning for assembly reference conflicts](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")</span></span>

2. <span data-ttu-id="49cb4-138">En cas de conflit de liaison d’assembly, un avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="49cb4-138">If there are assembly binding conflicts, a warning appears.</span></span> <span data-ttu-id="49cb4-139">Double-cliquez sur l’avertissement, ou sélectionnez l’avertissement et appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="49cb4-139">Double-click the warning, or select the warning and press **Enter**.</span></span>

   <span data-ttu-id="49cb4-140">Une boîte de dialogue apparaît qui vous permet d’ajouter automatiquement les redirections de liaison nécessaires vers le fichier web.config source.</span><span class="sxs-lookup"><span data-stu-id="49cb4-140">A dialog box that enables you to automatically add the necessary binding redirects to the source web.config file appears.</span></span>

   <span data-ttu-id="49cb4-141">![Boîte de dialogue liaison de redirection autorisation](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")</span><span class="sxs-lookup"><span data-stu-id="49cb4-141">![Binding redirect permission dialog](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")</span></span>

## <a name="see-also"></a><span data-ttu-id="49cb4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49cb4-142">See also</span></span>

- [<span data-ttu-id="49cb4-143">\<bindingRedirect > élément</span><span class="sxs-lookup"><span data-stu-id="49cb4-143">\<bindingRedirect> Element</span></span>](../../../docs/framework/configure-apps/file-schema/runtime/bindingredirect-element.md)
- [<span data-ttu-id="49cb4-144">Redirection des versions d'assemblys</span><span class="sxs-lookup"><span data-stu-id="49cb4-144">Redirecting Assembly Versions</span></span>](../../../docs/framework/configure-apps/redirect-assembly-versions.md)
