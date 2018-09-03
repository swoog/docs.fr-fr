---
title: -keycontainer (Options du compilateur C#)
ms.date: 05/16/2018
f1_keywords:
- /keycontainer
helpviewer_keywords:
- /keycontainer compiler option [C#]
- keycontainer compiler option [C#]
- -keycontainer compiler option [C#]
ms.assetid: b3982b6d-2382-4f7e-bebd-ce98eaa30763
ms.openlocfilehash: 57d3acb4fe128e07020bfe7c85ed86563b16f40a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467543"
---
# <a name="-keycontainer-c-compiler-options"></a><span data-ttu-id="08da8-102">-keycontainer (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="08da8-102">-keycontainer (C# Compiler Options)</span></span>
<span data-ttu-id="08da8-103">Spécifie le nom du conteneur de la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="08da8-103">Specifies the name of the cryptographic key container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08da8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08da8-104">Syntax</span></span>  
  
```console  
-keycontainer:string  
```  
  
## <a name="arguments"></a><span data-ttu-id="08da8-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="08da8-105">Arguments</span></span>  
 `string`  
 <span data-ttu-id="08da8-106">Nom du conteneur de clé de nom fort.</span><span class="sxs-lookup"><span data-stu-id="08da8-106">The name of the strong name key container.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="08da8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="08da8-107">Remarks</span></span>  
 <span data-ttu-id="08da8-108">Quand l’option **-keycontainer** est utilisée, le compilateur crée un composant pouvant être partagé.</span><span class="sxs-lookup"><span data-stu-id="08da8-108">When the **-keycontainer** option is used, the compiler creates a sharable component.</span></span> <span data-ttu-id="08da8-109">Le compilateur insère une clé publique à partir du conteneur spécifié dans le manifeste d’assembly et signe l’assembly final avec la clé privée.</span><span class="sxs-lookup"><span data-stu-id="08da8-109">The compiler inserts a public key from the specified container into the assembly manifest and signs the final assembly with the private key.</span></span> <span data-ttu-id="08da8-110">Pour générer un fichier de clé, tapez `sn -k file` à la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="08da8-110">To generate a key file, type `sn -k file` at the command line.</span></span> <span data-ttu-id="08da8-111">`sn -i` installe la paire de clés dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="08da8-111">`sn -i` installs the key pair into a container.</span></span> <span data-ttu-id="08da8-112">Cette option n’est pas prise en charge quand le compilateur s’exécute sur CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="08da8-112">This option is not supported when the compiler runs on CoreCLR.</span></span> <span data-ttu-id="08da8-113">Pour signer un assembly en cas de génération sur CoreCLR, utilisez l’option [-keyfile](keyfile-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="08da8-113">To sign an assembly when building on CoreCLR, use the [-keyfile](keyfile-compiler-option.md) option.</span></span>
  
 <span data-ttu-id="08da8-114">Si vous compilez avec [-target:module](../../../csharp/language-reference/compiler-options/target-module-compiler-option.md), le nom du fichier de clé est conservé dans le module et incorporé dans l’assembly quand vous compilez ce module dans un assembly avec [-addmodule](../../../csharp/language-reference/compiler-options/addmodule-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="08da8-114">If you compile with [-target:module](../../../csharp/language-reference/compiler-options/target-module-compiler-option.md), the name of the key file is held in the module and incorporated into the assembly when you compile this module into an assembly with [-addmodule](../../../csharp/language-reference/compiler-options/addmodule-compiler-option.md).</span></span>  
  
 <span data-ttu-id="08da8-115">Vous pouvez également spécifier cette option comme attribut personnalisé (<xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=nameWithType>) dans le code source de n'importe quel module MSIL (Microsoft Intermediate Language).</span><span class="sxs-lookup"><span data-stu-id="08da8-115">You can also specify this option as a custom attribute (<xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=nameWithType>) in the source code for any Microsoft intermediate language (MSIL) module.</span></span>  
  
 <span data-ttu-id="08da8-116">Vous pouvez également passer vos informations de chiffrement au compilateur avec [-keyfile](../../../csharp/language-reference/compiler-options/keyfile-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="08da8-116">You can also pass your encryption information to the compiler with [-keyfile](../../../csharp/language-reference/compiler-options/keyfile-compiler-option.md).</span></span> <span data-ttu-id="08da8-117">Utilisez [-delaysign](../../../csharp/language-reference/compiler-options/delaysign-compiler-option.md) si vous voulez ajouter la clé publique au manifeste d’assembly, mais que vous voulez différer la signature de l’assembly tant qu’il n’a pas été testé.</span><span class="sxs-lookup"><span data-stu-id="08da8-117">Use [-delaysign](../../../csharp/language-reference/compiler-options/delaysign-compiler-option.md) if you want the public key added to the assembly manifest but want to delay signing the assembly until it has been tested.</span></span>  
  
 <span data-ttu-id="08da8-118">Pour plus d’informations, consultez [Création et utilisation d’assemblys avec nom fort](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) et [Différer la signature d’un assembly](../../../framework/app-domains/delay-sign-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="08da8-118">For more information, see [Creating and Using Strong-Named Assemblies](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) and [Delay Signing an Assembly](../../../framework/app-domains/delay-sign-assembly.md).</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="08da8-119">Pour définir cette option du compilateur dans l'environnement de développement Visual Studio</span><span class="sxs-lookup"><span data-stu-id="08da8-119">To set this compiler option in the Visual Studio development environment</span></span>  
  
1.  <span data-ttu-id="08da8-120">Cette option de compilateur n’est pas disponible dans l'environnement de développement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="08da8-120">This compiler option is not available in the Visual Studio development environment.</span></span>  
  
 <span data-ttu-id="08da8-121">Vous pouvez accéder par programmation à cette option de compilateur avec <xref:VSLangProj.ProjectProperties.AssemblyKeyContainerName%2A>.</span><span class="sxs-lookup"><span data-stu-id="08da8-121">You can programmatically access this compiler option with <xref:VSLangProj.ProjectProperties.AssemblyKeyContainerName%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08da8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08da8-122">See Also</span></span>

- [<span data-ttu-id="08da8-123">Option -keyfile du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="08da8-123">C# Compiler -keyfile option</span></span>](keyfile-compiler-option.md)
- [<span data-ttu-id="08da8-124">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="08da8-124">C# Compiler Options</span></span>](index.md)  
- [<span data-ttu-id="08da8-125">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="08da8-125">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
