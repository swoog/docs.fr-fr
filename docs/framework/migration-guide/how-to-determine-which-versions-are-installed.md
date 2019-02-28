---
title: 'Procédure : déterminer les versions du .NET Framework installées'
ms.date: 02/20/2019
dev_langs:
- csharp
- vb
ms.custom: updateeachrelease
helpviewer_keywords:
- versions, determining for .NET Framework
- .NET Framework, determining version
ms.assetid: 40a67826-e4df-4f59-a651-d9eb0fdc755d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7661b3ebaa8f29d6d3b2adbc56c405c8f0945f3
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584172"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a><span data-ttu-id="ff01a-102">Procédure : déterminer les versions du .NET Framework installées</span><span class="sxs-lookup"><span data-stu-id="ff01a-102">How to: Determine which .NET Framework versions are installed</span></span>

<span data-ttu-id="ff01a-103">Les utilisateurs peuvent installer et exécuter plusieurs versions de .NET Framework sur leurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="ff01a-103">Users can install and run multiple versions of the .NET Framework on their computers.</span></span> <span data-ttu-id="ff01a-104">Quand vous développez ou déployez votre application, vous pouvez avoir besoin de savoir quelles versions de .NET Framework sont installées sur l'ordinateur de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff01a-104">When you develop or deploy your app, you might need to know which .NET Framework versions are installed on the user’s computer.</span></span> <span data-ttu-id="ff01a-105">Notez que .NET Framework comporte deux principaux composants, dont les versions sont définies séparément :</span><span class="sxs-lookup"><span data-stu-id="ff01a-105">Note that the .NET Framework consists of two main components, which are versioned separately:</span></span>  
  
- <span data-ttu-id="ff01a-106">Un jeu d'assemblys, qui correspondent aux collections de types et de ressources qui fournissent les fonctionnalités de vos applications.</span><span class="sxs-lookup"><span data-stu-id="ff01a-106">A set of assemblies, which are collections of types and resources that provide the functionality for your apps.</span></span> <span data-ttu-id="ff01a-107">.NET Framework et les assemblys partagent le même numéro de version.</span><span class="sxs-lookup"><span data-stu-id="ff01a-107">The .NET Framework and assemblies share the same version number.</span></span>  
  
- <span data-ttu-id="ff01a-108">Le Common Language Runtime (CLR), qui gère et exécute le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="ff01a-108">The common language runtime (CLR), which manages and executes your app's code.</span></span> <span data-ttu-id="ff01a-109">Le CLR est identifié par son propre numéro de version (consultez [Versions et dépendances](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span><span class="sxs-lookup"><span data-stu-id="ff01a-109">The CLR is identified by its own version number (see [Versions and Dependencies](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span></span>  
  
<span data-ttu-id="ff01a-110">Pour obtenir la liste précise des versions de .NET Framework installées sur un ordinateur, vous pouvez consulter le Registre ou l'interroger en utilisant du code :</span><span class="sxs-lookup"><span data-stu-id="ff01a-110">To get an accurate list of the .NET Framework versions installed on a computer, you can view the registry or query the registry in code:</span></span>  
  
 [<span data-ttu-id="ff01a-111">Identifier les versions 1-4 de .NET Framework dans le Registre</span><span class="sxs-lookup"><span data-stu-id="ff01a-111">Find .NET Framework versions 1-4 in the registry</span></span>](#net_a)  
 [<span data-ttu-id="ff01a-112">Identifier les versions 4.5 et ultérieures de .NET Framework dans le Registre</span><span class="sxs-lookup"><span data-stu-id="ff01a-112">Find .NET Framework versions 4.5 and later in the registry)</span></span>](#net_b)  
 [<span data-ttu-id="ff01a-113">Utilisation de code pour interroger le Registre (versions 1-4)</span><span class="sxs-lookup"><span data-stu-id="ff01a-113">Using code to query the registry (versions 1-4)</span></span>](#net_c)  
 [<span data-ttu-id="ff01a-114">Utilisation de code pour interroger le Registre (version 4.5 et ultérieure)</span><span class="sxs-lookup"><span data-stu-id="ff01a-114">Using code to query the registry (version 4.5 and later)</span></span>](#net_d)  
 [<span data-ttu-id="ff01a-115">Utilisation de PowerShell pour interroger le Registre (version 4.5 et ultérieure)</span><span class="sxs-lookup"><span data-stu-id="ff01a-115">Using PowerShell to query the registry (version 4.5 and later)</span></span>](#ps_a)  

 <span data-ttu-id="ff01a-116">Pour rechercher la version CLR, vous pouvez utiliser un outil ou du code :</span><span class="sxs-lookup"><span data-stu-id="ff01a-116">To find the CLR version, you can use a tool or code:</span></span>  
  
 [<span data-ttu-id="ff01a-117">Utilisation de l’outil Clrver</span><span class="sxs-lookup"><span data-stu-id="ff01a-117">Using the Clrver tool</span></span>](#clr_a)  
 [<span data-ttu-id="ff01a-118">Utilisation de code pour interroger la classe System.Environment</span><span class="sxs-lookup"><span data-stu-id="ff01a-118">Using code to query the System.Environment class</span></span>](#clr_b)  

> [!NOTE]
> <span data-ttu-id="ff01a-119">Il existe une différence entre la version de .NET Framework et celle du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="ff01a-119">There is a difference between the .NET Framework version and the common language runtime (CLR) version.</span></span> <span data-ttu-id="ff01a-120">Les versions de .NET Framework dépendent du jeu d’assemblys qui constituent la bibliothèque de classes .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff01a-120">The .NET Framework is versioned based on the set of assemblies that form the .NET Framework Class Library.</span></span> <span data-ttu-id="ff01a-121">Par exemple, 4.5, 4.6.1 et 4.7.2 sont des versions de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff01a-121">For example, .NET Framework versions include 4.5, 4.6.1, and 4.7.2.</span></span> <span data-ttu-id="ff01a-122">Les versions du CLR sont créées selon le runtime sur lequel s’exécutent les applications .NET Framework ; une même version du CLR prend généralement en charge plusieurs versions de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff01a-122">The CLR is versioned based on the runtime on which .NET Framework applications execute, and a single CLR version typically supports multiple .NET Framework versions.</span></span> <span data-ttu-id="ff01a-123">Le CLR version 4.30319.*xxxxx* prend en charge les versions 4 à 4.5.2 de .NET Framework ; le CLR version 4.30319.42000 prend en charge toutes les versions de .NET Framework à partir de .NET Framework 4.6.</span><span class="sxs-lookup"><span data-stu-id="ff01a-123">CLR version 4.30319.*xxxxx* supports .NET Framework versions 4 through 4.5.2; CLR version 4.30319.42000 supports .NET Framework versions starting with .NET Framework 4.6.</span></span> <span data-ttu-id="ff01a-124">Pour plus d'informations, consultez la propriété <xref:System.Environment.Version?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ff01a-124">For more information, see the <xref:System.Environment.Version?displayProperty=nameWithType> property.</span></span>

 <span data-ttu-id="ff01a-125">Pour plus d’informations sur la détection des mises à jour installées pour chaque version de .NET Framework, consultez [Guide pratique pour déterminer les mises à jour .NET Framework installées](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span><span class="sxs-lookup"><span data-stu-id="ff01a-125">For information about detecting the installed updates for each version of the .NET Framework, see [How to: Determine Which .NET Framework Updates Are Installed](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span></span> <span data-ttu-id="ff01a-126">Pour plus d’informations sur l’installation du .NET Framework, consultez [Installer le .NET Framework pour les développeurs](../../../docs/framework/install/guide-for-developers.md).</span><span class="sxs-lookup"><span data-stu-id="ff01a-126">For information about installing the .NET Framework, see [Install the .NET Framework for developers](../../../docs/framework/install/guide-for-developers.md).</span></span>  
  
<a name="net_a"></a>   
## <a name="find-net-framework-versions-1-4-in-the-registry"></a><span data-ttu-id="ff01a-127">Identifier les versions 1-4 de .NET Framework dans le Registre</span><span class="sxs-lookup"><span data-stu-id="ff01a-127">Find .NET Framework versions 1-4 in the registry</span></span> 
  
1.  <span data-ttu-id="ff01a-128">Dans le menu **Démarrer**, choisissez **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="ff01a-128">On the **Start** menu, choose **Run**.</span></span>  
  
2.  <span data-ttu-id="ff01a-129">Dans la zone **Ouvrir**, entrez **regedit.exe**.</span><span class="sxs-lookup"><span data-stu-id="ff01a-129">In the **Open** box, enter **regedit.exe**.</span></span>  
  
     <span data-ttu-id="ff01a-130">Vous devez disposer d'informations d'identification d'administration pour exécuter regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="ff01a-130">You must have administrative credentials to run regedit.exe.</span></span>  
  
3.  <span data-ttu-id="ff01a-131">Dans l'Éditeur du Registre, ouvrez la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="ff01a-131">In the Registry Editor, open the following subkey:</span></span>  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     <span data-ttu-id="ff01a-132">Pour les versions 1.1 à 3.5 de .NET Framework, les versions installées sont présentées sous la forme de sous-clés sous la sous-clé `NDP`.</span><span class="sxs-lookup"><span data-stu-id="ff01a-132">For .NET Framework versions 1.1 through 3.5, the installed versions are listed as subkeys under the `NDP` subkey.</span></span> <span data-ttu-id="ff01a-133">Le numéro de version est stocké dans l’entrée **Version** de la sous-clé de version.</span><span class="sxs-lookup"><span data-stu-id="ff01a-133">The version number is stored in the version subkey's **Version** entry.</span></span> 
     
     <span data-ttu-id="ff01a-134">Pour .NET Framework 4, l’entrée **Version** se trouve sous la sous-clé `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Client`, `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Full` ou les deux.</span><span class="sxs-lookup"><span data-stu-id="ff01a-134">For .NET Framework 4, the **Version** entry is under the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Client` subkey, the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Full` subkey, or under both subkeys.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff01a-135">Le dossier d’installation « NET Framework Setup » dans le Registre ne commence pas par un point.</span><span class="sxs-lookup"><span data-stu-id="ff01a-135">The "NET Framework Setup" folder in the registry does not begin with a period.</span></span>

    <span data-ttu-id="ff01a-136">L’illustration suivante montre la sous-clé de .NET Framework 3.5 avec son entrée **Version**.</span><span class="sxs-lookup"><span data-stu-id="ff01a-136">The following figure shows that the subkey for the .NET Framework 3.5 along with its **Version** entry.</span></span>

     <span data-ttu-id="ff01a-137">![Entrée de Registre pour .NET Framework 3.5](../../../docs/framework/migration-guide/media/net-4-and-earlier.png ".NET Framework 4 et versions antérieures")</span><span class="sxs-lookup"><span data-stu-id="ff01a-137">![The registry entry for the .NET Framework 3.5.](../../../docs/framework/migration-guide/media/net-4-and-earlier.png ".NET Framework 4 and earlier versions")</span></span>

<a name="net_b"></a> 
## <a name="find-net-framework-versions-45-and-later-in-the-registry"></a><span data-ttu-id="ff01a-138">Identifier les versions 4.5 et ultérieures de .NET Framework dans le Registre</span><span class="sxs-lookup"><span data-stu-id="ff01a-138">Find .NET Framework versions 4.5 and later in the registry</span></span>

1. <span data-ttu-id="ff01a-139">Dans le menu **Démarrer**, choisissez **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="ff01a-139">On the **Start** menu, choose **Run**.</span></span>

2. <span data-ttu-id="ff01a-140">Dans la zone **Ouvrir**, entrez **regedit.exe**.</span><span class="sxs-lookup"><span data-stu-id="ff01a-140">In the **Open** box, enter **regedit.exe**.</span></span>

     <span data-ttu-id="ff01a-141">Vous devez disposer d'informations d'identification d'administration pour exécuter regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="ff01a-141">You must have administrative credentials to run regedit.exe.</span></span>

3. <span data-ttu-id="ff01a-142">Dans l'Éditeur du Registre, ouvrez la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="ff01a-142">In the Registry Editor, open the following subkey:</span></span>

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     <span data-ttu-id="ff01a-143">Notez que le chemin d'accès à la sous-clé `Full` inclut le `Net Framework` de la sous-clé plutôt que `.NET Framework`.</span><span class="sxs-lookup"><span data-stu-id="ff01a-143">Note that the path to the `Full` subkey includes the subkey `Net Framework` rather than `.NET Framework`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff01a-144">Si la sous-clé `Full` n'est pas disponible, le .NET Framework 4.5 ou version ultérieure n'est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ff01a-144">If the `Full` subkey is not present, then you do not have the .NET Framework 4.5 or later installed.</span></span>

     <span data-ttu-id="ff01a-145">Recherchez une valeur DWORD nommée `Release`.</span><span class="sxs-lookup"><span data-stu-id="ff01a-145">Check for a DWORD value named `Release`.</span></span> <span data-ttu-id="ff01a-146">La présence du DWORD `Release` indique que .NET Framework 4.5 (ou une version ultérieure) est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff01a-146">The existence of the `Release` DWORD indicates that .NET Framework 4.5 or later has been installed on that computer.</span></span> <span data-ttu-id="ff01a-147">Sa valeur est une clé de version correspondant à une version particulière de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff01a-147">Its value is a release key that corresponds to a particular version of .NET Framework.</span></span> <span data-ttu-id="ff01a-148">Dans l’illustration suivante, par exemple, la valeur DWORD `Release` est 378389, à savoir la clé de version de .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="ff01a-148">In the following figure, for example, the value of the `Release` DWORD is 378389, which is the release key for .NET Framework 4.5.</span></span> 

     <span data-ttu-id="ff01a-149">![L’entrée du Registre du .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span><span class="sxs-lookup"><span data-stu-id="ff01a-149">![The registry entry for the .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span></span>

<span data-ttu-id="ff01a-150">Le tableau suivant présente la valeur minimale de la valeur DWORD `Release` pour chaque version de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff01a-150">The following table lists the minimum value of the `Release` DWORD for each .NET Framework version.</span></span> <span data-ttu-id="ff01a-151">Vous pouvez utiliser ces valeurs de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="ff01a-151">You can use these values as follows:</span></span>

- <span data-ttu-id="ff01a-152">Pour déterminer si une version minimale de .NET Framework est présente, testez si la valeur DWORD `Release` trouvée dans le Registre est *supérieure ou égale à* la valeur figurant dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ff01a-152">To determine whether a minimum .NET Framework version is present, test whether the `Release` DWORD value found in the registry is *greater than or equal to* the value listed in the table.</span></span> <span data-ttu-id="ff01a-153">Par exemple, si votre application exige .NET Framework 4.7 ou une version ultérieure, vérifiez que la valeur de clé de version est au minimum 460798.</span><span class="sxs-lookup"><span data-stu-id="ff01a-153">For example, if your application requires .NET Framework 4.7 or later, you would test for a minimum release key value of 460798.</span></span>

- <span data-ttu-id="ff01a-154">Pour tester plusieurs versions, commencez par la dernière version de .NET Framework, puis passez successivement à des versions de plus en plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="ff01a-154">To test for multiple versions, begin with the latest .NET Framework version, and then test for each successive earlier version.</span></span>

[!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

|<span data-ttu-id="ff01a-155">Version du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ff01a-155">.NET Framework Version</span></span>|<span data-ttu-id="ff01a-156">Valeur du paramètre DWORD Release</span><span class="sxs-lookup"><span data-stu-id="ff01a-156">Value of the Release DWORD</span></span>|
|--------------------------------|-------------|
|<span data-ttu-id="ff01a-157">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="ff01a-157">.NET Framework 4.5</span></span>|<span data-ttu-id="ff01a-158">378389</span><span class="sxs-lookup"><span data-stu-id="ff01a-158">378389</span></span>|
|<span data-ttu-id="ff01a-159">.NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="ff01a-159">.NET Framework 4.5.1</span></span>|<span data-ttu-id="ff01a-160">378675</span><span class="sxs-lookup"><span data-stu-id="ff01a-160">378675</span></span>|
|<span data-ttu-id="ff01a-161">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="ff01a-161">.NET Framework 4.5.2</span></span>|<span data-ttu-id="ff01a-162">379893</span><span class="sxs-lookup"><span data-stu-id="ff01a-162">379893</span></span>|
|<span data-ttu-id="ff01a-163">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="ff01a-163">.NET Framework 4.6</span></span>|<span data-ttu-id="ff01a-164">393295</span><span class="sxs-lookup"><span data-stu-id="ff01a-164">393295</span></span>|
|<span data-ttu-id="ff01a-165">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="ff01a-165">.NET Framework 4.6.1</span></span>|<span data-ttu-id="ff01a-166">394254</span><span class="sxs-lookup"><span data-stu-id="ff01a-166">394254</span></span>|
|<span data-ttu-id="ff01a-167">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="ff01a-167">.NET Framework 4.6.2</span></span>|<span data-ttu-id="ff01a-168">394802</span><span class="sxs-lookup"><span data-stu-id="ff01a-168">394802</span></span>|
|<span data-ttu-id="ff01a-169">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="ff01a-169">.NET Framework 4.7</span></span>|<span data-ttu-id="ff01a-170">460798</span><span class="sxs-lookup"><span data-stu-id="ff01a-170">460798</span></span>|
|<span data-ttu-id="ff01a-171">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="ff01a-171">.NET Framework 4.7.1</span></span>|<span data-ttu-id="ff01a-172">461308</span><span class="sxs-lookup"><span data-stu-id="ff01a-172">461308</span></span>|
|<span data-ttu-id="ff01a-173">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="ff01a-173">.NET Framework 4.7.2</span></span>|<span data-ttu-id="ff01a-174">461808</span><span class="sxs-lookup"><span data-stu-id="ff01a-174">461808</span></span>|

<span data-ttu-id="ff01a-175">Pour un tableau complet des clés de version de .NET Framework sur des versions spécifiques du système d’exploitation Windows, voir [Clés de version de .NET Framework et versions du système d’exploitation Windows](release-keys-and-os-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ff01a-175">For a complete table of release keys for the .NET Framework for specific Windows operating system versions, see [.NET Framework release keys and Windows operating system versions](release-keys-and-os-versions.md).</span></span>

<a name="net_c"></a> 
## <a name="find-net-framework-versions-1-4-with-code"></a><span data-ttu-id="ff01a-176">Identifier les versions 1-4 de .NET Framework avec du code</span><span class="sxs-lookup"><span data-stu-id="ff01a-176">Find .NET Framework versions 1-4 with code</span></span>

- <span data-ttu-id="ff01a-177">Utilisez la classe <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> pour accéder à la sous-clé `Software\Microsoft\NET Framework Setup\NDP\` sous la branche `HKEY_LOCAL_MACHINE` dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="ff01a-177">Use the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the `Software\Microsoft\NET Framework Setup\NDP\` subkey under `HKEY_LOCAL_MACHINE` branch in the Windows registry.</span></span>

     <span data-ttu-id="ff01a-178">Le code ci-dessous est un exemple de cette requête.</span><span class="sxs-lookup"><span data-stu-id="ff01a-178">The following code shows an example of this query.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff01a-179">Ce code ne montre pas comment détecter .NET Framework 4.5 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ff01a-179">This code does not show how to detect .NET Framework 4.5 or later.</span></span> <span data-ttu-id="ff01a-180">Examinez la valeur de DWORD `Release` pour détecter ces versions, comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="ff01a-180">Check the `Release` DWORD to detect those versions, as described in the previous section.</span></span> <span data-ttu-id="ff01a-181">Pour passer au code qui détecte .NET Framework 4.5 et les versions ultérieures, voir la section suivante de cet article.</span><span class="sxs-lookup"><span data-stu-id="ff01a-181">For code that detects .NET Framework 4.5 or later versions, see the next section in this article.</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

<a name="net_d"></a> 
## <a name="find-net-framework-versions-45-and-later-with-code"></a><span data-ttu-id="ff01a-182">Identifier les versions 4.5 et ultérieures de .NET Framework avec du code</span><span class="sxs-lookup"><span data-stu-id="ff01a-182">Find .NET Framework versions 4.5 and later with code</span></span>

1. <span data-ttu-id="ff01a-183">L'existence de la valeur DWORD `Release` dans la clé `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` indique que .NET Framework 4.5 (ou une version ultérieure) est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff01a-183">The existence of the `Release` DWORD in the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` key indicates that the .NET Framework 4.5 or later is installed on a computer.</span></span> <span data-ttu-id="ff01a-184">La valeur du mot clé indique la version installée.</span><span class="sxs-lookup"><span data-stu-id="ff01a-184">The value of the keyword indicates the installed version.</span></span> <span data-ttu-id="ff01a-185">Pour vérifier ce mot clé, utilisez les méthodes <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A?displayProperty=nameWithType> et <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A?displayProperty=nameWithType> afin d’accéder à la sous-clé dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="ff01a-185">To check this keyword, use the <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A?displayProperty=nameWithType> and <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A?displayProperty=nameWithType> methods to access the subkey in the Windows registry.</span></span>

2. <span data-ttu-id="ff01a-186">Vérifiez la valeur du mot clé `Release` pour déterminer la version installée.</span><span class="sxs-lookup"><span data-stu-id="ff01a-186">Check the value of the `Release` keyword to determine the installed version.</span></span> <span data-ttu-id="ff01a-187">Dans une optique de compatibilité ascendante, vous pouvez vérifier la présence d’une valeur supérieure ou égale à celle du tableau de la section [Identifier les versions 4.5 et ultérieures de .NET Framework dans le Registre](#net_b).</span><span class="sxs-lookup"><span data-stu-id="ff01a-187">To be forward-compatible, you can check for a value greater than or equal to the value listed in the table in the [Find .NET Framework versions 4.5 and later in the registry](#net_b) section.</span></span>

<span data-ttu-id="ff01a-188">L’exemple suivant vérifie la valeur `Release` dans le Registre pour déterminer si .NET Framework 4.5 ou une version ultérieure est installée.</span><span class="sxs-lookup"><span data-stu-id="ff01a-188">The following example checks the `Release` value in the registry to determine whether .NET Framework 4.5 or a later version is installed.</span></span>

[!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
[!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

<span data-ttu-id="ff01a-189">Cet exemple suit la pratique recommandée concernant la vérification de version :</span><span class="sxs-lookup"><span data-stu-id="ff01a-189">This example follows the recommended practice for version checking:</span></span>

- <span data-ttu-id="ff01a-190">Il vérifie si la valeur de l’entrée `Release` est *supérieure ou égale à* la valeur des clés de version connues.</span><span class="sxs-lookup"><span data-stu-id="ff01a-190">It checks whether the value of the `Release` entry is *greater than or equal to* the value of the known release keys.</span></span>

- <span data-ttu-id="ff01a-191">Il effectue sa vérification en partant de la version la plus récente vers la version la plus ancienne.</span><span class="sxs-lookup"><span data-stu-id="ff01a-191">It checks in order from most recent version to earliest version.</span></span>

<a name="ps_a"></a> 
## <a name="check-for-a-minimum-required-net-framework-version-45-and-later-with-powershell"></a><span data-ttu-id="ff01a-192">Rechercher une version minimale requise de .NET Framework (4.5 ou ultérieure) avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff01a-192">Check for a minimum required .NET Framework version (4.5 and later) with PowerShell</span></span>

<span data-ttu-id="ff01a-193">L’exemple suivant vérifie la valeur du mot clé `Release` pour déterminer si .NET Framework 4.6.2 ou une version ultérieure est installé (retourne `True` si la condition est vérifiée, `False` sinon).</span><span class="sxs-lookup"><span data-stu-id="ff01a-193">The following example checks the value of the `Release` keyword to determine whether .NET Framework 4.6.2 or higher is installed (returning `True` if it is and `False` otherwise).</span></span>

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    You can replace `394802` in the previous example with another value from the following table in the [Find .NET Framework versions 4.5 and later in the registry](#net_b) section to check for a different minimum required .NET Framework version.
  
<a name="clr_a"></a> 
## <a name="find-the-current-clr-version-with-clrverexe"></a><span data-ttu-id="ff01a-194">Identifier la version actuelle du CLR avec Clrver.exe</span><span class="sxs-lookup"><span data-stu-id="ff01a-194">Find the current CLR version with Clrver.exe</span></span>

<span data-ttu-id="ff01a-195">Utilisez l'outil de version CLR (Clrver.exe) pour déterminer quelles versions du CLR (Common Language Runtime) sont installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff01a-195">Use the CLR Version Tool (Clrver.exe) to determine which versions of the common language runtime are installed on a computer.</span></span>

<span data-ttu-id="ff01a-196">À partir d’une invite de commandes développeur pour Visual Studio, entrez `clrver`.</span><span class="sxs-lookup"><span data-stu-id="ff01a-196">From a Developer Command Prompt for Visual Studio, enter `clrver`.</span></span> <span data-ttu-id="ff01a-197">Cette commande produit un résultat similaire au suivant :</span><span class="sxs-lookup"><span data-stu-id="ff01a-197">This command produces output similar to the following:</span></span>

```console
Versions installed on the machine:
v2.0.50727
v4.0.30319
```

<span data-ttu-id="ff01a-198">Pour plus d’informations sur l’utilisation de cet outil, consultez [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span><span class="sxs-lookup"><span data-stu-id="ff01a-198">For more information about using this tool, see [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span></span>

<a name="clr_b"></a> 
## <a name="find-the-current-clr-version-with-the-environment-class"></a><span data-ttu-id="ff01a-199">Identifier la version actuelle du CLR avec la classe Environment</span><span class="sxs-lookup"><span data-stu-id="ff01a-199">Find the current CLR version with the Environment class</span></span>

<span data-ttu-id="ff01a-200">Vous pouvez récupérer la valeur de la propriété <xref:System.Environment.Version?displayProperty=nameWithType> pour obtenir un objet <xref:System.Version> identifiant la version du runtime.</span><span class="sxs-lookup"><span data-stu-id="ff01a-200">You can retrieve the value of the <xref:System.Environment.Version?displayProperty=nameWithType> property to retrieve a <xref:System.Version> object that identifies the version of the runtime that is currently executing the code.</span></span> <span data-ttu-id="ff01a-201">Cette propriété retourne une valeur unique reflétant la version du runtime qui exécute actuellement le code, et non les versions d’assembly ou d’autres versions du runtime qui peuvent avoir été installées sur l’ordinateur. Vous pouvez utiliser la propriété <xref:System.Version.Major%2A?displayProperty=nameWithType> pour obtenir l’identificateur de version majeure (par exemple, « 4 » pour la version 4.0), la propriété <xref:System.Version.Minor%2A?displayProperty=nameWithType> pour l’identificateur de version mineure (par exemple, « 0 » pour la version 4.0) ou la méthode <xref:System.Version.ToString%2A?displayProperty=nameWithType> pour la totalité de la chaîne de version (par exemple, « 4.0.30319.18010 », comme dans le code suivant).</span><span class="sxs-lookup"><span data-stu-id="ff01a-201">This property returns a single value that reflects the version of the runtime that is currently executing the code; it does not return assembly versions or other versions of the runtime that may have been installed on the computer.You can use the <xref:System.Version.Major%2A?displayProperty=nameWithType> property to get the major release identifier (for example, "4" for version 4.0), the <xref:System.Version.Minor%2A?displayProperty=nameWithType> property to get the minor release identifier (for example, "0" for version 4.0), or the <xref:System.Version.ToString%2A?displayProperty=nameWithType> method to get the entire version string (for example, "4.0.30319.18010", as shown in the following code).</span></span> 

<span data-ttu-id="ff01a-202">Pour .NET Framework versions 4, 4.5, 4.5.1 et 4.5.2, la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> retourne un objet <xref:System.Version> dont la représentation sous forme de chaîne se présente sous la forme `4.0.30319.xxxxx`.</span><span class="sxs-lookup"><span data-stu-id="ff01a-202">For the .NET Framework Versions 4, 4.5, 4.5.1, and 4.5.2, the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property returns a <xref:System.Version> object whose string representation has the form `4.0.30319.xxxxx`.</span></span> <span data-ttu-id="ff01a-203">Pour .NET Framework 4.6 et versions ultérieures, le format est `4.0.30319.42000`.</span><span class="sxs-lookup"><span data-stu-id="ff01a-203">For the .NET Framework 4.6 and later, it has the form `4.0.30319.42000`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff01a-204">Avec .NET Framework 4.5 et les versions ultérieures, nous déconseillons d’utiliser la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour détecter la version du runtime.</span><span class="sxs-lookup"><span data-stu-id="ff01a-204">For the .NET Framework 4.5 and later, we do not recommend using the  <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to detect the version of the runtime.</span></span> <span data-ttu-id="ff01a-205">Nous recommandons plutôt d’interroger le Registre, comme décrit dans la section [Pour déterminer les versions de .NET Framework en interrogeant le Registre à l’aide de code (.NET Framework 4.5 et ultérieur)](#net_d), plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="ff01a-205">Instead, we recommend that you query the registry, as described in the [To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)](#net_d) section earlier in this article.</span></span>

<span data-ttu-id="ff01a-206">L’exemple suivant utilise la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour récupérer les informations de version du runtime :</span><span class="sxs-lookup"><span data-stu-id="ff01a-206">The following example used the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to retrieve runtime version information:</span></span>

[!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
[!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

## <a name="see-also"></a><span data-ttu-id="ff01a-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff01a-207">See also</span></span>

- [<span data-ttu-id="ff01a-208">Guide pratique pour Déterminer les mises à jour .NET Framework installées</span><span class="sxs-lookup"><span data-stu-id="ff01a-208">How to: Determine Which .NET Framework Updates Are Installed</span></span>](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)
- [<span data-ttu-id="ff01a-209">Installer le .NET Framework pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="ff01a-209">Install the .NET Framework for developers</span></span>](../../../docs/framework/install/guide-for-developers.md)
- [<span data-ttu-id="ff01a-210">Versions et dépendances</span><span class="sxs-lookup"><span data-stu-id="ff01a-210">Versions and Dependencies</span></span>](~/docs/framework/migration-guide/versions-and-dependencies.md)
