---
title: -moduleassemblyname
ms.date: 03/13/2018
helpviewer_keywords:
- moduleassemblyname compiler option [Visual Basic]
- /moduleassemblyname compiler option [Visual Basic]
- -moduleassemblyname compiler option [Visual Basic]
ms.assetid: 013a57b6-f425-4dd3-b333-512d72c42f55
ms.openlocfilehash: b0279c5ac658c7d0749f62066abbd705d0a271af
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793898"
---
# <a name="-moduleassemblyname"></a><span data-ttu-id="6c802-102">-moduleassemblyname</span><span class="sxs-lookup"><span data-stu-id="6c802-102">-moduleassemblyname</span></span>
<span data-ttu-id="6c802-103">Spécifie le nom de l’assembly dont ce module doit faire partie.</span><span class="sxs-lookup"><span data-stu-id="6c802-103">Specifies the name of the assembly that this module will be a part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c802-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c802-104">Syntax</span></span>  
  
```  
-moduleassemblyname:assembly_name  
```  
  
## <a name="arguments"></a><span data-ttu-id="6c802-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="6c802-105">Arguments</span></span>  
  
|<span data-ttu-id="6c802-106">Terme</span><span class="sxs-lookup"><span data-stu-id="6c802-106">Term</span></span>|<span data-ttu-id="6c802-107">Définition</span><span class="sxs-lookup"><span data-stu-id="6c802-107">Definition</span></span>|  
|---|---|  
|`assembly_name`|<span data-ttu-id="6c802-108">Le nom de l’assembly de ce module fera partie.</span><span class="sxs-lookup"><span data-stu-id="6c802-108">The name of the assembly that this module will be a part of.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c802-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6c802-109">Remarks</span></span>  
 <span data-ttu-id="6c802-110">Le compilateur traite la `-moduleassemblyname` option uniquement si le `-target:module` option a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c802-110">The compiler processes the `-moduleassemblyname` option only if the `-target:module` option has been specified.</span></span> <span data-ttu-id="6c802-111">Cela indique au compilateur de créer un module.</span><span class="sxs-lookup"><span data-stu-id="6c802-111">This causes the compiler to create a module.</span></span> <span data-ttu-id="6c802-112">Le module créé par le compilateur est valide uniquement pour l’assembly spécifié avec la `-moduleassemblyname` option.</span><span class="sxs-lookup"><span data-stu-id="6c802-112">The module created by the compiler is valid only for the assembly specified with the `-moduleassemblyname` option.</span></span> <span data-ttu-id="6c802-113">Si vous placez le module dans un assembly différent, les erreurs d’exécution seront produit.</span><span class="sxs-lookup"><span data-stu-id="6c802-113">If you place the module in a different assembly, run-time errors will occur.</span></span>  
  
 <span data-ttu-id="6c802-114">Le `-moduleassemblyname` option est uniquement requise lorsque les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="6c802-114">The `-moduleassemblyname` option is needed only when the following are true:</span></span>  
  
- <span data-ttu-id="6c802-115">Un type de données dans le module a besoin d’accéder à un `Friend` type dans un assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="6c802-115">A data type in the module needs access to a `Friend` type in a referenced assembly.</span></span>  
  
- <span data-ttu-id="6c802-116">L’assembly référencé a accordé l’accès d’assembly friend à l’assembly dans lequel le module sera généré.</span><span class="sxs-lookup"><span data-stu-id="6c802-116">The referenced assembly has granted friend assembly access to the assembly into which the module will be built.</span></span>  
  
 <span data-ttu-id="6c802-117">Pour plus d’informations sur la création d’un module, consultez [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md).</span><span class="sxs-lookup"><span data-stu-id="6c802-117">For more information about creating a module, see [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md).</span></span> <span data-ttu-id="6c802-118">Pour plus d’informations sur les assemblys friend, consultez [assemblys Friend](../../../standard/assembly/friend-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="6c802-118">For more information about friend assemblies, see [Friend Assemblies](../../../standard/assembly/friend-assemblies.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6c802-119">Le `-moduleassemblyname` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lorsque vous compilez à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="6c802-119">The `-moduleassemblyname` option is not available from within the Visual Studio development environment; it is available only when you compile from a command prompt.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c802-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c802-120">See also</span></span>

- [<span data-ttu-id="6c802-121">Guide pratique pour générer un assembly multifichier</span><span class="sxs-lookup"><span data-stu-id="6c802-121">How to: Build a Multifile Assembly</span></span>](../../../framework/app-domains/how-to-build-a-multifile-assembly.md)
- [<span data-ttu-id="6c802-122">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6c802-122">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="6c802-123">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6c802-123">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="6c802-124">-main</span><span class="sxs-lookup"><span data-stu-id="6c802-124">-main</span></span>](../../../visual-basic/reference/command-line-compiler/main.md)
- [<span data-ttu-id="6c802-125">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6c802-125">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)
- [<span data-ttu-id="6c802-126">-addmodule</span><span class="sxs-lookup"><span data-stu-id="6c802-126">-addmodule</span></span>](../../../visual-basic/reference/command-line-compiler/addmodule.md)
- [<span data-ttu-id="6c802-127">Assemblys dans .NET</span><span class="sxs-lookup"><span data-stu-id="6c802-127">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
- [<span data-ttu-id="6c802-128">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="6c802-128">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [<span data-ttu-id="6c802-129">Assemblys friend</span><span class="sxs-lookup"><span data-stu-id="6c802-129">Friend Assemblies</span></span>](../../../standard/assembly/friend-assemblies.md)
