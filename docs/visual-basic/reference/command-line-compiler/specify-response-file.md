---
title: '@ (spécifier un fichier réponse) (Visual Basic)'
ms.date: 03/13/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- '@ (Specify Response File) compiler option [Visual Basic]'
ms.assetid: a6847eaa-e5f9-4303-9421-45b55484b9ca
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: af66000208dee0896792892a52dc6acdf5cb1e37
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-specify-response-file-visual-basic"></a><span data-ttu-id="2cee5-102">@ (spécifier un fichier réponse) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2cee5-102">@ (Specify Response File) (Visual Basic)</span></span>
<span data-ttu-id="2cee5-103">Spécifie un fichier qui contient les options du compilateur et les fichiers de code source à compiler.</span><span class="sxs-lookup"><span data-stu-id="2cee5-103">Specifies a file that contains compiler options and source-code files to compile.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2cee5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cee5-104">Syntax</span></span>  
  
```  
@response_file  
```  
  
## <a name="arguments"></a><span data-ttu-id="2cee5-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="2cee5-105">Arguments</span></span>  
 `response_file`  
 <span data-ttu-id="2cee5-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2cee5-106">Required.</span></span> <span data-ttu-id="2cee5-107">Un fichier qui répertorie les options du compilateur ou les fichiers de code source à compiler.</span><span class="sxs-lookup"><span data-stu-id="2cee5-107">A file that lists compiler options or source-code files to compile.</span></span> <span data-ttu-id="2cee5-108">Placez le nom de fichier entre guillemets ( » «) si elle contient un espace.</span><span class="sxs-lookup"><span data-stu-id="2cee5-108">Enclose the file name in quotation marks (" ") if it contains a space.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2cee5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2cee5-109">Remarks</span></span>  
 <span data-ttu-id="2cee5-110">Le compilateur traite les options du compilateur et les fichiers de code source spécifiés dans un fichier réponse comme s’ils avaient été spécifiés sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2cee5-110">The compiler processes the compiler options and source-code files specified in a response file as if they had been specified on the command line.</span></span>  
  
 <span data-ttu-id="2cee5-111">Pour spécifier plusieurs fichiers réponse dans une compilation, spécifiez plusieurs options de fichier de réponse, telles que les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2cee5-111">To specify more than one response file in a compilation, specify multiple response-file options, such as the following.</span></span>  
  
```  
@file1.rsp @file2.rsp  
```  
  
 <span data-ttu-id="2cee5-112">Dans une réponse du fichier, plusieurs options du compilateur et les fichiers de code source peuvent apparaître sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="2cee5-112">In a response file, multiple compiler options and source-code files can appear on one line.</span></span> <span data-ttu-id="2cee5-113">Une spécification de l’option du compilateur unique doit apparaître sur une seule ligne (ne peut pas étendre sur plusieurs lignes).</span><span class="sxs-lookup"><span data-stu-id="2cee5-113">A single compiler-option specification must appear on one line (cannot span multiple lines).</span></span> <span data-ttu-id="2cee5-114">Fichiers réponse peuvent contenir des commentaires qui commencent par le `#` symbole.</span><span class="sxs-lookup"><span data-stu-id="2cee5-114">Response files can have comments that begin with the `#` symbol.</span></span>  
  
 <span data-ttu-id="2cee5-115">Vous pouvez combiner des options spécifiées sur la ligne de commande avec les options spécifiées dans un ou plusieurs fichiers de réponse.</span><span class="sxs-lookup"><span data-stu-id="2cee5-115">You can combine options specified on the command line with options specified in one or more response files.</span></span> <span data-ttu-id="2cee5-116">Le compilateur traite les options de commande qu’il les rencontre.</span><span class="sxs-lookup"><span data-stu-id="2cee5-116">The compiler processes the command options as it encounters them.</span></span> <span data-ttu-id="2cee5-117">Par conséquent, les arguments de ligne de commande peuvent remplacer des options précédemment affichées dans les fichiers réponse.</span><span class="sxs-lookup"><span data-stu-id="2cee5-117">Therefore, command-line arguments can override previously listed options in response files.</span></span> <span data-ttu-id="2cee5-118">À l’inverse, les options dans un fichier réponse remplacent les options répertoriées précédemment sur la ligne de commande ou dans d’autres fichiers réponse.</span><span class="sxs-lookup"><span data-stu-id="2cee5-118">Conversely, options in a response file override options listed previously on the command line or in other response files.</span></span>  
  
 <span data-ttu-id="2cee5-119">Visual Basic fournit le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe.</span><span class="sxs-lookup"><span data-stu-id="2cee5-119">Visual Basic provides the Vbc.rsp file, which is located in the same directory as the Vbc.exe file.</span></span> <span data-ttu-id="2cee5-120">Le fichier Vbc.rsp est inclus par défaut, sauf si la `-noconfig` option est utilisée.</span><span class="sxs-lookup"><span data-stu-id="2cee5-120">The Vbc.rsp file is included by default unless the `-noconfig` option is used.</span></span> <span data-ttu-id="2cee5-121">Pour plus d’informations, consultez [- /noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md).</span><span class="sxs-lookup"><span data-stu-id="2cee5-121">For more information, see [-noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2cee5-122">Le `@` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2cee5-122">The `@` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2cee5-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cee5-123">Example</span></span>  
 <span data-ttu-id="2cee5-124">Les lignes suivantes sont à partir d’un exemple de fichier de réponse.</span><span class="sxs-lookup"><span data-stu-id="2cee5-124">The following lines are from a sample response file.</span></span>  
  
```console
# build the first output file  
-target:exe   
-out:MyExe.exe  
source1.vb   
source2.vb  
```  
  
## <a name="example"></a><span data-ttu-id="2cee5-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cee5-125">Example</span></span>  
 <span data-ttu-id="2cee5-126">L’exemple suivant montre comment utiliser le `@` option avec le fichier de réponse nommé `File1.rsp`.</span><span class="sxs-lookup"><span data-stu-id="2cee5-126">The following example demonstrates how to use the `@` option with the response file named `File1.rsp`.</span></span>  
  
```console
vbc @file1.rsp  
```  
  
## <a name="see-also"></a><span data-ttu-id="2cee5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cee5-127">See Also</span></span>  
 [<span data-ttu-id="2cee5-128">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2cee5-128">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="2cee5-129">-noconfig</span><span class="sxs-lookup"><span data-stu-id="2cee5-129">-noconfig</span></span>](../../../visual-basic/reference/command-line-compiler/noconfig.md)  
 [<span data-ttu-id="2cee5-130">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="2cee5-130">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
