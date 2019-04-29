---
title: -win32resource
ms.date: 03/13/2018
f1_keywords:
- -win32resource
- win32resource
helpviewer_keywords:
- /win32resource compiler option [Visual Basic]
- -win32resource compiler option [Visual Basic]
- win32resource compiler option [Visual Basic]
ms.assetid: e226946d-19ce-4cc9-91f5-aed24f77aa2b
ms.openlocfilehash: 9351e9f6bcb7660dac2c49667ca8db6d578eff7c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774762"
---
# <a name="-win32resource"></a><span data-ttu-id="69739-102">-win32resource</span><span class="sxs-lookup"><span data-stu-id="69739-102">-win32resource</span></span>
<span data-ttu-id="69739-103">Insère un fichier de ressources Win32 dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="69739-103">Inserts a Win32 resource file in the output file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69739-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69739-104">Syntax</span></span>  
  
```  
-win32resource:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="69739-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="69739-105">Arguments</span></span>  
 `filename`  
 <span data-ttu-id="69739-106">Le nom du fichier de ressources à ajouter à votre fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="69739-106">The name of the resource file to add to your output file.</span></span> <span data-ttu-id="69739-107">Placez le nom de fichier entre guillemets ( » «) s’il contient un espace.</span><span class="sxs-lookup"><span data-stu-id="69739-107">Enclose the file name in quotation marks (" ") if it contains a space.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="69739-108">Notes</span><span class="sxs-lookup"><span data-stu-id="69739-108">Remarks</span></span>  
 <span data-ttu-id="69739-109">Vous pouvez créer un fichier de ressources Win32 avec le compilateur de ressources (RC) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="69739-109">You can create a Win32 resource file with the Microsoft Windows Resource Compiler (RC).</span></span>  
  
 <span data-ttu-id="69739-110">Une ressource Win32 peut contenir la version ou des informations de bitmap (icône) qui vous aide à identifier votre application dans **Explorateur de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="69739-110">A Win32 resource can contain version or bitmap (icon) information that helps identify your application in **File Explorer**.</span></span> <span data-ttu-id="69739-111">Si vous ne spécifiez pas `-win32resource`, le compilateur génère des informations de version en fonction de la version d’assembly.</span><span class="sxs-lookup"><span data-stu-id="69739-111">If you do not specify `-win32resource`, the compiler generates version information based on the assembly version.</span></span> <span data-ttu-id="69739-112">Le `-win32resource` et `-win32icon` options s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="69739-112">The `-win32resource` and `-win32icon` options are mutually exclusive.</span></span>  
  
 <span data-ttu-id="69739-113">Consultez [- linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md) pour référencer un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fichier de ressources, ou [-ressources (Visual Basic)](../../../visual-basic/reference/command-line-compiler/resource.md) pour attacher un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="69739-113">See [-linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md) to reference a [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] resource file, or [-resource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/resource.md) to attach a [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] resource file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="69739-114">Le `-win32resource` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="69739-114">The `-win32resource` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="69739-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="69739-115">Example</span></span>  
 <span data-ttu-id="69739-116">Le code suivant compile `In.vb` et attache un fichier de ressources Win32, `Rf.res`:</span><span class="sxs-lookup"><span data-stu-id="69739-116">The following code compiles `In.vb` and attaches a Win32 resource file, `Rf.res`:</span></span>  
  
```console  
vbc -win32resource:rf.res in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="69739-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69739-117">See also</span></span>

- [<span data-ttu-id="69739-118">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="69739-118">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="69739-119">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="69739-119">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
