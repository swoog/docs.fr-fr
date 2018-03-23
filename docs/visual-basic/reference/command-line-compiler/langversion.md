---
title: -/langversion (Visual Basic)
ms.date: 03/10/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- /langversion compiler option [Visual Basic]
- langversion compiler option [Visual Basic]
- -langversion compiler option [Visual Basic]
ms.assetid: 59b7b0c8-2dde-4e9b-94e7-0237f7e0bafb
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d9b91bf8efa6fabd21d257e51062dc881ab288f5
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-langversion-visual-basic"></a><span data-ttu-id="d79f3-102">-/langversion (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d79f3-102">-langversion (Visual Basic)</span></span>
<span data-ttu-id="d79f3-103">Entraîne le compilateur à accepter uniquement la syntaxe qui est incluse dans la version du langage Visual Basic spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d79f3-103">Causes the compiler to accept only syntax that is included in the specified Visual Basic language version.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d79f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d79f3-104">Syntax</span></span>  
  
```  
-langversion:version  
```  
  
## <a name="arguments"></a><span data-ttu-id="d79f3-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="d79f3-105">Arguments</span></span>  
 `version`  
 <span data-ttu-id="d79f3-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d79f3-106">Required.</span></span> <span data-ttu-id="d79f3-107">La langue à utiliser lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d79f3-107">The language version to be used during the compilation.</span></span> <span data-ttu-id="d79f3-108">Valeurs acceptées sont `9`, `9.0`, `10`, et `10.0`.</span><span class="sxs-lookup"><span data-stu-id="d79f3-108">Accepted values are `9`, `9.0`, `10`, and `10.0`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d79f3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d79f3-109">Remarks</span></span>  
 <span data-ttu-id="d79f3-110">Le `-langversion` option spécifie la syntaxe acceptée par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="d79f3-110">The `-langversion` option specifies what syntax the compiler accepts.</span></span> <span data-ttu-id="d79f3-111">Par exemple, si vous spécifiez que la version est 9.0, le compilateur génère des erreurs de syntaxe qui est valide uniquement dans la version 10.0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d79f3-111">For example, if you specify that the language version is 9.0, the compiler generates errors for syntax that is valid only in version 10.0 and later.</span></span>  
  
 <span data-ttu-id="d79f3-112">Vous pouvez utiliser cette option lorsque vous développez des applications qui ciblent des versions différentes du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d79f3-112">You can use this option when you develop applications that target different versions of the .NET Framework.</span></span> <span data-ttu-id="d79f3-113">Par exemple, si vous ciblez .NET Framework 3.5, vous pouvez utiliser cette option pour vous assurer que vous n’utilisez pas la syntaxe de la version de langage 10.0.</span><span class="sxs-lookup"><span data-stu-id="d79f3-113">For example, if you are targeting .NET Framework 3.5, you could use this option to ensure that you do not use syntax from language version 10.0.</span></span>  
  
 <span data-ttu-id="d79f3-114">Vous pouvez définir `-langversion` directement uniquement à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d79f3-114">You can set `-langversion` directly only by using the command line.</span></span> <span data-ttu-id="d79f3-115">Pour plus d’informations, consultez [Ciblage d’une version spécifique du .NET Framework](/visualstudio/ide/targeting-a-specific-dotnet-framework-version).</span><span class="sxs-lookup"><span data-stu-id="d79f3-115">For more information, see [Targeting a Specific .NET Framework Version](/visualstudio/ide/targeting-a-specific-dotnet-framework-version).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d79f3-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="d79f3-116">Example</span></span>  
 <span data-ttu-id="d79f3-117">Le code suivant compile `sample.vb` pour Visual Basic 9.0.</span><span class="sxs-lookup"><span data-stu-id="d79f3-117">The following code compiles `sample.vb` for Visual Basic 9.0.</span></span>  
  
```console  
vbc -langversion:9.0 sample.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="d79f3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d79f3-118">See Also</span></span>  
 [<span data-ttu-id="d79f3-119">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d79f3-119">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="d79f3-120">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="d79f3-120">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="d79f3-121">Cibler une version spécifique du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d79f3-121">Targeting a Specific .NET Framework Version</span></span>](/visualstudio/ide/targeting-a-specific-dotnet-framework-version)
