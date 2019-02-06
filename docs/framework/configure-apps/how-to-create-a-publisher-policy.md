---
title: 'Procédure : Créer une stratégie d’éditeur'
ms.date: 03/30/2017
helpviewer_keywords:
- publisher policy assembly
- publisher policy files
- GAC (global assembly cache), publisher policy assembly
- global assembly cache, publisher policy assembly
ms.assetid: 8046bc5d-2fa9-4277-8a5e-6dcc96c281d9
ms.openlocfilehash: b98d3ef62fc9dda48920d32fed6f6acf797334d6
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758987"
---
# <a name="how-to-create-a-publisher-policy"></a><span data-ttu-id="be4ed-102">Procédure : Créer une stratégie d’éditeur</span><span class="sxs-lookup"><span data-stu-id="be4ed-102">How to: Create a Publisher Policy</span></span>
<span data-ttu-id="be4ed-103">Les fournisseurs d’assemblys peuvent indiquer que les applications doivent utiliser une version plus récente d’un assembly en incluant un fichier de stratégie de serveur de publication avec l’assembly mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="be4ed-103">Vendors of assemblies can state that applications should use a newer version of an assembly by including a publisher policy file with the upgraded assembly.</span></span> <span data-ttu-id="be4ed-104">Le fichier de stratégie d’éditeur spécifie la redirection d’assembly et les paramètres de base de code et utilise le même format qu’un fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="be4ed-104">The publisher policy file specifies assembly redirection and code base settings, and uses the same format as an application configuration file.</span></span> <span data-ttu-id="be4ed-105">Le fichier de stratégie d’éditeur est compilé dans un assembly et placé dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="be4ed-105">The publisher policy file is compiled into an assembly and placed in the global assembly cache.</span></span>  
  
 <span data-ttu-id="be4ed-106">Il existe trois étapes impliquées dans la création d’une stratégie d’éditeur :</span><span class="sxs-lookup"><span data-stu-id="be4ed-106">There are three steps involved in creating a publisher policy:</span></span>  
  
1.  <span data-ttu-id="be4ed-107">Créez un fichier de stratégie de serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="be4ed-107">Create a publisher policy file.</span></span>  
  
2.  <span data-ttu-id="be4ed-108">Créer un assembly de stratégie de serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="be4ed-108">Create a publisher policy assembly.</span></span>  
  
3.  <span data-ttu-id="be4ed-109">Ajoutez l’assembly de stratégie de serveur de publication dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="be4ed-109">Add the publisher policy assembly to the global assembly cache.</span></span>  
  
 <span data-ttu-id="be4ed-110">Le schéma pour la stratégie d’éditeur est décrit dans [redirection des Versions d’Assembly](../../../docs/framework/configure-apps/redirect-assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be4ed-110">The schema for publisher policy is described in [Redirecting Assembly Versions](../../../docs/framework/configure-apps/redirect-assembly-versions.md).</span></span> <span data-ttu-id="be4ed-111">L’exemple suivant montre un serveur de publication des fichiers de stratégie qui redirige une version de `myAssembly` vers un autre.</span><span class="sxs-lookup"><span data-stu-id="be4ed-111">The following example shows a publisher policy file that redirects one version of `myAssembly` to another.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
       <dependentAssembly>  
         <assemblyIdentity name="myAssembly"  
                           publicKeyToken="32ab4ba45e0a69a1"  
                           culture="en-us" />  
         <!-- Redirecting to version 2.0.0.0 of the assembly. -->  
         <bindingRedirect oldVersion="1.0.0.0"  
                          newVersion="2.0.0.0"/>  
       </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="be4ed-112">Pour savoir comment spécifier une base de code, consultez [spécifiant l’emplacement d’un Assembly](../../../docs/framework/configure-apps/specify-assembly-location.md).</span><span class="sxs-lookup"><span data-stu-id="be4ed-112">To learn how to specify a code base, see [Specifying an Assembly's Location](../../../docs/framework/configure-apps/specify-assembly-location.md).</span></span>  
  
## <a name="creating-the-publisher-policy-assembly"></a><span data-ttu-id="be4ed-113">Création de l’Assembly de stratégie de serveur de publication</span><span class="sxs-lookup"><span data-stu-id="be4ed-113">Creating the Publisher Policy Assembly</span></span>  
 <span data-ttu-id="be4ed-114">Utilisez le [Assembly Linker (Al.exe)](../../../docs/framework/tools/al-exe-assembly-linker.md) pour créer l’assembly de stratégie de serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="be4ed-114">Use the [Assembly Linker (Al.exe)](../../../docs/framework/tools/al-exe-assembly-linker.md) to create the publisher policy assembly.</span></span>  
  
#### <a name="to-create-a-publisher-policy-assembly"></a><span data-ttu-id="be4ed-115">Pour créer un assembly de stratégie de serveur de publication</span><span class="sxs-lookup"><span data-stu-id="be4ed-115">To create a publisher policy assembly</span></span>  
  
1.  <span data-ttu-id="be4ed-116">Tapez la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="be4ed-116">Type the following command at the command prompt:</span></span>  
  
     <span data-ttu-id="be4ed-117">**al /link:** *publisherPolicyFile* **/out:** *publisherPolicyAssemblyFile* **/keyfile:** *keyPairFile* **/platform:** *processorArchitecture*</span><span class="sxs-lookup"><span data-stu-id="be4ed-117">**al /link:** *publisherPolicyFile* **/out:** *publisherPolicyAssemblyFile* **/keyfile:** *keyPairFile* **/platform:** *processorArchitecture*</span></span>  
  
     <span data-ttu-id="be4ed-118">Dans cette commande :</span><span class="sxs-lookup"><span data-stu-id="be4ed-118">In this command:</span></span>  
  
    -   <span data-ttu-id="be4ed-119">Le *publisherPolicyFile* argument est le nom du fichier de stratégie de serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="be4ed-119">The *publisherPolicyFile* argument is the name of the publisher policy file.</span></span>  
  
    -   <span data-ttu-id="be4ed-120">Le *publisherPolicyAssemblyFile* argument est le nom de l’assembly de stratégie d’éditeur qui résulte de cette commande.</span><span class="sxs-lookup"><span data-stu-id="be4ed-120">The *publisherPolicyAssemblyFile* argument is the name of the publisher policy assembly that results from this command.</span></span> <span data-ttu-id="be4ed-121">Le nom de fichier d’assembly doit respecter le format :</span><span class="sxs-lookup"><span data-stu-id="be4ed-121">The assembly file name must follow the format:</span></span>  
  
         <span data-ttu-id="be4ed-122">**policy.**</span><span class="sxs-lookup"><span data-stu-id="be4ed-122">**policy.**</span></span> <span data-ttu-id="be4ed-123">*majorNumber* **.**</span><span class="sxs-lookup"><span data-stu-id="be4ed-123">*majorNumber* **.**</span></span> <span data-ttu-id="be4ed-124">*minorNumber* **.**</span><span class="sxs-lookup"><span data-stu-id="be4ed-124">*minorNumber* **.**</span></span> <span data-ttu-id="be4ed-125">*mainAssemblyName* **.dll**</span><span class="sxs-lookup"><span data-stu-id="be4ed-125">*mainAssemblyName* **.dll**</span></span>  
  
    -   <span data-ttu-id="be4ed-126">Le *keyPairFile* argument est le nom du fichier contenant la paire de clés.</span><span class="sxs-lookup"><span data-stu-id="be4ed-126">The *keyPairFile* argument is the name of the file containing the key pair.</span></span> <span data-ttu-id="be4ed-127">Vous devez signer l’assembly et l’assembly de stratégie d’éditeur avec la même paire de clés.</span><span class="sxs-lookup"><span data-stu-id="be4ed-127">You must sign the assembly and publisher policy assembly with the same key pair.</span></span>  
  
    -   <span data-ttu-id="be4ed-128">Le *processorArchitecture* argument identifie la plateforme ciblée par un assembly spécifique au processeur.</span><span class="sxs-lookup"><span data-stu-id="be4ed-128">The *processorArchitecture* argument identifies the platform targeted by a processor-specific assembly.</span></span>  
  
        > [!NOTE]
        >  <span data-ttu-id="be4ed-129">La possibilité de cibler une architecture de processeur spécifique est une nouveauté dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="be4ed-129">The ability to target a specific processor architecture is new in the .NET Framework version 2.0.</span></span>  
  
     <span data-ttu-id="be4ed-130">La commande suivante crée un assembly de stratégie d’éditeur appelé `policy.1.0.myAssembly` à partir d’un fichier de stratégie de serveur de publication nommé `pub.config`, assigne un nom fort à l’assembly à l’aide de la paire de clés dans le `sgKey.snk` de fichiers et spécifie que l’assembly cible la x86 architecture de processeur.</span><span class="sxs-lookup"><span data-stu-id="be4ed-130">The following command creates a publisher policy assembly called `policy.1.0.myAssembly` from a publisher policy file called `pub.config`, assigns a strong name to the assembly using the key pair in the `sgKey.snk` file, and specifies that the assembly targets the x86 processor architecture.</span></span>  
  
    ```  
    al /link:pub.config /out:policy.1.0.myAssembly.dll /keyfile:sgKey.snk /platform:x86  
    ```  
  
     <span data-ttu-id="be4ed-131">L’assembly de stratégie de serveur de publication doit correspondre à l’architecture de processeur de l’assembly qui s’applique à.</span><span class="sxs-lookup"><span data-stu-id="be4ed-131">The publisher policy assembly must match the processor architecture of the assembly that it applies to.</span></span> <span data-ttu-id="be4ed-132">Par conséquent, si l’assembly comporte un <xref:System.Reflection.AssemblyName.ProcessorArchitecture%2A> valeur <xref:System.Reflection.ProcessorArchitecture.MSIL>, l’assembly de stratégie d’éditeur pour cet assembly doit être créé avec `/platform:anycpu`.</span><span class="sxs-lookup"><span data-stu-id="be4ed-132">Thus, if your assembly has a <xref:System.Reflection.AssemblyName.ProcessorArchitecture%2A> value of <xref:System.Reflection.ProcessorArchitecture.MSIL>, the publisher policy assembly for that assembly must be created with `/platform:anycpu`.</span></span> <span data-ttu-id="be4ed-133">Vous devez fournir un distinct assembly de stratégie d’éditeur pour chaque assembly spécifique au processeur.</span><span class="sxs-lookup"><span data-stu-id="be4ed-133">You must provide a separate publisher policy assembly for each processor-specific assembly.</span></span>  
  
     <span data-ttu-id="be4ed-134">Une conséquence de cette règle est que, pour modifier l’architecture de processeur pour un assembly, vous devez modifier le composant majeur ou mineurs du numéro de version, afin que vous pouvez fournir un nouvel assembly de stratégie de serveur de publication avec l’architecture de processeur correcte.</span><span class="sxs-lookup"><span data-stu-id="be4ed-134">A consequence of this rule is that in order to change the processor architecture for an assembly, you must change the major or minor component of the version number, so that you can supply a new publisher policy assembly with the correct processor architecture.</span></span> <span data-ttu-id="be4ed-135">L’ancien assembly de stratégie de serveur de publication ne peut pas traiter votre assembly une fois que votre assembly dispose d’une architecture de processeur différente.</span><span class="sxs-lookup"><span data-stu-id="be4ed-135">The old publisher policy assembly cannot service your assembly once your assembly has a different processor architecture.</span></span>  
  
     <span data-ttu-id="be4ed-136">Une autre conséquence est que l’éditeur de liens version 2.0 ne peut pas être utilisé pour créer un assembly de stratégie de serveur de publication pour un assembly compilé à l’aide de versions antérieures du .NET Framework, car elle spécifie toujours architecture de processeur.</span><span class="sxs-lookup"><span data-stu-id="be4ed-136">Another consequence is that the version 2.0 linker cannot be used to create a publisher policy assembly for an assembly compiled using earlier versions of the .NET Framework, because it always specifies processor architecture.</span></span>  
  
## <a name="adding-the-publisher-policy-assembly-to-the-global-assembly-cache"></a><span data-ttu-id="be4ed-137">Ajout de l’Assembly de stratégie de serveur de publication dans le Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="be4ed-137">Adding the Publisher Policy Assembly to the Global Assembly Cache</span></span>  
 <span data-ttu-id="be4ed-138">Utilisez le [outil Global Assembly Cache (Gacutil.exe)](../../../docs/framework/tools/gacutil-exe-gac-tool.md) pour ajouter l’assembly de stratégie de serveur de publication dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="be4ed-138">Use the [Global Assembly Cache tool (Gacutil.exe)](../../../docs/framework/tools/gacutil-exe-gac-tool.md) to add the publisher policy assembly to the global assembly cache.</span></span>  
  
#### <a name="to-add-the-publisher-policy-assembly-to-the-global-assembly-cache"></a><span data-ttu-id="be4ed-139">Pour ajouter l’assembly de stratégie de serveur de publication dans le global assembly cache</span><span class="sxs-lookup"><span data-stu-id="be4ed-139">To add the publisher policy assembly to the global assembly cache</span></span>  
  
1.  <span data-ttu-id="be4ed-140">Tapez la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="be4ed-140">Type the following command at the command prompt:</span></span>  
  
     <span data-ttu-id="be4ed-141">**gacutil /i**  *publisherPolicyAssemblyFile*</span><span class="sxs-lookup"><span data-stu-id="be4ed-141">**gacutil /i**  *publisherPolicyAssemblyFile*</span></span>  
  
     <span data-ttu-id="be4ed-142">La commande suivante ajoute `policy.1.0.myAssembly.dll` dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="be4ed-142">The following command adds `policy.1.0.myAssembly.dll` to the global assembly cache.</span></span>  
  
    ```  
    gacutil /i policy.1.0.myAssembly.dll  
    ```  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="be4ed-143">L’assembly de stratégie de serveur de publication ne peut pas être ajouté au global assembly cache, sauf si le fichier de stratégie de serveur de publication d’origine se trouve dans le même répertoire que l’assembly.</span><span class="sxs-lookup"><span data-stu-id="be4ed-143">The publisher policy assembly cannot be added to the global assembly cache unless the original publisher policy file is located in the same directory as the assembly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be4ed-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4ed-144">See also</span></span>
- [<span data-ttu-id="be4ed-145">Programmation à l’aide d’assemblys</span><span class="sxs-lookup"><span data-stu-id="be4ed-145">Programming with Assemblies</span></span>](../../../docs/framework/app-domains/programming-with-assemblies.md)
- [<span data-ttu-id="be4ed-146">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="be4ed-146">How the Runtime Locates Assemblies</span></span>](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [<span data-ttu-id="be4ed-147">Configuration d’applications à l’aide de fichiers de Configuration</span><span class="sxs-lookup"><span data-stu-id="be4ed-147">Configuring Apps by using Configuration Files</span></span>](../../../docs/framework/configure-apps/index.md)
- [<span data-ttu-id="be4ed-148">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="be4ed-148">Runtime Settings Schema</span></span>](../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="be4ed-149">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="be4ed-149">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="be4ed-150">Redirection des versions d'assemblys</span><span class="sxs-lookup"><span data-stu-id="be4ed-150">Redirecting Assembly Versions</span></span>](../../../docs/framework/configure-apps/redirect-assembly-versions.md)
