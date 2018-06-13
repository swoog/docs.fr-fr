---
title: -keyfile
ms.date: 03/10/2018
helpviewer_keywords:
- /keyfile compiler option [Visual Basic]
- keyfile compiler option [Visual Basic]
- -keyfile compiler option [Visual Basic]
ms.assetid: ffa82a4b-517a-4c6c-9889-5bae7b534bb8
ms.openlocfilehash: 12895e4a18203a0d6c409a3b2117abbc59fab7a2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653479"
---
# <a name="-keyfile"></a><span data-ttu-id="501a7-102">-keyfile</span><span class="sxs-lookup"><span data-stu-id="501a7-102">-keyfile</span></span>
<span data-ttu-id="501a7-103">Spécifie un fichier contenant une clé ou une paire de clés afin d'attribuer un nom fort à un assembly.</span><span class="sxs-lookup"><span data-stu-id="501a7-103">Specifies a file containing a key or key pair to give an assembly a strong name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="501a7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="501a7-104">Syntax</span></span>  
  
``` 
-keyfile:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="501a7-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="501a7-105">Arguments</span></span>  
 `file`  
 <span data-ttu-id="501a7-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="501a7-106">Required.</span></span> <span data-ttu-id="501a7-107">Fichier qui contient la clé.</span><span class="sxs-lookup"><span data-stu-id="501a7-107">File that contains the key.</span></span> <span data-ttu-id="501a7-108">Si le nom de fichier contient un espace, placez-le entre guillemets (« »).</span><span class="sxs-lookup"><span data-stu-id="501a7-108">If the file name contains a space, enclose the name in quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="501a7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="501a7-109">Remarks</span></span>  
 <span data-ttu-id="501a7-110">Le compilateur insère la clé publique dans le manifeste d’assembly et puis signe l’assembly final avec la clé privée.</span><span class="sxs-lookup"><span data-stu-id="501a7-110">The compiler inserts the public key into the assembly manifest and then signs the final assembly with the private key.</span></span> <span data-ttu-id="501a7-111">Pour générer un fichier de clé, tapez `sn -k file` à la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="501a7-111">To generate a key file, type `sn -k file` at the command line.</span></span> <span data-ttu-id="501a7-112">Pour plus d’informations, consultez [Sn.exe (outil Strong Name)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="501a7-112">For more information, see [Sn.exe (Strong Name Tool)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)).</span></span>  
  
 <span data-ttu-id="501a7-113">Si vous compilez avec `-target:module`, le nom du fichier de clé est conservé dans le module et incorporé dans l’assembly qui est créé lorsque vous compilez un assembly avec [/addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md).</span><span class="sxs-lookup"><span data-stu-id="501a7-113">If you compile with `-target:module`, the name of the key file is held in the module and incorporated into the assembly that is created when you compile an assembly with [/addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md).</span></span>  
  
 <span data-ttu-id="501a7-114">Vous pouvez également passer vos informations de chiffrement au compilateur avec [-keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md).</span><span class="sxs-lookup"><span data-stu-id="501a7-114">You can also pass your encryption information to the compiler with [-keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md).</span></span> <span data-ttu-id="501a7-115">Utilisez [-delaysign](../../../visual-basic/reference/command-line-compiler/delaysign.md) si vous voulez obtenir un assembly partiellement signé.</span><span class="sxs-lookup"><span data-stu-id="501a7-115">Use [-delaysign](../../../visual-basic/reference/command-line-compiler/delaysign.md) if you want a partially signed assembly.</span></span>  
  
 <span data-ttu-id="501a7-116">Vous pouvez également spécifier cette option comme attribut personnalisé (<xref:System.Reflection.AssemblyKeyFileAttribute>) dans le code source de n’importe quel module Microsoft intermediate language.</span><span class="sxs-lookup"><span data-stu-id="501a7-116">You can also specify this option as a custom attribute (<xref:System.Reflection.AssemblyKeyFileAttribute>) in the source code for any Microsoft intermediate language module.</span></span>  
  
 <span data-ttu-id="501a7-117">Tous deux `-keyfile` et [- keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md) sont spécifiés (par option de ligne de commande ou par attribut personnalisé) dans la même compilation, le compilateur essaie d’abord le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="501a7-117">In case both `-keyfile` and [-keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md) are specified (either by command-line option or by custom attribute) in the same compilation, the compiler first tries the key container.</span></span> <span data-ttu-id="501a7-118">Si cette tentative réussit, l'assembly est signé avec les informations figurant dans le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="501a7-118">If that succeeds, then the assembly is signed with the information in the key container.</span></span> <span data-ttu-id="501a7-119">Si le compilateur ne trouve pas le conteneur de clé, il essaie le fichier spécifié avec `-keyfile`.</span><span class="sxs-lookup"><span data-stu-id="501a7-119">If the compiler does not find the key container, it tries the file specified with `-keyfile`.</span></span> <span data-ttu-id="501a7-120">Si cette opération réussit, l’assembly est signé avec les informations contenues dans le fichier de clé et les informations de clé sont installées dans le conteneur de clé (semblable à `sn -i`) afin que lors de la compilation suivante, le conteneur de clé sera valide.</span><span class="sxs-lookup"><span data-stu-id="501a7-120">If this succeeds, the assembly is signed with the information in the key file, and the key information is installed in the key container (similar to `sn -i`) so that on the next compilation, the key container will be valid.</span></span>  
  
 <span data-ttu-id="501a7-121">Notez qu’un fichier de clé peut contenir uniquement la clé publique.</span><span class="sxs-lookup"><span data-stu-id="501a7-121">Note that a key file might contain only the public key.</span></span>  
  
 <span data-ttu-id="501a7-122">Consultez [création et assemblys avec nom fort](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) pour plus d’informations sur la signature d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="501a7-122">See [Creating and Using Strong-Named Assemblies](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) for more information on signing an assembly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="501a7-123">Le `-keyfile` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="501a7-123">The `-keyfile` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="501a7-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="501a7-124">Example</span></span>  
 <span data-ttu-id="501a7-125">Le code suivant compile le fichier source `Input.vb` et spécifie un fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="501a7-125">The following code compiles source file `Input.vb` and specifies a key file.</span></span>  
  
```console  
vbc -keyfile:myfile.sn input.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="501a7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="501a7-126">See Also</span></span>  
 [<span data-ttu-id="501a7-127">Assemblys et le Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="501a7-127">Assemblies and the Global Assembly Cache</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
 [<span data-ttu-id="501a7-128">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="501a7-128">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="501a7-129">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="501a7-129">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)  
 [<span data-ttu-id="501a7-130">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="501a7-130">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
