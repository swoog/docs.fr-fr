---
title: -target:exe (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /exe
helpviewer_keywords:
- target compiler options [C#], /target:exe
- /target compiler options [C#], /target:exe
- -target compiler options [C#], /target:exe
ms.assetid: bda5717d-1b91-4848-956b-fcf85c30e432
ms.openlocfilehash: 7d34a25fd614a209761714e1f4eff3042ca240c0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59331310"
---
# <a name="-targetexe-c-compiler-options"></a><span data-ttu-id="ea895-102">-target:exe (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="ea895-102">-target:exe (C# Compiler Options)</span></span>
<span data-ttu-id="ea895-103">L’option **-target:exe** indique au compilateur de créer une application console exécutable (EXE).</span><span class="sxs-lookup"><span data-stu-id="ea895-103">The **-target:exe** option causes the compiler to create an executable (EXE), console application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea895-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea895-104">Syntax</span></span>  
  
```console  
-target:exe  
```  
  
## <a name="remarks"></a><span data-ttu-id="ea895-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea895-105">Remarks</span></span>  
 <span data-ttu-id="ea895-106">L’option **-target:exe** est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ea895-106">The **-target:exe** option is in effect by default.</span></span> <span data-ttu-id="ea895-107">Le fichier exécutable est créé avec l’extension .exe.</span><span class="sxs-lookup"><span data-stu-id="ea895-107">The executable file will be created with the .exe extension.</span></span>  
  
 <span data-ttu-id="ea895-108">Utilisez [-target:winexe](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md) pour créer un programme exécutable Windows.</span><span class="sxs-lookup"><span data-stu-id="ea895-108">Use [-target:winexe](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md) to create a Windows program executable.</span></span>  
  
 <span data-ttu-id="ea895-109">À moins que l’option [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md) spécifie autre chose, le fichier de sortie prend le nom du fichier d’entrée qui contient la méthode [Main](../../../csharp/programming-guide/main-and-command-args/index.md).</span><span class="sxs-lookup"><span data-stu-id="ea895-109">Unless otherwise specified with the [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md) option, the output file name takes the name of the input file that contains the [Main](../../../csharp/programming-guide/main-and-command-args/index.md) method.</span></span>  
  
 <span data-ttu-id="ea895-110">Quand ils sont spécifiés dans la ligne de commande, tous les fichiers jusqu’à l’option **-out** ou **-target:module** suivante sont utilisés pour créer le fichier .exe.</span><span class="sxs-lookup"><span data-stu-id="ea895-110">When specified at the command line, all files up to the next **-out** or **-target:module** option are used to create the .exe file</span></span>  
  
 <span data-ttu-id="ea895-111">Une seule et unique méthode **Main** est requise dans les fichiers de code source qui sont compilés dans un fichier .exe.</span><span class="sxs-lookup"><span data-stu-id="ea895-111">One and only one **Main** method is required in the source code files that are compiled into an .exe file.</span></span> <span data-ttu-id="ea895-112">L’option de compilateur [-main](../../../csharp/language-reference/compiler-options/main-compiler-option.md) vous permet de spécifier la classe contenant la méthode **Main**, au cas où votre code possède plusieurs classes avec une méthode **Main**.</span><span class="sxs-lookup"><span data-stu-id="ea895-112">The [-main](../../../csharp/language-reference/compiler-options/main-compiler-option.md) compiler option lets you specify which class contains the **Main** method, in cases where your code has more than one class with a **Main** method.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="ea895-113">Pour définir cette option du compilateur dans l'environnement de développement Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ea895-113">To set this compiler option in the Visual Studio development environment</span></span>  
  
1. <span data-ttu-id="ea895-114">Ouvrez la page **Propriétés** du projet.</span><span class="sxs-lookup"><span data-stu-id="ea895-114">Open the project's **Properties** page.</span></span>  
  
2. <span data-ttu-id="ea895-115">Cliquez sur la page de propriétés **Application**.</span><span class="sxs-lookup"><span data-stu-id="ea895-115">Click the **Application** property page.</span></span>  
  
3. <span data-ttu-id="ea895-116">Modifiez la propriété **Type de sortie**.</span><span class="sxs-lookup"><span data-stu-id="ea895-116">Modify the **Output type** property.</span></span>  
  
 <span data-ttu-id="ea895-117">Pour plus d’informations sur la définition de cette option du compilateur par programmation, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.</span><span class="sxs-lookup"><span data-stu-id="ea895-117">For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ea895-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="ea895-118">Example</span></span>  
 <span data-ttu-id="ea895-119">Chacune des lignes de commande suivantes compile `in.cs` et crée `in.exe` :</span><span class="sxs-lookup"><span data-stu-id="ea895-119">Each of the following command lines will compile `in.cs`, creating `in.exe`:</span></span>  
  
```console  
csc -target:exe in.cs  
csc in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="ea895-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea895-120">See also</span></span>

- [<span data-ttu-id="ea895-121">-target (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="ea895-121">-target (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/target-compiler-option.md)
- [<span data-ttu-id="ea895-122">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="ea895-122">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
