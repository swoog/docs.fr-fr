---
title: 'Procédure : signer un assembly avec un nom fort'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- strong-named assemblies, signing with strong names
- signing assemblies
- assemblies [.NET Framework], signing
- assemblies [.NET Framework], strong-named
ms.assetid: 2c30799a-a826-46b4-a25d-c584027a6c67
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5580b6d8af7319397ad7eb6416941c2be0dcdb76
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59303419"
---
# <a name="how-to-sign-an-assembly-with-a-strong-name"></a><span data-ttu-id="98470-102">Procédure : signer un assembly avec un nom fort</span><span class="sxs-lookup"><span data-stu-id="98470-102">How to: Sign an Assembly with a Strong Name</span></span>
<span data-ttu-id="98470-103">Il existe plusieurs façons de signer un assembly avec un nom fort :</span><span class="sxs-lookup"><span data-stu-id="98470-103">There are a number of ways to sign an assembly with a strong name:</span></span>  
  
-   <span data-ttu-id="98470-104">À l'aide de l'onglet **Signature** dans la boîte de dialogue **Propriétés** d'un projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="98470-104">By using the **Signing** tab in a project's **Properties** dialog box in Visual Studio.</span></span> <span data-ttu-id="98470-105">Il s'agit de la façon la plus facile et la plus pratique de signer un assembly avec un nom fort.</span><span class="sxs-lookup"><span data-stu-id="98470-105">This is the easiest and most convenient way to sign an assembly with a strong name.</span></span>  
  
-   <span data-ttu-id="98470-106">À l’aide de l’utilitaire [Assembly Linker (Al.exe)](../../../docs/framework/tools/al-exe-assembly-linker.md) pour lier un module de code .NET Framework (un fichier .netmodule) à un fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="98470-106">By using the [Assembly Linker (Al.exe)](../../../docs/framework/tools/al-exe-assembly-linker.md) to link a .NET Framework code module (a .netmodule file) with a key file.</span></span>  
  
-   <span data-ttu-id="98470-107">À l'aide d'attributs d'assembly pour insérer les informations de nom fort dans votre code.</span><span class="sxs-lookup"><span data-stu-id="98470-107">By using assembly attributes to insert the strong name information into your code.</span></span> <span data-ttu-id="98470-108">Vous pouvez utiliser l'attribut <xref:System.Reflection.AssemblyKeyFileAttribute> ou <xref:System.Reflection.AssemblyKeyNameAttribute> , selon l'emplacement du fichier de clé à utiliser.</span><span class="sxs-lookup"><span data-stu-id="98470-108">You can use either the <xref:System.Reflection.AssemblyKeyFileAttribute> or the <xref:System.Reflection.AssemblyKeyNameAttribute> attribute, depending on where the key file to be used is located.</span></span>  
  
-   <span data-ttu-id="98470-109">À l'aide des options du compilateur.</span><span class="sxs-lookup"><span data-stu-id="98470-109">By using compiler options.</span></span>  
  
 <span data-ttu-id="98470-110">Pour signer un assembly avec un nom fort, vous devez avoir une paire de clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="98470-110">You must have a cryptographic key pair to sign an assembly with a strong name.</span></span> <span data-ttu-id="98470-111">Pour plus d’informations sur la création d’une paire de clés, consultez [Guide pratique pour créer une paire de clés publique/privée](../../../docs/framework/app-domains/how-to-create-a-public-private-key-pair.md).</span><span class="sxs-lookup"><span data-stu-id="98470-111">For more information about creating a key pair, see [How to: Create a Public-Private Key Pair](../../../docs/framework/app-domains/how-to-create-a-public-private-key-pair.md).</span></span>  
  
### <a name="to-create-and-sign-an-assembly-with-a-strong-name-by-using-visual-studio"></a><span data-ttu-id="98470-112">Pour créer et signer un assembly avec un nom fort à l'aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98470-112">To create and sign an assembly with a strong name by using Visual Studio</span></span>  
  
1. <span data-ttu-id="98470-113">Dans l’ **Explorateur de solutions**, ouvrez le menu contextuel du projet et choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="98470-113">In **Solution Explorer**, open the shortcut menu for the project, and then choose **Properties**.</span></span>  
  
2. <span data-ttu-id="98470-114">Choisissez l'onglet **Signature** .</span><span class="sxs-lookup"><span data-stu-id="98470-114">Choose the **Signing** tab.</span></span>  
  
3. <span data-ttu-id="98470-115">Sélectionnez la zone **Signer l'assembly** .</span><span class="sxs-lookup"><span data-stu-id="98470-115">Select the **Sign the assembly** box.</span></span>  
  
4. <span data-ttu-id="98470-116">Dans la zone **Choisir un fichier de clé de nom fort**, choisissez **\<<Parcourir...>**, puis recherchez le fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="98470-116">In the **Choose a strong name key file** box, choose **\<Browse…>**, and then navigate to the key file.</span></span> <span data-ttu-id="98470-117">Pour créer un fichier de clé, choisissez **\<<Nouveau...>** et entrez son nom dans la boîte de dialogue **Créer une clé de nom fort**.</span><span class="sxs-lookup"><span data-stu-id="98470-117">To create a new key file, choose **\<New…>** and enter its name in the **Create Strong Name Key** dialog box.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="98470-118">Pour [différer la signature d’un assembly](../../../docs/framework/app-domains/delay-sign-assembly.md), choisissez un fichier de clé publique.</span><span class="sxs-lookup"><span data-stu-id="98470-118">In order to [delay sign an assembly](../../../docs/framework/app-domains/delay-sign-assembly.md), choose a public key file.</span></span>  
  
### <a name="to-create-and-sign-an-assembly-with-a-strong-name-by-using-the-assembly-linker"></a><span data-ttu-id="98470-119">Pour créer et signer un assembly avec un nom fort à l'aide de l'utilitaire Assembly Linker</span><span class="sxs-lookup"><span data-stu-id="98470-119">To create and sign an assembly with a strong name by using the Assembly Linker</span></span>  
  
-   <span data-ttu-id="98470-120">À l’[Invite de commandes développeur pour Visual Studio](../../../docs/framework/tools/developer-command-prompt-for-vs.md), tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="98470-120">At the [Developer Command Prompt for Visual Studio](../../../docs/framework/tools/developer-command-prompt-for-vs.md), type the following command:</span></span>  
  
     <span data-ttu-id="98470-121">**al** **/out:**\<*assemblyName*> *\<moduleName>* **/keyfile:**\<*keyfileName*></span><span class="sxs-lookup"><span data-stu-id="98470-121">**al** **/out:**\<*assemblyName*> *\<moduleName>* **/keyfile:**\<*keyfileName*></span></span>  
  
     <span data-ttu-id="98470-122">où :</span><span class="sxs-lookup"><span data-stu-id="98470-122">where:</span></span>  
  
     *<span data-ttu-id="98470-123">assemblyName</span><span class="sxs-lookup"><span data-stu-id="98470-123">assemblyName</span></span>*  
     <span data-ttu-id="98470-124">Nom de l'assembly fortement signé (un fichier .dll ou .exe) que l'utilitaire Assembly Linker émettra.</span><span class="sxs-lookup"><span data-stu-id="98470-124">The name of the strongly signed assembly (a .dll or .exe file) that Assembly Linker will emit.</span></span>  
  
     *<span data-ttu-id="98470-125">moduleName</span><span class="sxs-lookup"><span data-stu-id="98470-125">moduleName</span></span>*  
     <span data-ttu-id="98470-126">Nom d’un module de code .NET Framework (un fichier .netmodule) qui inclut un ou plusieurs types.</span><span class="sxs-lookup"><span data-stu-id="98470-126">The name of a .NET Framework code module (a .netmodule file) that includes one or more types.</span></span> <span data-ttu-id="98470-127">Vous pouvez créer un fichier .netmodule en compilant votre code avec le commutateur `/target:module` en C# ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="98470-127">You can create a .netmodule file by compiling your code with the `/target:module` switch in C# or Visual Basic.</span></span>  
  
     *<span data-ttu-id="98470-128">keyfileName</span><span class="sxs-lookup"><span data-stu-id="98470-128">keyfileName</span></span>*  
     <span data-ttu-id="98470-129">Nom du conteneur ou du fichier qui contient la paire de clés.</span><span class="sxs-lookup"><span data-stu-id="98470-129">The name of the container or file that contains the key pair.</span></span> <span data-ttu-id="98470-130">L'utilitaire Assembly Linker interprète un chemin d'accès relatif en relation avec le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="98470-130">Assembly Linker interprets a relative path in relationship to the current directory.</span></span>  
  
 <span data-ttu-id="98470-131">L'exemple suivant signe l'assembly `MyAssembly.dll` avec un nom fort à l'aide du fichier de clé `sgKey.snk`.</span><span class="sxs-lookup"><span data-stu-id="98470-131">The following example signs the assembly `MyAssembly.dll` with a strong name by using the key file `sgKey.snk`.</span></span>  
  
```  
al /out:MyAssembly.dll MyModule.netmodule /keyfile:sgKey.snk  
```  
  
 <span data-ttu-id="98470-132">Pour plus d'informations sur l'utilisation de cet outil, consultez [Assembly Linker](../../../docs/framework/tools/al-exe-assembly-linker.md).</span><span class="sxs-lookup"><span data-stu-id="98470-132">For more information about this tool, see [Assembly Linker](../../../docs/framework/tools/al-exe-assembly-linker.md).</span></span>  
  
#### <a name="to-sign-an-assembly-with-a-strong-name-by-using-attributes"></a><span data-ttu-id="98470-133">Pour signer un assembly avec un nom fort à l'aide d'attributs</span><span class="sxs-lookup"><span data-stu-id="98470-133">To sign an assembly with a strong name by using attributes</span></span>  
  
1. <span data-ttu-id="98470-134">Ajoutez l'attribut <xref:System.Reflection.AssemblyKeyFileAttribute?displayProperty=nameWithType> ou <xref:System.Reflection.AssemblyKeyNameAttribute> à votre fichier de code source et spécifiez le nom du fichier ou du conteneur qui contient la paire de clés à utiliser lors de la signature de l'assembly avec un nom fort.</span><span class="sxs-lookup"><span data-stu-id="98470-134">Add the <xref:System.Reflection.AssemblyKeyFileAttribute?displayProperty=nameWithType> or <xref:System.Reflection.AssemblyKeyNameAttribute> attribute to your source code file, and specify the name of the file or container that contains the key pair to use when signing the assembly with a strong name.</span></span>  
  
2. <span data-ttu-id="98470-135">Compilez le fichier de code source normalement.</span><span class="sxs-lookup"><span data-stu-id="98470-135">Compile the source code file normally.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="98470-136">Les compilateurs C# et Visual Basic génèrent des avertissements (CS1699 et BC41008, respectivement) lorsqu'ils rencontrent l'attribut <xref:System.Reflection.AssemblyKeyFileAttribute> ou <xref:System.Reflection.AssemblyKeyNameAttribute> dans le code source.</span><span class="sxs-lookup"><span data-stu-id="98470-136">The C# and Visual Basic compilers issue compiler warnings (CS1699 and BC41008, respectively) when they encounter the <xref:System.Reflection.AssemblyKeyFileAttribute> or <xref:System.Reflection.AssemblyKeyNameAttribute> attribute in source code.</span></span> <span data-ttu-id="98470-137">Vous pouvez ignorer les avertissements.</span><span class="sxs-lookup"><span data-stu-id="98470-137">You can ignore the warnings.</span></span>  
  
 <span data-ttu-id="98470-138">L'exemple de code suivant utilise l'attribut <xref:System.Reflection.AssemblyKeyFileAttribute> avec un fichier de clé nommé `keyfile.snk`, situé dans le répertoire où l'assembly est compilé.</span><span class="sxs-lookup"><span data-stu-id="98470-138">The following example uses the <xref:System.Reflection.AssemblyKeyFileAttribute> attribute with a key file called `keyfile.snk`, which is located in the directory where the assembly is compiled.</span></span>  
  
 [!code-cpp[AssemblyName_KeyPair#21](../../../samples/snippets/cpp/VS_Snippets_CLR/AssemblyName_KeyPair/CPP/keyfileattrib.cpp#21)]
 [!code-csharp[AssemblyName_KeyPair#21](../../../samples/snippets/csharp/VS_Snippets_CLR/AssemblyName_KeyPair/CS/keyfileattrib.cs#21)]
 [!code-vb[AssemblyName_KeyPair#21](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AssemblyName_KeyPair/VB/keyfileattrib.vb#21)]  
  
 <span data-ttu-id="98470-139">Vous pouvez également différer la signature d'un assembly lors de la compilation de votre fichier source.</span><span class="sxs-lookup"><span data-stu-id="98470-139">You can also delay sign an assembly when compiling your source file.</span></span> <span data-ttu-id="98470-140">Pour plus d'informations, consultez [Temporisation de signature d'un assembly](../../../docs/framework/app-domains/delay-sign-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="98470-140">For more information, see [Delay Signing an Assembly](../../../docs/framework/app-domains/delay-sign-assembly.md).</span></span>  
  
### <a name="to-sign-an-assembly-with-a-strong-name-by-using-the-compiler"></a><span data-ttu-id="98470-141">Pour signer un assembly avec un nom fort à l'aide du compilateur</span><span class="sxs-lookup"><span data-stu-id="98470-141">To sign an assembly with a strong name by using the compiler</span></span>  
  
-   <span data-ttu-id="98470-142">Compilez vos fichiers de code source avec l'option du compilateur `/keyfile` ou `/delaysign` en C# et Visual Basic, ou l'option de l'éditeur de liens `/KEYFILE` ou `/DELAYSIGN` en C++.</span><span class="sxs-lookup"><span data-stu-id="98470-142">Compile your source code file or files with the `/keyfile` or `/delaysign` compiler option in C# and Visual Basic, or the `/KEYFILE` or `/DELAYSIGN` linker option in C++.</span></span> <span data-ttu-id="98470-143">Après le nom de l'option, ajoutez une virgule et le nom du fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="98470-143">After the option name, add a colon and the name of the key file.</span></span> <span data-ttu-id="98470-144">Lorsque vous utilisez des compilateurs de ligne de commande, vous pouvez copier le fichier de clé dans le répertoire qui contient vos fichiers de code source.</span><span class="sxs-lookup"><span data-stu-id="98470-144">When using command-line compilers, you can copy the key file to the directory that contains your source code files.</span></span>  
  
     <span data-ttu-id="98470-145">Pour plus d’informations sur la signature différée, consultez [Delay Signing an Assembly](../../../docs/framework/app-domains/delay-sign-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="98470-145">For information on delay signing, see [Delay Signing an Assembly](../../../docs/framework/app-domains/delay-sign-assembly.md).</span></span>  
  
     <span data-ttu-id="98470-146">L'exemple suivant utilise le compilateur C# et signe l'assembly `UtilityLibrary.dll` avec un nom fort à l'aide du fichier de clé `sgKey.snk`.</span><span class="sxs-lookup"><span data-stu-id="98470-146">The following example uses the C# compiler and signs the assembly `UtilityLibrary.dll` with a strong name by using the key file `sgKey.snk`.</span></span>  
  
    ```  
    csc /t:library UtilityLibrary.cs /keyfile:sgKey.snk  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="98470-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98470-147">See also</span></span>

- [<span data-ttu-id="98470-148">Création et utilisation d'assemblys avec nom fort</span><span class="sxs-lookup"><span data-stu-id="98470-148">Creating and Using Strong-Named Assemblies</span></span>](../../../docs/framework/app-domains/create-and-use-strong-named-assemblies.md)
- [<span data-ttu-id="98470-149">Procédure : créer une paire de clés publique/privée</span><span class="sxs-lookup"><span data-stu-id="98470-149">How to: Create a Public-Private Key Pair</span></span>](../../../docs/framework/app-domains/how-to-create-a-public-private-key-pair.md)
- [<span data-ttu-id="98470-150">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="98470-150">Al.exe (Assembly Linker)</span></span>](../../../docs/framework/tools/al-exe-assembly-linker.md)
- [<span data-ttu-id="98470-151">Temporisation de signature d'un assembly</span><span class="sxs-lookup"><span data-stu-id="98470-151">Delay Signing an Assembly</span></span>](../../../docs/framework/app-domains/delay-sign-assembly.md)
- [<span data-ttu-id="98470-152">Gestion d'assembly et signature de manifeste</span><span class="sxs-lookup"><span data-stu-id="98470-152">Managing Assembly and Manifest Signing</span></span>](/visualstudio/ide/managing-assembly-and-manifest-signing)
- [<span data-ttu-id="98470-153">Page Signature, Concepteur de projets</span><span class="sxs-lookup"><span data-stu-id="98470-153">Signing Page, Project Designer</span></span>](/visualstudio/ide/reference/signing-page-project-designer)
