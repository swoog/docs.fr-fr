---
title: -vbruntime
ms.date: 03/13/2018
f1_keywords:
- vbruntime
- -vbruntime
helpviewer_keywords:
- vbruntime compiler option [Visual Basic]
- -vbruntime compiler option [Visual Basic]
- /vbruntime compiler option [Visual Basic]
ms.assetid: 1aa0239e-511a-4c29-957d-fd72877b350a
ms.openlocfilehash: a1988fcd19c6629d85ae0e739681fd39fe033c0d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796128"
---
# <a name="-vbruntime"></a><span data-ttu-id="bcfd4-102">-vbruntime</span><span class="sxs-lookup"><span data-stu-id="bcfd4-102">-vbruntime</span></span>
<span data-ttu-id="bcfd4-103">Spécifie que le compilateur doit compiler sans référence à la bibliothèque runtime Visual Basic, ou avec une référence à une bibliothèque runtime spécifique.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-103">Specifies that the compiler should compile without a reference to the Visual Basic Runtime Library, or with a reference to a specific runtime library.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcfd4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcfd4-104">Syntax</span></span>  
  
```  
-vbruntime:{ - | + | * | path }  
```  
  
## <a name="arguments"></a><span data-ttu-id="bcfd4-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="bcfd4-105">Arguments</span></span>  
 \-  
 <span data-ttu-id="bcfd4-106">Compiler sans référence à la bibliothèque Runtime Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-106">Compile without a reference to the Visual Basic Runtime Library.</span></span>  
  
 \+  
 <span data-ttu-id="bcfd4-107">Compilez avec une référence à la bibliothèque Runtime Visual Basic par défaut.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-107">Compile with a reference to the default Visual Basic Runtime Library.</span></span>  
  
 \*  
 <span data-ttu-id="bcfd4-108">Compiler sans référence à la bibliothèque Runtime Visual Basic et incorporer la fonctionnalité principale de la bibliothèque Runtime Visual Basic dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-108">Compile without a reference to the Visual Basic Runtime Library, and embed core functionality from the Visual Basic Runtime Library into the assembly.</span></span>  
  
 `path`  
 <span data-ttu-id="bcfd4-109">Compilez avec une référence à la bibliothèque spécifiée (DLL).</span><span class="sxs-lookup"><span data-stu-id="bcfd4-109">Compile with a reference to the specified library (DLL).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bcfd4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bcfd4-110">Remarks</span></span>  
 <span data-ttu-id="bcfd4-111">Le `-vbruntime` option du compilateur vous permet de spécifier que le compilateur doit compiler sans référence à la bibliothèque Runtime Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-111">The `-vbruntime` compiler option enables you to specify that the compiler should compile without a reference to the Visual Basic Runtime Library.</span></span> <span data-ttu-id="bcfd4-112">Si vous compilez sans référence à la bibliothèque Runtime Visual Basic, erreurs ou avertissements sont consignés sur les constructions de code ou de langage qui génèrent un appel à une application d’assistance du runtime Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-112">If you compile without a reference to the Visual Basic Runtime Library, errors or warnings are logged on code or language constructs that generate a call to a Visual Basic runtime helper.</span></span> <span data-ttu-id="bcfd4-113">(Un *du composant d’exécution Visual Basic* est une fonction définie dans Microsoft.VisualBasic.dll, qui est appelée pendant l’exécution pour exécuter une sémantique de langue spécifique.)</span><span class="sxs-lookup"><span data-stu-id="bcfd4-113">(A *Visual Basic runtime helper* is a function defined in Microsoft.VisualBasic.dll that is called at runtime to execute a specific language semantic.)</span></span>  
  
 <span data-ttu-id="bcfd4-114">Le `-vbruntime+` option produit le même comportement se produit si aucun `-vbruntime` commutateur est spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-114">The `-vbruntime+` option produces the same behavior that occurs if no `-vbruntime` switch is specified.</span></span> <span data-ttu-id="bcfd4-115">Vous pouvez utiliser la `-vbruntime+` option permettant de remplacer la précédente `-vbruntime` commutateurs.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-115">You can use the `-vbruntime+` option to override previous `-vbruntime` switches.</span></span>  
  
 <span data-ttu-id="bcfd4-116">La plupart des objets de la `My` type ne sont pas disponibles lorsque vous utilisez le `-vbruntime-` ou `-vbruntime:path` options.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-116">Most objects of the `My` type are unavailable when you use the `-vbruntime-` or `-vbruntime:path` options.</span></span>  
  
## <a name="embedding-visual-basic-runtime-core-functionality"></a><span data-ttu-id="bcfd4-117">Incorporation des fonctionnalités principales de Runtime de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bcfd4-117">Embedding Visual Basic Runtime core functionality</span></span>  
 <span data-ttu-id="bcfd4-118">Le `-vbruntime*` option vous permet de compiler sans référence à une bibliothèque runtime.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-118">The `-vbruntime*` option enables you to compile without a reference to a runtime library.</span></span> <span data-ttu-id="bcfd4-119">Au lieu de cela, les fonctionnalités principales de la bibliothèque Runtime Visual Basic sont incorporée dans l’assembly de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-119">Instead, core functionality from the Visual Basic Runtime Library is embedded in the user assembly.</span></span> <span data-ttu-id="bcfd4-120">Vous pouvez utiliser cette option si votre application s’exécute sur les plateformes qui ne contiennent pas le runtime Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-120">You can use this option if your application runs on platforms that do not contain the Visual Basic runtime.</span></span>  
  
 <span data-ttu-id="bcfd4-121">Les membres du runtime suivants sont incorporés :</span><span class="sxs-lookup"><span data-stu-id="bcfd4-121">The following runtime members are embedded:</span></span>  
  
- <span data-ttu-id="bcfd4-122">Classe <xref:Microsoft.VisualBasic.CompilerServices.Conversions></span><span class="sxs-lookup"><span data-stu-id="bcfd4-122"><xref:Microsoft.VisualBasic.CompilerServices.Conversions> class</span></span>  
  
- <span data-ttu-id="bcfd4-123">Méthode <xref:Microsoft.VisualBasic.Strings.AscW%28System.Char%29></span><span class="sxs-lookup"><span data-stu-id="bcfd4-123"><xref:Microsoft.VisualBasic.Strings.AscW%28System.Char%29> method</span></span>  
  
- <span data-ttu-id="bcfd4-124">Méthode <xref:Microsoft.VisualBasic.Strings.AscW%28System.String%29></span><span class="sxs-lookup"><span data-stu-id="bcfd4-124"><xref:Microsoft.VisualBasic.Strings.AscW%28System.String%29> method</span></span>  
  
- <span data-ttu-id="bcfd4-125">Méthode <xref:Microsoft.VisualBasic.Strings.ChrW%28System.Int32%29></span><span class="sxs-lookup"><span data-stu-id="bcfd4-125"><xref:Microsoft.VisualBasic.Strings.ChrW%28System.Int32%29> method</span></span>  
  
- <span data-ttu-id="bcfd4-126"><xref:Microsoft.VisualBasic.Constants.vbBack> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-126"><xref:Microsoft.VisualBasic.Constants.vbBack> constant</span></span>  
  
- <span data-ttu-id="bcfd4-127"><xref:Microsoft.VisualBasic.Constants.vbCr> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-127"><xref:Microsoft.VisualBasic.Constants.vbCr> constant</span></span>  
  
- <span data-ttu-id="bcfd4-128"><xref:Microsoft.VisualBasic.Constants.vbCrLf> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-128"><xref:Microsoft.VisualBasic.Constants.vbCrLf> constant</span></span>  
  
- <span data-ttu-id="bcfd4-129"><xref:Microsoft.VisualBasic.Constants.vbFormFeed> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-129"><xref:Microsoft.VisualBasic.Constants.vbFormFeed> constant</span></span>  
  
- <span data-ttu-id="bcfd4-130"><xref:Microsoft.VisualBasic.Constants.vbLf> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-130"><xref:Microsoft.VisualBasic.Constants.vbLf> constant</span></span>  
  
- <span data-ttu-id="bcfd4-131"><xref:Microsoft.VisualBasic.Constants.vbNewLine> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-131"><xref:Microsoft.VisualBasic.Constants.vbNewLine> constant</span></span>  
  
- <span data-ttu-id="bcfd4-132"><xref:Microsoft.VisualBasic.Constants.vbNullChar> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-132"><xref:Microsoft.VisualBasic.Constants.vbNullChar> constant</span></span>  
  
- <span data-ttu-id="bcfd4-133"><xref:Microsoft.VisualBasic.Constants.vbNullString> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-133"><xref:Microsoft.VisualBasic.Constants.vbNullString> constant</span></span>  
  
- <span data-ttu-id="bcfd4-134"><xref:Microsoft.VisualBasic.Constants.vbTab> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-134"><xref:Microsoft.VisualBasic.Constants.vbTab> constant</span></span>  
  
- <span data-ttu-id="bcfd4-135"><xref:Microsoft.VisualBasic.Constants.vbVerticalTab> Constante</span><span class="sxs-lookup"><span data-stu-id="bcfd4-135"><xref:Microsoft.VisualBasic.Constants.vbVerticalTab> constant</span></span>  
  
- <span data-ttu-id="bcfd4-136">Certains objets de la `My` type</span><span class="sxs-lookup"><span data-stu-id="bcfd4-136">Some objects of the `My` type</span></span>  
  
 <span data-ttu-id="bcfd4-137">Si vous compilez à l’aide de la `-vbruntime*` option et votre code fait référence à un membre à partir de la bibliothèque Runtime Visual Basic qui ne sont pas incorporées avec la fonctionnalité principale, le compilateur retourne une erreur qui indique que le membre n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-137">If you compile using the `-vbruntime*` option and your code references a member from the Visual Basic Runtime Library that is not embedded with the core functionality, the compiler returns an error that indicates that the member is not available.</span></span>  
  
## <a name="referencing-a-specified-library"></a><span data-ttu-id="bcfd4-138">Fait référence à une bibliothèque spécifiée</span><span class="sxs-lookup"><span data-stu-id="bcfd4-138">Referencing a specified library</span></span>  
 <span data-ttu-id="bcfd4-139">Vous pouvez utiliser le `path` argument pour compiler avec une référence à une bibliothèque runtime personnalisé au lieu de la bibliothèque Runtime Visual Basic par défaut.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-139">You can use the `path` argument to compile with a reference to a custom runtime library instead of the default Visual Basic Runtime Library.</span></span>  
  
 <span data-ttu-id="bcfd4-140">Si la valeur de la `path` argument est un chemin d’accès qualifié complet à une DLL, le compilateur utilisera ce fichier en tant que la bibliothèque runtime.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-140">If the value for the `path` argument is a fully qualified path to a DLL, the compiler will use that file as the runtime library.</span></span> <span data-ttu-id="bcfd4-141">Si la valeur de la `path` argument n’est pas un chemin d’accès qualifié complet à une DLL, le compilateur Visual Basic recherchera la DLL identifiée dans le dossier actif tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-141">If the value for the `path` argument is not a fully qualified path to a DLL, the Visual Basic compiler will search for the identified DLL in the current folder first.</span></span> <span data-ttu-id="bcfd4-142">Il recherche ensuite dans le chemin d’accès que vous avez spécifié à l’aide de la [- sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md) option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-142">It will then search in the path that you have specified by using the [-sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md) compiler option.</span></span> <span data-ttu-id="bcfd4-143">Si le `-sdkpath` option du compilateur n’est pas utilisée, le compilateur recherchera la DLL identifiée dans le dossier .NET Framework (`%systemroot%\Microsoft.NET\Framework\versionNumber`).</span><span class="sxs-lookup"><span data-stu-id="bcfd4-143">If the `-sdkpath` compiler option is not used, the compiler will search for the identified DLL in the .NET Framework folder (`%systemroot%\Microsoft.NET\Framework\versionNumber`).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bcfd4-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="bcfd4-144">Example</span></span>  
 <span data-ttu-id="bcfd4-145">L’exemple suivant montre comment utiliser le `-vbruntime` possibilité de compiler avec une référence à une bibliothèque personnalisée.</span><span class="sxs-lookup"><span data-stu-id="bcfd4-145">The following example shows how to use the `-vbruntime` option to compile with a reference to a custom library.</span></span>  
  
```console
vbc -vbruntime:C:\VBLibraries\CustomVBLibrary.dll  
```  
  
## <a name="see-also"></a><span data-ttu-id="bcfd4-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcfd4-146">See also</span></span>

- [<span data-ttu-id="bcfd4-147">Core Visual Basic – nouveau mode de compilation dans Visual Studio 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="bcfd4-147">Visual Basic Core – New compilation mode in Visual Studio 2010 SP1</span></span>](https://devblogs.microsoft.com/vbteam/vb-core-new-compilation-mode-in-visual-studio-2010-sp1/)
- [<span data-ttu-id="bcfd4-148">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bcfd4-148">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="bcfd4-149">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="bcfd4-149">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [<span data-ttu-id="bcfd4-150">-sdkpath</span><span class="sxs-lookup"><span data-stu-id="bcfd4-150">-sdkpath</span></span>](../../../visual-basic/reference/command-line-compiler/sdkpath.md)
