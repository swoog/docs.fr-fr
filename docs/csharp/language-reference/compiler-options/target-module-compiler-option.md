---
title: -target:module (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /target:module
helpviewer_keywords:
- -target compiler options [C#], /target:module
- target compiler options [C#], /target:module
- /target compiler options [C#], /target:module
ms.assetid: 9af1e4fa-c749-44e7-ae58-90a3d05d4e72
ms.openlocfilehash: 7cc0e48a7a4a3ec3f28c89e80fadf6aa7e1130f2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43393124"
---
# <a name="-targetmodule-c-compiler-options"></a><span data-ttu-id="a4b81-102">-target:module (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="a4b81-102">-target:module (C# Compiler Options)</span></span>
<span data-ttu-id="a4b81-103">Cette option empêche le compilateur de générer un manifeste d’assembly.</span><span class="sxs-lookup"><span data-stu-id="a4b81-103">This option causes the compiler to not generate an assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4b81-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4b81-104">Syntax</span></span>  
  
```console  
-target:module  
```  
  
## <a name="remarks"></a><span data-ttu-id="a4b81-105">Notes</span><span class="sxs-lookup"><span data-stu-id="a4b81-105">Remarks</span></span>  
 <span data-ttu-id="a4b81-106">Par défaut, le fichier de sortie créé en effectuant une compilation avec cette option porte l’extension .netmodule.</span><span class="sxs-lookup"><span data-stu-id="a4b81-106">By default, the output file created by compiling with this option will have an extension of .netmodule.</span></span>  
  
 <span data-ttu-id="a4b81-107">Un fichier ne disposant pas d’un manifeste d’assembly ne peut pas être chargé par le Common Language Runtime (CLR) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a4b81-107">A file that does not have an assembly manifest cannot be loaded by the .NET Framework common language runtime.</span></span> <span data-ttu-id="a4b81-108">Cependant, un tel fichier peut être incorporé dans le manifeste d’un assembly au moyen de [-addmodule](../../../csharp/language-reference/compiler-options/addmodule-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="a4b81-108">However, such a file can be incorporated into the assembly manifest of an assembly by means of [-addmodule](../../../csharp/language-reference/compiler-options/addmodule-compiler-option.md).</span></span>  
  
 <span data-ttu-id="a4b81-109">Si plusieurs modules sont créés dans une seule compilation, les types [internal](../../../csharp/language-reference/keywords/internal.md) d’un module sont accessibles à d’autres modules dans la compilation.</span><span class="sxs-lookup"><span data-stu-id="a4b81-109">If more than one module is created in a single compilation, [internal](../../../csharp/language-reference/keywords/internal.md) types in one module will be available to other modules in the compilation.</span></span> <span data-ttu-id="a4b81-110">Quand le code d’un module référence des types `internal` dans un autre module, les deux modules doivent être incorporés dans un manifeste d’assembly au moyen de **-addmodule**.</span><span class="sxs-lookup"><span data-stu-id="a4b81-110">When code in one module references `internal` types in another module, then both modules must be incorporated into an assembly manifest, by means of **-addmodule**.</span></span>  
  
 <span data-ttu-id="a4b81-111">La création d’un module n’est pas prise en charge dans l’environnement de développement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a4b81-111">Creating a module is not supported in the Visual Studio development environment.</span></span>  
  
 <span data-ttu-id="a4b81-112">Pour plus d’informations sur la façon de définir cette option du compilateur par programmation, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.</span><span class="sxs-lookup"><span data-stu-id="a4b81-112">For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a4b81-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="a4b81-113">Example</span></span>  
 <span data-ttu-id="a4b81-114">Compilez `in.cs`, en créant `in.netmodule` :</span><span class="sxs-lookup"><span data-stu-id="a4b81-114">Compile `in.cs`, creating `in.netmodule`:</span></span>  
  
```console  
csc -target:module in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="a4b81-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4b81-115">See Also</span></span>  

- [<span data-ttu-id="a4b81-116">-target (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="a4b81-116">-target (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/target-compiler-option.md)  
- [<span data-ttu-id="a4b81-117">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="a4b81-117">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
