---
title: -optionexplicit
ms.date: 07/20/2015
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- /optionexplicit
- -optionexplicit
helpviewer_keywords:
- /optionexplicit compiler option [Visual Basic]
- optionexplicit compiler option [Visual Basic]
- -optionexplicit compiler option [Visual Basic]
ms.assetid: 5d296ab3-bafe-4c4d-9887-78f162ed86c7
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 39ad78c82303d3655d5dda9e2286df0a55b8bf3e
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-optionexplicit"></a><span data-ttu-id="8722c-102">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="8722c-102">-optionexplicit</span></span>
<span data-ttu-id="8722c-103">Indique au compilateur de signaler des erreurs si les variables ne sont pas déclarées avant leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="8722c-103">Causes the compiler to report errors if variables are not declared before they are used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8722c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8722c-104">Syntax</span></span>  
  
```  
-optionexplicit[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="8722c-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="8722c-105">Arguments</span></span>  
 <span data-ttu-id="8722c-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="8722c-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="8722c-107">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8722c-107">Optional.</span></span> <span data-ttu-id="8722c-108">Spécifiez `-optionexplicit+` pour exiger la déclaration explicite des variables.</span><span class="sxs-lookup"><span data-stu-id="8722c-108">Specify `-optionexplicit+` to require explicit declaration of variables.</span></span> <span data-ttu-id="8722c-109">Le `-optionexplicit+` option est la valeur par défaut et est identique à `-optionexplicit`.</span><span class="sxs-lookup"><span data-stu-id="8722c-109">The `-optionexplicit+` option is the default and is the same as `-optionexplicit`.</span></span> <span data-ttu-id="8722c-110">Le `-optionexplicit-` option permet une déclaration implicite des variables.</span><span class="sxs-lookup"><span data-stu-id="8722c-110">The `-optionexplicit-` option enables implicit declaration of variables.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8722c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8722c-111">Remarks</span></span>  
 <span data-ttu-id="8722c-112">Si le fichier de code source contient un [instruction Option Explicit](../../../visual-basic/language-reference/statements/option-explicit-statement.md), l’instruction substitue le `-optionexplicit` paramètre du compilateur de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8722c-112">If the source code file contains an [Option Explicit statement](../../../visual-basic/language-reference/statements/option-explicit-statement.md), the statement overrides the `-optionexplicit` command-line compiler setting.</span></span>  
  
### <a name="to-set--optionexplicit-in-the-visual-studio-ide"></a><span data-ttu-id="8722c-113">Pour définir des - optionexplicit dans l’IDE de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8722c-113">To set -optionexplicit in the Visual Studio IDE</span></span>  
  
1.  <span data-ttu-id="8722c-114">Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="8722c-114">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="8722c-115">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8722c-115">On the **Project** menu, click **Properties**.</span></span>   
  
2.  <span data-ttu-id="8722c-116">Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="8722c-116">Click the **Compile** tab.</span></span>  
  
3.  <span data-ttu-id="8722c-117">Modifiez la valeur dans la **Option Explicit** boîte.</span><span class="sxs-lookup"><span data-stu-id="8722c-117">Modify the value in the **Option Explicit** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8722c-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="8722c-118">Example</span></span>  
 <span data-ttu-id="8722c-119">Le code suivant compile si `-optionexplicit-` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8722c-119">The following code compiles when `-optionexplicit-` is used.</span></span>  
  
 [!code-vb[VbVbalrCompiler#5](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/optionexplicit_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="8722c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8722c-120">See Also</span></span>  
 [<span data-ttu-id="8722c-121">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8722c-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="8722c-122">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="8722c-122">-optioncompare</span></span>](../../../visual-basic/reference/command-line-compiler/optioncompare.md)  
 [<span data-ttu-id="8722c-123">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="8722c-123">-optionstrict</span></span>](../../../visual-basic/reference/command-line-compiler/optionstrict.md)  
 [<span data-ttu-id="8722c-124">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="8722c-124">-optioninfer</span></span>](../../../visual-basic/reference/command-line-compiler/optioninfer.md)  
 [<span data-ttu-id="8722c-125">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="8722c-125">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="8722c-126">Option Explicit (instruction)</span><span class="sxs-lookup"><span data-stu-id="8722c-126">Option Explicit Statement</span></span>](../../../visual-basic/language-reference/statements/option-explicit-statement.md)  
 [<span data-ttu-id="8722c-127">Valeurs par défaut Visual Basic, Projets, boîte de dialogue Options</span><span class="sxs-lookup"><span data-stu-id="8722c-127">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
