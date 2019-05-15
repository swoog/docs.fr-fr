---
title: Regsvcs.exe (outil .NET Services Installation)
ms.date: 03/30/2017
helpviewer_keywords:
- Regsvcs.exe
- .NET Services Installation tool
- loading assemblies
- assemblies [.NET Framework], registering
- type libraries
- registering assemblies
ms.assetid: 5220fe58-5aaf-4e8e-8bc3-b78c63025804
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0dc05294ae762b4f896bb7f514df102c1f948fe0
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64623406"
---
# <a name="regsvcsexe-net-services-installation-tool"></a><span data-ttu-id="4e43a-102">Regsvcs.exe (outil .NET Services Installation)</span><span class="sxs-lookup"><span data-stu-id="4e43a-102">Regsvcs.exe (.NET Services Installation Tool)</span></span>
<span data-ttu-id="4e43a-103">L'outil .NET Services Installation (Installation des services .NET) effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e43a-103">The .NET Services Installation tool performs the following actions:</span></span>  
  
- <span data-ttu-id="4e43a-104">Il charge et inscrit un assembly ;</span><span class="sxs-lookup"><span data-stu-id="4e43a-104">Loads and registers an assembly.</span></span>  
  
- <span data-ttu-id="4e43a-105">Il génère, inscrit et installe une bibliothèque de types dans l'application COM+ spécifiée ;</span><span class="sxs-lookup"><span data-stu-id="4e43a-105">Generates, registers, and installs a type library into a specified COM+ application.</span></span>  
  
- <span data-ttu-id="4e43a-106">Il configure les services que vous avez ajoutés à votre classe par programmation.</span><span class="sxs-lookup"><span data-stu-id="4e43a-106">Configures services that you have added programmatically to your class.</span></span>  
  
 <span data-ttu-id="4e43a-107">Pour exécuter l’outil, utilisez l’invite de commandes développeur pour Visual Studio (ou l’invite de commandes Visual Studio dans Windows 7).</span><span class="sxs-lookup"><span data-stu-id="4e43a-107">To run the tool, use the Developer Command Prompt for Visual Studio (or the Visual Studio Command Prompt in Windows 7).</span></span> <span data-ttu-id="4e43a-108">Pour plus d'informations, consultez [Invites de commandes](../../../docs/framework/tools/developer-command-prompt-for-vs.md).</span><span class="sxs-lookup"><span data-stu-id="4e43a-108">For more information, see [Command Prompts](../../../docs/framework/tools/developer-command-prompt-for-vs.md).</span></span>  
  
 <span data-ttu-id="4e43a-109">À l'invite de commandes, tapez le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="4e43a-109">At the command prompt, type the following:</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e43a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e43a-110">Syntax</span></span>  
  
```  
      regsvcs [/c | /fc | /u] [/tlb:typeLibraryFile] [/extlb]  
[/reconfig] [/componly] [/appname:applicationName]  
[/nologo] [/quiet]assemblyFile.dll   
```  
  
## <a name="parameters"></a><span data-ttu-id="4e43a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e43a-111">Parameters</span></span>  
  
|<span data-ttu-id="4e43a-112">Argument</span><span class="sxs-lookup"><span data-stu-id="4e43a-112">Argument</span></span>|<span data-ttu-id="4e43a-113">Description</span><span class="sxs-lookup"><span data-stu-id="4e43a-113">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="4e43a-114">*assemblyFile.dll*</span><span class="sxs-lookup"><span data-stu-id="4e43a-114">*assemblyFile.dll*</span></span>|<span data-ttu-id="4e43a-115">Fichier d'assembly source.</span><span class="sxs-lookup"><span data-stu-id="4e43a-115">The source assembly file.</span></span> <span data-ttu-id="4e43a-116">L'assembly doit être signé avec un nom fort.</span><span class="sxs-lookup"><span data-stu-id="4e43a-116">The assembly must be signed with a strong name.</span></span> <span data-ttu-id="4e43a-117">Pour plus d’informations, consultez [Signature d’un assembly avec un nom fort](../../../docs/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span><span class="sxs-lookup"><span data-stu-id="4e43a-117">For more information, see [Signing an Assembly with a Strong Name](../../../docs/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span>|  
  
|<span data-ttu-id="4e43a-118">Option</span><span class="sxs-lookup"><span data-stu-id="4e43a-118">Option</span></span>|<span data-ttu-id="4e43a-119">Description</span><span class="sxs-lookup"><span data-stu-id="4e43a-119">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="4e43a-120">**/appdir:** *path*</span><span class="sxs-lookup"><span data-stu-id="4e43a-120">**/appdir:** *path*</span></span>|<span data-ttu-id="4e43a-121">Spécifie le répertoire racine de l'application.</span><span class="sxs-lookup"><span data-stu-id="4e43a-121">Specifies the root directory of the application.</span></span>|  
|<span data-ttu-id="4e43a-122">**/appname:** *applicationName*</span><span class="sxs-lookup"><span data-stu-id="4e43a-122">**/appname:** *applicationName*</span></span>|<span data-ttu-id="4e43a-123">Spécifie le nom de l'application COM+ à rechercher ou à créer.</span><span class="sxs-lookup"><span data-stu-id="4e43a-123">Specifies the name of the COM+ application to either find or create.</span></span>|  
|<span data-ttu-id="4e43a-124">**/c**</span><span class="sxs-lookup"><span data-stu-id="4e43a-124">**/c**</span></span>|<span data-ttu-id="4e43a-125">Crée l'application cible.</span><span class="sxs-lookup"><span data-stu-id="4e43a-125">Creates the target application.</span></span>|  
|<span data-ttu-id="4e43a-126">**/componly**</span><span class="sxs-lookup"><span data-stu-id="4e43a-126">**/componly**</span></span>|<span data-ttu-id="4e43a-127">Configure uniquement les composants ; ignore les méthodes et les interfaces.</span><span class="sxs-lookup"><span data-stu-id="4e43a-127">Configures components only; ignores methods and interfaces.</span></span>|  
|<span data-ttu-id="4e43a-128">**/exapp**</span><span class="sxs-lookup"><span data-stu-id="4e43a-128">**/exapp**</span></span>|<span data-ttu-id="4e43a-129">Spécifie à l'outil qu'il doit attendre une application existante.</span><span class="sxs-lookup"><span data-stu-id="4e43a-129">Specifies to the tool to expect an existing application.</span></span>|  
|<span data-ttu-id="4e43a-130">**/extlb**</span><span class="sxs-lookup"><span data-stu-id="4e43a-130">**/extlb**</span></span>|<span data-ttu-id="4e43a-131">Utilise une bibliothèque de types existante.</span><span class="sxs-lookup"><span data-stu-id="4e43a-131">Uses an existing type library.</span></span>|  
|<span data-ttu-id="4e43a-132">**/fc**</span><span class="sxs-lookup"><span data-stu-id="4e43a-132">**/fc**</span></span>|<span data-ttu-id="4e43a-133">Recherche ou crée l'application cible.</span><span class="sxs-lookup"><span data-stu-id="4e43a-133">Finds or creates the target application.</span></span>|  
|<span data-ttu-id="4e43a-134">**/help**</span><span class="sxs-lookup"><span data-stu-id="4e43a-134">**/help**</span></span>|<span data-ttu-id="4e43a-135">Affiche la syntaxe et les options de commande de l'outil.</span><span class="sxs-lookup"><span data-stu-id="4e43a-135">Displays command syntax and options for the tool.</span></span>|  
|<span data-ttu-id="4e43a-136">**/noreconfig**</span><span class="sxs-lookup"><span data-stu-id="4e43a-136">**/noreconfig**</span></span>|<span data-ttu-id="4e43a-137">Ne reconfigure pas une application cible existante.</span><span class="sxs-lookup"><span data-stu-id="4e43a-137">Does not reconfigure an existing target application.</span></span>|  
|<span data-ttu-id="4e43a-138">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="4e43a-138">**/nologo**</span></span>|<span data-ttu-id="4e43a-139">Supprime l'affichage de la bannière de démarrage Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e43a-139">Suppresses the Microsoft startup banner display.</span></span>|  
|<span data-ttu-id="4e43a-140">**/parname:** *name*</span><span class="sxs-lookup"><span data-stu-id="4e43a-140">**/parname:** *name*</span></span>|<span data-ttu-id="4e43a-141">Spécifie le nom ou l'identificateur de l'application COM+ à rechercher ou à créer.</span><span class="sxs-lookup"><span data-stu-id="4e43a-141">Specifies the name or id of the COM+ application to either find or create.</span></span>|  
|<span data-ttu-id="4e43a-142">**/reconfig**</span><span class="sxs-lookup"><span data-stu-id="4e43a-142">**/reconfig**</span></span>|<span data-ttu-id="4e43a-143">Reconfigure une application cible existante.</span><span class="sxs-lookup"><span data-stu-id="4e43a-143">Reconfigures an existing target application.</span></span> <span data-ttu-id="4e43a-144">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e43a-144">This is the default.</span></span>|  
|<span data-ttu-id="4e43a-145">**/tlb:** *typelibraryfile*</span><span class="sxs-lookup"><span data-stu-id="4e43a-145">**/tlb:** *typelibraryfile*</span></span>|<span data-ttu-id="4e43a-146">Spécifie le fichier bibliothèque de types à installer.</span><span class="sxs-lookup"><span data-stu-id="4e43a-146">Specifies the type library file to install.</span></span>|  
|<span data-ttu-id="4e43a-147">**/u**</span><span class="sxs-lookup"><span data-stu-id="4e43a-147">**/u**</span></span>|<span data-ttu-id="4e43a-148">Désinstalle l'application cible.</span><span class="sxs-lookup"><span data-stu-id="4e43a-148">Uninstalls the target application.</span></span>|  
|<span data-ttu-id="4e43a-149">**/quiet**</span><span class="sxs-lookup"><span data-stu-id="4e43a-149">**/quiet**</span></span>|<span data-ttu-id="4e43a-150">Spécifie le mode silencieux ; supprime le logo et l'affichage des messages de réussite.</span><span class="sxs-lookup"><span data-stu-id="4e43a-150">Specifies quiet mode; suppresses the logo and success message display.</span></span>|  
|<span data-ttu-id="4e43a-151">**/?**</span><span class="sxs-lookup"><span data-stu-id="4e43a-151">**/?**</span></span>|<span data-ttu-id="4e43a-152">Affiche la syntaxe et les options de commande de l'outil.</span><span class="sxs-lookup"><span data-stu-id="4e43a-152">Displays command syntax and options for the tool.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4e43a-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e43a-153">Remarks</span></span>  
 <span data-ttu-id="4e43a-154">Regsvcs.exe nécessite un fichier d’assembly source spécifié par *assemblyFile.dll*.</span><span class="sxs-lookup"><span data-stu-id="4e43a-154">Regsvcs.exe requires a source assembly file specified by *assemblyFile.dll*.</span></span> <span data-ttu-id="4e43a-155">Cet assembly doit être signé avec un nom fort.</span><span class="sxs-lookup"><span data-stu-id="4e43a-155">This assembly must be signed with a strong name.</span></span> <span data-ttu-id="4e43a-156">Pour plus d’informations sur la signature avec un nom fort, consultez [Signature d’un assembly avec un nom fort](../../../docs/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span><span class="sxs-lookup"><span data-stu-id="4e43a-156">For more information on strong name signing, see [Signing an Assembly with a Strong Name](../../../docs/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span> <span data-ttu-id="4e43a-157">Le nom de l'application cible et le nom du fichier bibliothèque de types sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="4e43a-157">The names of the target application and the type library file are optional.</span></span> <span data-ttu-id="4e43a-158">L’argument *applicationName* peut être généré à partir du fichier d’assembly source et sera créé par Regsvcs.exe, s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="4e43a-158">The *applicationName* argument can be generated from the source assembly file and will be created by Regsvcs.exe, if it does not already exist.</span></span> <span data-ttu-id="4e43a-159">L’argument *typelibraryfile* peut spécifier un nom de bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4e43a-159">The *typelibraryfile* argument can specify a type library name.</span></span> <span data-ttu-id="4e43a-160">Si vous ne spécifiez pas de nom de bibliothèque de types, Regsvcs.exe utilise alors par défaut le nom de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="4e43a-160">If you do not specify a type library name, Regsvcs.exe uses the assembly name as the default.</span></span>  
  
 <span data-ttu-id="4e43a-161">Quand Regsvcs.exe inscrit les méthodes d’un composant, il est soumis aux [demandes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/9kc0c6st(v=vs.100)) et aux [demandes de liaison](../../../docs/framework/misc/link-demands.md) sur ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4e43a-161">When Regsvcs.exe registers a component's methods, it is subject to the [demands](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/9kc0c6st(v=vs.100)) and [link demands](../../../docs/framework/misc/link-demands.md) on those methods.</span></span> <span data-ttu-id="4e43a-162">Étant donné que l'outil s'exécute dans un environnement de niveau de confiance total, la plupart des demandes d'autorisation aboutissent.</span><span class="sxs-lookup"><span data-stu-id="4e43a-162">Because the tool executes in a fully-trusted environment, most demands for a permission succeed.</span></span> <span data-ttu-id="4e43a-163">Toutefois, Regsvcs.exe ne peut pas inscrire de composants avec des méthodes protégées par une demande ou une demande de liaison pour les autorisations <xref:System.Security.Permissions.StrongNameIdentityPermission> ou <xref:System.Security.Permissions.PublisherIdentityPermission>.</span><span class="sxs-lookup"><span data-stu-id="4e43a-163">However, Regsvcs.exe cannot register components with methods protected by a demand or link demand for the <xref:System.Security.Permissions.StrongNameIdentityPermission> or the <xref:System.Security.Permissions.PublisherIdentityPermission>.</span></span>  
  
 <span data-ttu-id="4e43a-164">Vous devez détenir des privilèges d'administrateur sur l'ordinateur local pour utiliser Regsvcs.exe.</span><span class="sxs-lookup"><span data-stu-id="4e43a-164">You must have administrative privileges on the local computer to use Regsvcs.exe.</span></span>  
  
 <span data-ttu-id="4e43a-165">Si Regsvcs.exe échoue tandis qu'il effectue l'une de ces actions, il affiche les messages d'erreur correspondants.</span><span class="sxs-lookup"><span data-stu-id="4e43a-165">If Regsvcs.exe fails while performing any of these actions, it displays corresponding error messages.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="4e43a-166">Exemples</span><span class="sxs-lookup"><span data-stu-id="4e43a-166">Examples</span></span>  
 <span data-ttu-id="4e43a-167">La commande suivante ajoute toutes les classes publiques figurant dans `myTest.dll` à `myTargetApp` (une application COM+ existante) et génère la bibliothèque de types `myTest.tlb`.</span><span class="sxs-lookup"><span data-stu-id="4e43a-167">The following command adds all public classes contained in `myTest.dll` to `myTargetApp` (an existing COM+ application) and produces the `myTest.tlb` type library.</span></span>  
  
```  
regsvcs /appname:myTargetApp myTest.dll  
```  
  
 <span data-ttu-id="4e43a-168">La commande suivante ajoute toutes les classes publiques figurant dans `myTest.dll` à `myTargetApp` (une application COM+ existante) et génère la bibliothèque de types `newTest.tlb`.</span><span class="sxs-lookup"><span data-stu-id="4e43a-168">The following command adds all public classes contained in `myTest.dll` to `myTargetApp` (an existing COM+ application) and produces the `newTest.tlb` type library.</span></span>  
  
```  
regsvcs /appname:myTargetApp /tlb:newTest.tlb myTest.dll  
```  
  
## <a name="see-also"></a><span data-ttu-id="4e43a-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e43a-169">See also</span></span>

- [<span data-ttu-id="4e43a-170">Outils</span><span class="sxs-lookup"><span data-stu-id="4e43a-170">Tools</span></span>](../../../docs/framework/tools/index.md)
- [<span data-ttu-id="4e43a-171">Guide pratique pour signer un assembly avec un nom fort</span><span class="sxs-lookup"><span data-stu-id="4e43a-171">How to: Sign an Assembly with a Strong Name</span></span>](../../../docs/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)
- [<span data-ttu-id="4e43a-172">Invites de commandes</span><span class="sxs-lookup"><span data-stu-id="4e43a-172">Command Prompts</span></span>](../../../docs/framework/tools/developer-command-prompt-for-vs.md)
