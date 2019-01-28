---
title: 'Procédure : déterminer les versions du .NET Framework installées'
ms.date: 04/10/2018
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
ms.openlocfilehash: 31200b72cb551c91791e2e14332aacab8e7f0519
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672004"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a><span data-ttu-id="f3811-102">Procédure : déterminer les versions du .NET Framework installées</span><span class="sxs-lookup"><span data-stu-id="f3811-102">How to: Determine which .NET Framework versions are installed</span></span>

<span data-ttu-id="f3811-103">Les utilisateurs peuvent installer et exécuter plusieurs versions de .NET Framework sur leurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="f3811-103">Users can install and run multiple versions of the .NET Framework on their computers.</span></span> <span data-ttu-id="f3811-104">Quand vous développez ou déployez votre application, vous pouvez avoir besoin de savoir quelles versions de .NET Framework sont installées sur l'ordinateur de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3811-104">When you develop or deploy your app, you might need to know which .NET Framework versions are installed on the user’s computer.</span></span> <span data-ttu-id="f3811-105">Notez que .NET Framework comporte deux principaux composants, dont les versions sont définies séparément :</span><span class="sxs-lookup"><span data-stu-id="f3811-105">Note that the .NET Framework consists of two main components, which are versioned separately:</span></span>  
  
-   <span data-ttu-id="f3811-106">Un jeu d'assemblys, qui correspondent aux collections de types et de ressources qui fournissent les fonctionnalités de vos applications.</span><span class="sxs-lookup"><span data-stu-id="f3811-106">A set of assemblies, which are collections of types and resources that provide the functionality for your apps.</span></span> <span data-ttu-id="f3811-107">.NET Framework et les assemblys partagent le même numéro de version.</span><span class="sxs-lookup"><span data-stu-id="f3811-107">The .NET Framework and assemblies share the same version number.</span></span>  
  
-   <span data-ttu-id="f3811-108">Le Common Language Runtime (CLR), qui gère et exécute le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="f3811-108">The common language runtime (CLR), which manages and executes your app's code.</span></span> <span data-ttu-id="f3811-109">Le CLR est identifié par son propre numéro de version (consultez [Versions et dépendances](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span><span class="sxs-lookup"><span data-stu-id="f3811-109">The CLR is identified by its own version number (see [Versions and Dependencies](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span></span>  
  
 <span data-ttu-id="f3811-110">Pour obtenir la liste précise des versions de .NET Framework installées sur un ordinateur, vous pouvez consulter le Registre ou l'interroger en utilisant du code :</span><span class="sxs-lookup"><span data-stu-id="f3811-110">To get an accurate list of the .NET Framework versions installed on a computer, you can view the registry or query the registry in code:</span></span>  
  
 [<span data-ttu-id="f3811-111">Affichage du Registre (versions 1-4)</span><span class="sxs-lookup"><span data-stu-id="f3811-111">Viewing the registry (versions 1-4)</span></span>](#net_a)  
 [<span data-ttu-id="f3811-112">Affichage du Registre (version 4.5 et ultérieure)</span><span class="sxs-lookup"><span data-stu-id="f3811-112">Viewing the registry (version 4.5 and later)</span></span>](#net_b)  
 [<span data-ttu-id="f3811-113">Utilisation de code pour interroger le Registre (versions 1-4)</span><span class="sxs-lookup"><span data-stu-id="f3811-113">Using code to query the registry (versions 1-4)</span></span>](#net_c)  
 [<span data-ttu-id="f3811-114">Utilisation de code pour interroger le Registre (version 4.5 et ultérieure)</span><span class="sxs-lookup"><span data-stu-id="f3811-114">Using code to query the registry (version 4.5 and later)</span></span>](#net_d)  
 [<span data-ttu-id="f3811-115">Utilisation de PowerShell pour interroger le Registre (version 4.5 et ultérieure)</span><span class="sxs-lookup"><span data-stu-id="f3811-115">Using PowerShell to query the registry (version 4.5 and later)</span></span>](#ps_a)  
  
 <span data-ttu-id="f3811-116">Pour rechercher la version CLR, vous pouvez utiliser un outil ou du code :</span><span class="sxs-lookup"><span data-stu-id="f3811-116">To find the CLR version, you can use a tool or code:</span></span>  
  
 [<span data-ttu-id="f3811-117">Utilisation de l’outil Clrver</span><span class="sxs-lookup"><span data-stu-id="f3811-117">Using the Clrver tool</span></span>](#clr_a)  
 [<span data-ttu-id="f3811-118">Utilisation de code pour interroger la classe System.Environment</span><span class="sxs-lookup"><span data-stu-id="f3811-118">Using code to query the System.Environment class</span></span>](#clr_b)  
  
 <span data-ttu-id="f3811-119">Pour plus d’informations sur la détection des mises à jour installées pour chaque version de .NET Framework, consultez [Guide pratique pour déterminer les mises à jour .NET Framework installées](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span><span class="sxs-lookup"><span data-stu-id="f3811-119">For information about detecting the installed updates for each version of the .NET Framework, see [How to: Determine Which .NET Framework Updates Are Installed](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span></span> <span data-ttu-id="f3811-120">Pour plus d’informations sur l’installation du .NET Framework, consultez [Installer le .NET Framework pour les développeurs](../../../docs/framework/install/guide-for-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f3811-120">For information about installing the .NET Framework, see [Install the .NET Framework for developers](../../../docs/framework/install/guide-for-developers.md).</span></span>  
  
<a name="net_a"></a>   
## <a name="to-find-net-framework-versions-by-viewing-the-registry-net-framework-1-4"></a><span data-ttu-id="f3811-121">Pour déterminer les versions du .NET Framework en affichant le Registre (.NET Framework 1-4)</span><span class="sxs-lookup"><span data-stu-id="f3811-121">To find .NET Framework versions by viewing the registry (.NET Framework 1-4)</span></span>  
  
1.  <span data-ttu-id="f3811-122">Dans le menu **Démarrer**, choisissez **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="f3811-122">On the **Start** menu, choose **Run**.</span></span>  
  
2.  <span data-ttu-id="f3811-123">Dans la zone **Ouvrir**, entrez **regedit.exe**.</span><span class="sxs-lookup"><span data-stu-id="f3811-123">In the **Open** box, enter **regedit.exe**.</span></span>  
  
     <span data-ttu-id="f3811-124">Vous devez disposer d'informations d'identification d'administration pour exécuter regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="f3811-124">You must have administrative credentials to run regedit.exe.</span></span>  
  
3.  <span data-ttu-id="f3811-125">Dans l'Éditeur du Registre, ouvrez la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="f3811-125">In the Registry Editor, open the following subkey:</span></span>  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     <span data-ttu-id="f3811-126">Les versions installées sont répertoriées sous la sous-clé NDP.</span><span class="sxs-lookup"><span data-stu-id="f3811-126">The installed versions are listed under the NDP subkey.</span></span> <span data-ttu-id="f3811-127">Le numéro de version est stocké dans l’entrée **Version**.</span><span class="sxs-lookup"><span data-stu-id="f3811-127">The version number is stored in the **Version** entry.</span></span> <span data-ttu-id="f3811-128">Pour [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], l’entrée **Version** se trouve sous la sous-clé Client ou Full (sous NDP), ou sous les deux sous-clés.</span><span class="sxs-lookup"><span data-stu-id="f3811-128">For the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] the **Version** entry is under the Client or Full subkey (under NDP), or under both subkeys.</span></span>  
  

    > [!NOTE]
    > <span data-ttu-id="f3811-129">Le dossier d’installation « NET Framework Setup » dans le Registre ne commence pas par un point.</span><span class="sxs-lookup"><span data-stu-id="f3811-129">The "NET Framework Setup" folder in the registry does not begin with a period.</span></span>

<a name="net_b"></a> 
## <a name="to-find-net-framework-versions-by-viewing-the-registry-net-framework-45-and-later"></a><span data-ttu-id="f3811-130">Pour déterminer les versions de .NET Framework en affichant le Registre (.NET Framework 4.5 et ultérieur)</span><span class="sxs-lookup"><span data-stu-id="f3811-130">To find .NET Framework versions by viewing the registry (.NET Framework 4.5 and later)</span></span>

1. <span data-ttu-id="f3811-131">Dans le menu **Démarrer**, choisissez **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="f3811-131">On the **Start** menu, choose **Run**.</span></span>

2. <span data-ttu-id="f3811-132">Dans la zone **Ouvrir**, entrez **regedit.exe**.</span><span class="sxs-lookup"><span data-stu-id="f3811-132">In the **Open** box, enter **regedit.exe**.</span></span>

     <span data-ttu-id="f3811-133">Vous devez disposer d'informations d'identification d'administration pour exécuter regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="f3811-133">You must have administrative credentials to run regedit.exe.</span></span>

3. <span data-ttu-id="f3811-134">Dans l'Éditeur du Registre, ouvrez la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="f3811-134">In the Registry Editor, open the following subkey:</span></span>

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     <span data-ttu-id="f3811-135">Notez que le chemin d'accès à la sous-clé `Full` inclut le `Net Framework` de la sous-clé plutôt que `.NET Framework`.</span><span class="sxs-lookup"><span data-stu-id="f3811-135">Note that the path to the `Full` subkey includes the subkey `Net Framework` rather than `.NET Framework`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3811-136">Si la sous-clé `Full` n'est pas disponible, le .NET Framework 4.5 ou version ultérieure n'est pas installé.</span><span class="sxs-lookup"><span data-stu-id="f3811-136">If the `Full` subkey is not present, then you do not have the .NET Framework 4.5 or later installed.</span></span>

     <span data-ttu-id="f3811-137">Recherchez une valeur DWORD nommée `Release`.</span><span class="sxs-lookup"><span data-stu-id="f3811-137">Check for a DWORD value named `Release`.</span></span> <span data-ttu-id="f3811-138">L'existence de la valeur DWORD `Release` indique que [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] ou une version plus récente a été installé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3811-138">The existence of the `Release` DWORD indicates that the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or newer has been installed on that computer.</span></span>

     <span data-ttu-id="f3811-139">![L’entrée du Registre du .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span><span class="sxs-lookup"><span data-stu-id="f3811-139">![The registry entry for the .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span></span>

     <span data-ttu-id="f3811-140">La valeur du paramètre DWORD `Release` indique quelle version du .NET Framework est installée.</span><span class="sxs-lookup"><span data-stu-id="f3811-140">The value of the `Release` DWORD indicates which version of the .NET Framework is installed.</span></span>

    [!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

    |<span data-ttu-id="f3811-141">Valeur du paramètre DWORD Release</span><span class="sxs-lookup"><span data-stu-id="f3811-141">Value of the Release DWORD</span></span>|<span data-ttu-id="f3811-142">Version</span><span class="sxs-lookup"><span data-stu-id="f3811-142">Version</span></span>|
    |--------------------------------|-------------|
    |<span data-ttu-id="f3811-143">378389</span><span class="sxs-lookup"><span data-stu-id="f3811-143">378389</span></span>|<span data-ttu-id="f3811-144">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="f3811-144">.NET Framework 4.5</span></span>|
    |<span data-ttu-id="f3811-145">378675</span><span class="sxs-lookup"><span data-stu-id="f3811-145">378675</span></span>|<span data-ttu-id="f3811-146">.NET Framework 4.5.1 installé avec Windows 8.1 ou Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f3811-146">.NET Framework 4.5.1 installed with Windows 8.1 or Windows Server 2012 R2</span></span>|
    |<span data-ttu-id="f3811-147">378758</span><span class="sxs-lookup"><span data-stu-id="f3811-147">378758</span></span>|<span data-ttu-id="f3811-148">.NET Framework 4.5.1 installé sur Windows 8, Windows 7 SP1, ou Windows Vista SP2</span><span class="sxs-lookup"><span data-stu-id="f3811-148">.NET Framework 4.5.1 installed on Windows 8, Windows 7 SP1, or Windows Vista SP2</span></span>|
    |<span data-ttu-id="f3811-149">379893</span><span class="sxs-lookup"><span data-stu-id="f3811-149">379893</span></span>|<span data-ttu-id="f3811-150">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="f3811-150">.NET Framework 4.5.2</span></span>|
    |<span data-ttu-id="f3811-151">Sur les systèmes Windows 10 uniquement : 393295</span><span class="sxs-lookup"><span data-stu-id="f3811-151">On Windows 10 systems only: 393295</span></span><br /><br /> <span data-ttu-id="f3811-152">Sur toutes les autres versions de système d’exploitation : 393297</span><span class="sxs-lookup"><span data-stu-id="f3811-152">On all other OS versions: 393297</span></span>|[!INCLUDE[net_v46](../../../includes/net-v46-md.md)]|
    |<span data-ttu-id="f3811-153">Sur les systèmes Windows 10 avec la mise à jour de novembre uniquement : 394254</span><span class="sxs-lookup"><span data-stu-id="f3811-153">On Windows 10 November Update systems only: 394254</span></span><br /><br /> <span data-ttu-id="f3811-154">Sur toutes les autres versions de système d’exploitation : 394271</span><span class="sxs-lookup"><span data-stu-id="f3811-154">On all other OS versions: 394271</span></span>|[!INCLUDE[net_v461](../../../includes/net-v461-md.md)]|
    |<span data-ttu-id="f3811-155">Sur les systèmes Mise à jour anniversaire Windows 10 et Windows Server 2016 : 394802</span><span class="sxs-lookup"><span data-stu-id="f3811-155">On Windows 10 Anniversary Update and Windows Server 2016: 394802</span></span><br /><br /> <span data-ttu-id="f3811-156">Sur toutes les autres versions de système d’exploitation : 394806</span><span class="sxs-lookup"><span data-stu-id="f3811-156">On all other OS versions: 394806</span></span>|[!INCLUDE[net_v462](../../../includes/net-v462-md.md)]| 
    |<span data-ttu-id="f3811-157">Sur les systèmes Windows 10 Creators Update uniquement : 460798</span><span class="sxs-lookup"><span data-stu-id="f3811-157">On Windows 10 Creators Update only: 460798</span></span><br/><br/> <span data-ttu-id="f3811-158">Sur toutes les autres versions de système d’exploitation : 460805</span><span class="sxs-lookup"><span data-stu-id="f3811-158">On all other OS versions: 460805</span></span> | <span data-ttu-id="f3811-159">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="f3811-159">.NET Framework 4.7</span></span> |
    |<span data-ttu-id="f3811-160">Sur les systèmes Windows 10 Fall Creators Update uniquement : 461308</span><span class="sxs-lookup"><span data-stu-id="f3811-160">On Windows 10 Fall Creators Update only: 461308</span></span><br/><br/> <span data-ttu-id="f3811-161">Sur toutes les autres versions de système d’exploitation : 461310</span><span class="sxs-lookup"><span data-stu-id="f3811-161">On all other OS versions: 461310</span></span> | <span data-ttu-id="f3811-162">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="f3811-162">.NET Framework 4.7.1</span></span> |
    |<span data-ttu-id="f3811-163">Sur les systèmes Windows 10 avec la mise à jour d’avril 2018 uniquement : 461808</span><span class="sxs-lookup"><span data-stu-id="f3811-163">On Windows 10 April 2018 Update only: 461808</span></span><br/><br/> <span data-ttu-id="f3811-164">Sur toutes les autres versions de système d’exploitation, y compris Windows 10 avec la mise à jour d’octobre 2018 : 461814</span><span class="sxs-lookup"><span data-stu-id="f3811-164">On all other OS versions, including Windows 10 October 2018 Update: 461814</span></span>| <span data-ttu-id="f3811-165">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f3811-165">.NET Framework 4.7.2</span></span> |
    
<a name="net_c"></a> 
## <a name="to-find-net-framework-versions-by-querying-the-registry-in-code-net-framework-1-4"></a><span data-ttu-id="f3811-166">Pour déterminer les versions de .NET Framework en interrogeant le Registre à l'aide de code (.NET Framework 1-4)</span><span class="sxs-lookup"><span data-stu-id="f3811-166">To find .NET Framework versions by querying the registry in code (.NET Framework 1-4)</span></span>

- <span data-ttu-id="f3811-167">Utilisez la classe <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> pour accéder à la sous-clé Software\Microsoft\NET Framework Setup\NDP\ sous HKEY_LOCAL_MACHINE, dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="f3811-167">Use the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the Software\Microsoft\NET Framework Setup\NDP\ subkey under HKEY_LOCAL_MACHINE in the Windows registry.</span></span>

     <span data-ttu-id="f3811-168">Le code ci-dessous est un exemple de cette requête.</span><span class="sxs-lookup"><span data-stu-id="f3811-168">The following code shows an example of this query.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3811-169">Ce code ne montre pas comment détecter le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f3811-169">This code does not show how to detect the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or later.</span></span> <span data-ttu-id="f3811-170">Examinez la valeur de DWORD `Release` pour détecter ces versions, comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="f3811-170">Check the `Release` DWORD to detect those versions, as described in the previous section.</span></span> <span data-ttu-id="f3811-171">Pour le code qui détecte le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] et versions ultérieures, consultez la section suivante de cet article.</span><span class="sxs-lookup"><span data-stu-id="f3811-171">For code that does detect the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or later versions, see the next section in this article.</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

     <span data-ttu-id="f3811-172">Cet exemple produit un résultat semblable au suivant :</span><span class="sxs-lookup"><span data-stu-id="f3811-172">The example produces output that's similar to the following:</span></span>

    ```
    v2.0.50727  2.0.50727.4016  SP2
    v3.0  3.0.30729.4037  SP2
    v3.5  3.5.30729.01  SP1
    v4
      Client  4.0.30319
      Full  4.0.30319
    ```

<a name="net_d"></a> 
## <a name="to-find-net-framework-versions-by-querying-the-registry-in-code-net-framework-45-and-later"></a><span data-ttu-id="f3811-173">Pour déterminer les versions de .NET Framework en interrogeant le Registre à l'aide de code (.NET Framework 4.5 et ultérieur)</span><span class="sxs-lookup"><span data-stu-id="f3811-173">To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)</span></span>

1. <span data-ttu-id="f3811-174">L'existence de la valeur DWORD `Release` indique que le .NET Framework 4.5 ou une version ultérieure a été installé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3811-174">The existence of the `Release` DWORD indicates that the .NET Framework 4.5 or later has been installed on a computer.</span></span> <span data-ttu-id="f3811-175">La valeur du mot clé indique la version installée.</span><span class="sxs-lookup"><span data-stu-id="f3811-175">The value of the keyword indicates the installed version.</span></span> <span data-ttu-id="f3811-176">Pour vérifier ce mot clé, utilisez les méthodes <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A> et <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A> de la classe <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> pour accéder à la sous-clé Software\Microsoft\NET Framework Setup\NDP\v4\Full, sous HKEY_LOCAL_MACHINE, dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="f3811-176">To check this keyword, use the <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A> and <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A> methods of the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the Software\Microsoft\NET Framework Setup\NDP\v4\Full subkey under HKEY_LOCAL_MACHINE in the Windows registry.</span></span>

2. <span data-ttu-id="f3811-177">Vérifiez la valeur du mot clé `Release` pour déterminer la version installée.</span><span class="sxs-lookup"><span data-stu-id="f3811-177">Check the value of the `Release` keyword to determine the installed version.</span></span> <span data-ttu-id="f3811-178">Pour une compatibilité ascendante, vérifiez que votre valeur est supérieure ou égale à celles répertoriées dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f3811-178">To be forward-compatible, you can check for a value greater than or equal to the values listed in the table.</span></span> <span data-ttu-id="f3811-179">Voici les versions du .NET Framework et les mots clés `Release` associés.</span><span class="sxs-lookup"><span data-stu-id="f3811-179">Here are the .NET Framework versions and associated `Release` keywords.</span></span>

    [!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

    |<span data-ttu-id="f3811-180">Version</span><span class="sxs-lookup"><span data-stu-id="f3811-180">Version</span></span>|<span data-ttu-id="f3811-181">Valeur du paramètre DWORD Release</span><span class="sxs-lookup"><span data-stu-id="f3811-181">Value of the Release DWORD</span></span>|
    |-------------|--------------------------------|
    |<span data-ttu-id="f3811-182">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="f3811-182">.NET Framework 4.5</span></span>|<span data-ttu-id="f3811-183">378389</span><span class="sxs-lookup"><span data-stu-id="f3811-183">378389</span></span>|
    |<span data-ttu-id="f3811-184">.NET Framework 4.5.1 installé avec Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3811-184">.NET Framework 4.5.1 installed with Windows 8.1</span></span>|<span data-ttu-id="f3811-185">378675</span><span class="sxs-lookup"><span data-stu-id="f3811-185">378675</span></span>|
    |<span data-ttu-id="f3811-186">.NET Framework 4.5.1 installé sur Windows 8, Windows 7 SP1, ou Windows Vista SP2</span><span class="sxs-lookup"><span data-stu-id="f3811-186">.NET Framework 4.5.1 installed on Windows 8, Windows 7 SP1, or Windows Vista SP2</span></span>|<span data-ttu-id="f3811-187">378758</span><span class="sxs-lookup"><span data-stu-id="f3811-187">378758</span></span>|
    |<span data-ttu-id="f3811-188">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="f3811-188">.NET Framework 4.5.2</span></span>|<span data-ttu-id="f3811-189">379893</span><span class="sxs-lookup"><span data-stu-id="f3811-189">379893</span></span>|
    |<span data-ttu-id="f3811-190">.NET Framework 4.6 installé avec Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3811-190">.NET Framework 4.6 installed with Windows 10</span></span>|<span data-ttu-id="f3811-191">393295</span><span class="sxs-lookup"><span data-stu-id="f3811-191">393295</span></span>|
    |<span data-ttu-id="f3811-192">.NET Framework 4.6 installé sur toutes les autres versions du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="f3811-192">.NET Framework 4.6 installed on all other Windows OS versions</span></span>|<span data-ttu-id="f3811-193">393297</span><span class="sxs-lookup"><span data-stu-id="f3811-193">393297</span></span>|
    |<span data-ttu-id="f3811-194">.NET Framework 4.6.1 installé sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3811-194">.NET Framework 4.6.1 installed on Windows 10</span></span>|<span data-ttu-id="f3811-195">394254</span><span class="sxs-lookup"><span data-stu-id="f3811-195">394254</span></span>|
    |<span data-ttu-id="f3811-196">.NET Framework 4.6.1 installé sur toutes les autres versions du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="f3811-196">.NET Framework 4.6.1 installed on all other Windows OS versions</span></span>|<span data-ttu-id="f3811-197">394271</span><span class="sxs-lookup"><span data-stu-id="f3811-197">394271</span></span>|
    |<span data-ttu-id="f3811-198">.NET Framework 4.6.2 installé sur la Mise à jour anniversaire Windows 10 et sur Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3811-198">.NET Framework 4.6.2 installed on Windows 10 Anniversary Update and Windows Server 2016</span></span>|<span data-ttu-id="f3811-199">394802</span><span class="sxs-lookup"><span data-stu-id="f3811-199">394802</span></span>|
    |<span data-ttu-id="f3811-200">.NET Framework 4.6.2 installé sur toutes les autres versions du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="f3811-200">.NET Framework 4.6.2 installed on all other Windows OS versions</span></span>|<span data-ttu-id="f3811-201">394806</span><span class="sxs-lookup"><span data-stu-id="f3811-201">394806</span></span>|
    |<span data-ttu-id="f3811-202">.NET Framework 4.7 est installé sur Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="f3811-202">.NET Framework 4.7 installed on Windows 10 Creators Update</span></span>|<span data-ttu-id="f3811-203">460798</span><span class="sxs-lookup"><span data-stu-id="f3811-203">460798</span></span>|
    |<span data-ttu-id="f3811-204">.NET Framework 4.7 installé sur toutes les autres versions du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="f3811-204">.NET Framework 4.7 installed on all other Windows OS versions</span></span>|<span data-ttu-id="f3811-205">460805</span><span class="sxs-lookup"><span data-stu-id="f3811-205">460805</span></span>|
    |<span data-ttu-id="f3811-206">.NET Framework 4.7.1 installé sur Windows 10 Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="f3811-206">.NET Framework 4.7.1 installed on Windows 10 Fall Creators Update</span></span>|<span data-ttu-id="f3811-207">461308</span><span class="sxs-lookup"><span data-stu-id="f3811-207">461308</span></span>|
    |<span data-ttu-id="f3811-208">.NET Framework 4.7.1 installé sur toutes les autres versions du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="f3811-208">.NET Framework 4.7.1 installed on all other Windows OS versions</span></span>|<span data-ttu-id="f3811-209">461310</span><span class="sxs-lookup"><span data-stu-id="f3811-209">461310</span></span>|
    |<span data-ttu-id="f3811-210">.NET Framework 4.7.2 installé sur Windows 10 avec la mise à jour d’octobre 2018</span><span class="sxs-lookup"><span data-stu-id="f3811-210">.NET Framework 4.7.2 installed on Windows 10 October 2018 Update</span></span>|<span data-ttu-id="f3811-211">461814</span><span class="sxs-lookup"><span data-stu-id="f3811-211">461814</span></span>|
    |<span data-ttu-id="f3811-212">.NET Framework 4.7.2 installé sur Windows 10 avec la mise à jour d’avril 2018</span><span class="sxs-lookup"><span data-stu-id="f3811-212">.NET Framework 4.7.2 installed on Windows 10 April 2018 Update</span></span>|<span data-ttu-id="f3811-213">461808</span><span class="sxs-lookup"><span data-stu-id="f3811-213">461808</span></span>|
    |<span data-ttu-id="f3811-214">.NET Framework 4.7.2 installé sur Windows 10 Fall Creators Update et les versions antérieures du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f3811-214">.NET Framework 4.7.2 installed on Windows 10 Fall Creators Update and earlier OS versions</span></span>|<span data-ttu-id="f3811-215">461814</span><span class="sxs-lookup"><span data-stu-id="f3811-215">461814</span></span>|
    
     <span data-ttu-id="f3811-216">L’exemple suivant vérifie la valeur `Release` dans le Registre pour déterminer si le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] ou version ultérieure du .NET Framework est installée.</span><span class="sxs-lookup"><span data-stu-id="f3811-216">The following example checks the `Release` value in the registry to determine whether the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or a later version of the .NET Framework is installed.</span></span>

     [!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
     [!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

     <span data-ttu-id="f3811-217">Cet exemple suit la pratique recommandée concernant la vérification de version :</span><span class="sxs-lookup"><span data-stu-id="f3811-217">This example follows the recommended practice for version checking:</span></span>

    - <span data-ttu-id="f3811-218">Il vérifie si la valeur de l’entrée `Release` est *supérieure ou égale à* la valeur des clés de version connues.</span><span class="sxs-lookup"><span data-stu-id="f3811-218">It checks whether the value of the `Release` entry is *greater than or equal to* the value of the known release keys.</span></span>

    - <span data-ttu-id="f3811-219">Il effectue sa vérification en partant de la version la plus récente vers la version la plus ancienne.</span><span class="sxs-lookup"><span data-stu-id="f3811-219">It checks in order from most recent version to earliest version.</span></span>

<a name="ps_a"></a> 
## <a name="to-check-for-a-minimum-required-net-framework-version-by-querying-the-registry-in-powershell-net-framework-45-and-later"></a><span data-ttu-id="f3811-220">Pour rechercher une version minimale requise du .NET Framework en interrogeant le Registre dans PowerShell (.NET Framework 4.5 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="f3811-220">To check for a minimum-required .NET Framework version by querying the registry in PowerShell (.NET Framework 4.5 and later)</span></span>

- <span data-ttu-id="f3811-221">L’exemple suivant vérifie la valeur du mot clé `Release` pour déterminer si .NET Framework 4.6.2 ou version ultérieure est installé, indépendamment de la version du système d’exploitation Windows (retourne `True` si la condition est vérifiée, `False` dans le cas contraire).</span><span class="sxs-lookup"><span data-stu-id="f3811-221">The following example checks the value of the `Release` keyword to determine whether .NET Framework 4.6.2 or higher is installed, regardless of Windows OS version (returning `True` if it is and `False` otherwise).</span></span>

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    <span data-ttu-id="f3811-222">Vous pouvez remplacer `394802` dans l’exemple précédent par une autre valeur du tableau suivant pour rechercher une autre version minimale requise du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f3811-222">You can replace `394802` in the previous example with another value from the following table to check for a different minimum-required .NET Framework version.</span></span>
  
    |<span data-ttu-id="f3811-223">Version</span><span class="sxs-lookup"><span data-stu-id="f3811-223">Version</span></span>|<span data-ttu-id="f3811-224">Valeur minimale du paramètre DWORD Release</span><span class="sxs-lookup"><span data-stu-id="f3811-224">Minimum value of the Release DWORD</span></span>|
    |-------------|--------------------------------|
    |<span data-ttu-id="f3811-225">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="f3811-225">.NET Framework 4.5</span></span>|<span data-ttu-id="f3811-226">378389</span><span class="sxs-lookup"><span data-stu-id="f3811-226">378389</span></span>|
    |<span data-ttu-id="f3811-227">.NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="f3811-227">.NET Framework 4.5.1</span></span>|<span data-ttu-id="f3811-228">378675</span><span class="sxs-lookup"><span data-stu-id="f3811-228">378675</span></span>|
    |<span data-ttu-id="f3811-229">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="f3811-229">.NET Framework 4.5.2</span></span>|<span data-ttu-id="f3811-230">379893</span><span class="sxs-lookup"><span data-stu-id="f3811-230">379893</span></span>|
    |[!INCLUDE[net_v46](../../../includes/net-v46-md.md)]|<span data-ttu-id="f3811-231">393295</span><span class="sxs-lookup"><span data-stu-id="f3811-231">393295</span></span>|
    |[!INCLUDE[net_v461](../../../includes/net-v461-md.md)]|<span data-ttu-id="f3811-232">394254</span><span class="sxs-lookup"><span data-stu-id="f3811-232">394254</span></span>|
    |[!INCLUDE[net_v462](../../../includes/net-v462-md.md)]|<span data-ttu-id="f3811-233">394802</span><span class="sxs-lookup"><span data-stu-id="f3811-233">394802</span></span>|
    |<span data-ttu-id="f3811-234">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="f3811-234">.NET Framework 4.7</span></span>|<span data-ttu-id="f3811-235">460798</span><span class="sxs-lookup"><span data-stu-id="f3811-235">460798</span></span>|
    |<span data-ttu-id="f3811-236">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="f3811-236">.NET Framework 4.7.1</span></span>|<span data-ttu-id="f3811-237">461308</span><span class="sxs-lookup"><span data-stu-id="f3811-237">461308</span></span>|
    |<span data-ttu-id="f3811-238">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f3811-238">.NET Framework 4.7.2</span></span>|<span data-ttu-id="f3811-239">461808</span><span class="sxs-lookup"><span data-stu-id="f3811-239">461808</span></span>|

<a name="clr_a"></a> 
## <a name="to-find-the-current-runtime-version-by-using-the-clrver-tool"></a><span data-ttu-id="f3811-240">Pour déterminer la version actuelle du runtime à l'aide de l'outil Clrver</span><span class="sxs-lookup"><span data-stu-id="f3811-240">To find the current runtime version by using the Clrver tool</span></span>

- <span data-ttu-id="f3811-241">Utilisez l'outil de version CLR (Clrver.exe) pour déterminer quelles versions du CLR (Common Language Runtime) sont installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3811-241">Use the CLR Version Tool (Clrver.exe) to determine which versions of the common language runtime are installed on a computer.</span></span>

     <span data-ttu-id="f3811-242">À partir d’une invite de commandes développeur pour Visual Studio, entrez `clrver`.</span><span class="sxs-lookup"><span data-stu-id="f3811-242">From a Developer Command Prompt for Visual Studio, enter `clrver`.</span></span> <span data-ttu-id="f3811-243">Cette commande produit un résultat similaire au suivant :</span><span class="sxs-lookup"><span data-stu-id="f3811-243">This command produces output similar to the following:</span></span>

    ```
    Versions installed on the machine:
    v2.0.50727
    v4.0.30319
    ```

     <span data-ttu-id="f3811-244">Pour plus d’informations sur l’utilisation de cet outil, consultez [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span><span class="sxs-lookup"><span data-stu-id="f3811-244">For more information about using this tool, see [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span></span>

<a name="clr_b"></a> 
## <a name="to-find-the-current-runtime-version-by-querying-the-environment-class-in-code"></a><span data-ttu-id="f3811-245">Pour rechercher la version actuelle du runtime en interrogeant la classe Environment dans le code</span><span class="sxs-lookup"><span data-stu-id="f3811-245">To find the current runtime version by querying the Environment class in code</span></span>

- <span data-ttu-id="f3811-246">Interrogez la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour récupérer un objet <xref:System.Version> identifiant la version du runtime qui exécute actuellement le code.</span><span class="sxs-lookup"><span data-stu-id="f3811-246">Query the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to retrieve a <xref:System.Version> object that identifies the version of the runtime that is currently executing the code.</span></span> <span data-ttu-id="f3811-247">Vous pouvez utiliser la propriété <xref:System.Version.Major%2A?displayProperty=nameWithType> pour obtenir l'identificateur de la version principale (par exemple, « 4 » pour la version 4,0), la propriété <xref:System.Version.Minor%2A?displayProperty=nameWithType> pour obtenir l'identificateur de la version secondaire (par exemple, « 0 » pour la version 4,0) ou la méthode <xref:System.Object.ToString%2A?displayProperty=nameWithType> pour obtenir la chaîne de version entière (par exemple, « 4.0.30319.18010 », comme indiqué dans le code suivant).</span><span class="sxs-lookup"><span data-stu-id="f3811-247">You can use the <xref:System.Version.Major%2A?displayProperty=nameWithType> property to get the major release identifier (for example, "4" for version 4.0), the <xref:System.Version.Minor%2A?displayProperty=nameWithType> property to get the minor release identifier (for example, "0" for version 4.0), or the <xref:System.Object.ToString%2A?displayProperty=nameWithType> method to get the entire version string (for example, "4.0.30319.18010", as shown in the following code).</span></span> <span data-ttu-id="f3811-248">Cette propriété retourne une valeur unique qui reflète la version du runtime exécutant actuellement le code. Elle ne retourne pas les versions d'assembly ou les autres versions du runtime qui ont pu être installées sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3811-248">This property returns a single value that reflects the version of the runtime that is currently executing the code; it does not return assembly versions or other versions of the runtime that may have been installed on the computer.</span></span>

     <span data-ttu-id="f3811-249">Pour .NET Framework versions 4, 4.5, 4.5.1 et 4.5.2, la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> retourne un objet <xref:System.Version> dont la représentation sous forme de chaîne se présente sous la forme `4.0.30319.xxxxx`.</span><span class="sxs-lookup"><span data-stu-id="f3811-249">For the .NET Framework Versions 4, 4.5, 4.5.1, and 4.5.2, the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property returns a <xref:System.Version> object whose string representation has the form `4.0.30319.xxxxx`.</span></span> <span data-ttu-id="f3811-250">Pour .NET Framework 4.6 et versions ultérieures, le format est `4.0.30319.42000`.</span><span class="sxs-lookup"><span data-stu-id="f3811-250">For the .NET Framework 4.6 and later, it has the form `4.0.30319.42000`.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f3811-251">Pour [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] et versions ultérieures, nous déconseillons l’utilisation de la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour détecter la version du runtime.</span><span class="sxs-lookup"><span data-stu-id="f3811-251">For the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] and later, we do not recommend using the  <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to detect the version of the runtime.</span></span> <span data-ttu-id="f3811-252">Nous recommandons plutôt d’interroger le Registre, comme décrit dans la section [Pour déterminer les versions de .NET Framework en interrogeant le Registre à l’aide de code (.NET Framework 4.5 et ultérieur)](#net_d), plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f3811-252">Instead, we recommend that you query the registry, as described in the [To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)](#net_d) section earlier in this article.</span></span>

     <span data-ttu-id="f3811-253">Voici un exemple illustrant l'interrogation de la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour obtenir les informations de version du runtime :</span><span class="sxs-lookup"><span data-stu-id="f3811-253">Here's an example of querying the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property for runtime version information:</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

     <span data-ttu-id="f3811-254">Cet exemple produit un résultat semblable au suivant :</span><span class="sxs-lookup"><span data-stu-id="f3811-254">The example produces output that's similar to the following:</span></span>

    ```
    Version: 4.0.30319.18010
    ```

## <a name="see-also"></a><span data-ttu-id="f3811-255">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3811-255">See also</span></span>

- [<span data-ttu-id="f3811-256">Guide pratique pour Déterminer les mises à jour .NET Framework installées</span><span class="sxs-lookup"><span data-stu-id="f3811-256">How to: Determine Which .NET Framework Updates Are Installed</span></span>](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)
- [<span data-ttu-id="f3811-257">Installer le .NET Framework pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="f3811-257">Install the .NET Framework for developers</span></span>](../../../docs/framework/install/guide-for-developers.md)
- [<span data-ttu-id="f3811-258">Versions et dépendances</span><span class="sxs-lookup"><span data-stu-id="f3811-258">Versions and Dependencies</span></span>](~/docs/framework/migration-guide/versions-and-dependencies.md)
