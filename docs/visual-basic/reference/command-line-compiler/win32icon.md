---
title: -win32icon
ms.date: 03/13/2018
helpviewer_keywords:
- win32icon compiler option [Visual Basic]
- -win32icon compiler option [Visual Basic]
- /win32icon compiler option [Visual Basic]
ms.assetid: aecaab01-9353-46c5-941c-6edabd4eff92
ms.openlocfilehash: afc35578f362f4a72a40fdb3d87406a8795cb59d
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194863"
---
# <a name="-win32icon"></a><span data-ttu-id="a8384-102">-win32icon</span><span class="sxs-lookup"><span data-stu-id="a8384-102">-win32icon</span></span>
<span data-ttu-id="a8384-103">Insère un fichier .ico dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="a8384-103">Inserts an .ico file in the output file.</span></span> <span data-ttu-id="a8384-104">Ce fichier .ico représente le fichier de sortie dans **Explorateur de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="a8384-104">This .ico file represents the output file in **File Explorer**.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8384-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8384-105">Syntax</span></span>  
  
```  
-win32icon:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="a8384-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="a8384-106">Arguments</span></span>  
  
|<span data-ttu-id="a8384-107">Terme</span><span class="sxs-lookup"><span data-stu-id="a8384-107">Term</span></span>|<span data-ttu-id="a8384-108">Définition</span><span class="sxs-lookup"><span data-stu-id="a8384-108">Definition</span></span>|  
|---|---|  
|`filename`|<span data-ttu-id="a8384-109">Le fichier .ico à ajouter à votre fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="a8384-109">The .ico file to add to your output file.</span></span> <span data-ttu-id="a8384-110">Placez le nom de fichier entre guillemets ( » «) s’il contient un espace.</span><span class="sxs-lookup"><span data-stu-id="a8384-110">Enclose the file name in quotation marks (" ") if it contains a space.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a8384-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a8384-111">Remarks</span></span>  
 <span data-ttu-id="a8384-112">Vous pouvez créer un fichier .ico avec le compilateur de ressources (RC) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a8384-112">You can create an .ico file with the Microsoft Windows Resource Compiler (RC).</span></span> <span data-ttu-id="a8384-113">Le compilateur de ressources est appelé lorsque vous compilez un programme Visual C++ ; un fichier .ico est créé à partir du fichier .rc.</span><span class="sxs-lookup"><span data-stu-id="a8384-113">The resource compiler is invoked when you compile a Visual C++ program; an .ico file is created from the .rc file.</span></span> <span data-ttu-id="a8384-114">Le `-win32icon` et `-win32resource` options s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="a8384-114">The `-win32icon` and `-win32resource` options are mutually exclusive.</span></span>  
  
 <span data-ttu-id="a8384-115">Consultez [- linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md) pour référencer un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fichier de ressources, ou [-ressources (Visual Basic)](../../../visual-basic/reference/command-line-compiler/resource.md) pour attacher un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="a8384-115">See [-linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md) to reference a [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] resource file, or [-resource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/resource.md) to attach a [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] resource file.</span></span> <span data-ttu-id="a8384-116">Consultez [-win32resource](../../../visual-basic/reference/command-line-compiler/win32resource.md) pour importer un fichier .res.</span><span class="sxs-lookup"><span data-stu-id="a8384-116">See [-win32resource](../../../visual-basic/reference/command-line-compiler/win32resource.md) to import a .res file.</span></span>  
  
|<span data-ttu-id="a8384-117">Pour définir - win32icon dans l’IDE Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8384-117">To set -win32icon in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="a8384-118">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="a8384-118">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="a8384-119">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a8384-119">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="a8384-120">2.  Cliquez sur l’onglet **Application** .</span><span class="sxs-lookup"><span data-stu-id="a8384-120">2.  Click the **Application** tab.</span></span><br /><span data-ttu-id="a8384-121">3.  Modifiez la valeur dans le **icône** boîte.</span><span class="sxs-lookup"><span data-stu-id="a8384-121">3.  Modify the value in the **Icon** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a8384-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8384-122">Example</span></span>  
 <span data-ttu-id="a8384-123">Le code suivant compile `In.vb` et attache un fichier .ico, `Rf.ico`.</span><span class="sxs-lookup"><span data-stu-id="a8384-123">The following code compiles `In.vb` and attaches an .ico file, `Rf.ico`.</span></span>  
  
```console
vbc -win32icon:rf.ico in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="a8384-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8384-124">See Also</span></span>  
 [<span data-ttu-id="a8384-125">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a8384-125">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="a8384-126">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="a8384-126">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
