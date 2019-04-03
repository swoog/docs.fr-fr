---
title: -out (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- /out compiler option [Visual Basic]
- -out compiler option [Visual Basic]
- out compiler option [Visual Basic]
ms.assetid: 9f148c15-0909-4cb8-a2db-777f8a8b45ae
ms.openlocfilehash: 5dcf9dc5cc0987e965aba7fd2b8821252e19a655
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58815990"
---
# <a name="-out-visual-basic"></a><span data-ttu-id="298f9-102">-out (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="298f9-102">-out (Visual Basic)</span></span>
<span data-ttu-id="298f9-103">Spécifie le nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="298f9-103">Specifies the name of the output file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="298f9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="298f9-104">Syntax</span></span>  
  
```  
-out:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="298f9-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="298f9-105">Arguments</span></span>  
  
|<span data-ttu-id="298f9-106">Terme</span><span class="sxs-lookup"><span data-stu-id="298f9-106">Term</span></span>|<span data-ttu-id="298f9-107">Définition</span><span class="sxs-lookup"><span data-stu-id="298f9-107">Definition</span></span>|  
|---|---|  
|`filename`|<span data-ttu-id="298f9-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="298f9-108">Required.</span></span> <span data-ttu-id="298f9-109">Le nom du fichier de sortie que le compilateur crée.</span><span class="sxs-lookup"><span data-stu-id="298f9-109">The name of the output file the compiler creates.</span></span> <span data-ttu-id="298f9-110">Si le nom de fichier contient un espace, placez le nom entre guillemets ( » «).</span><span class="sxs-lookup"><span data-stu-id="298f9-110">If the file name contains a space, enclose the name in quotation marks (" ").</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="298f9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="298f9-111">Remarks</span></span>  
 <span data-ttu-id="298f9-112">Spécifiez le nom complet et l’extension de fichier à créer.</span><span class="sxs-lookup"><span data-stu-id="298f9-112">Specify the full name and extension of the file to create.</span></span> <span data-ttu-id="298f9-113">Si vous ne le faites pas, le fichier .exe tire son nom de fichier de code source contenant le `Sub Main` procédure et le fichier .dll tire son nom du premier fichier de code source.</span><span class="sxs-lookup"><span data-stu-id="298f9-113">If you do not, the .exe file takes its name from the source-code file containing the `Sub Main` procedure, and the .dll file takes its name from the first source-code file.</span></span>  
  
 <span data-ttu-id="298f9-114">Si vous spécifiez un nom de fichier sans extension .exe ou .dll, le compilateur ajoute automatiquement l’extension pour vous, en fonction de la valeur spécifiée pour le `-target` option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="298f9-114">If you specify a file name without an .exe or .dll extension, the compiler automatically adds the extension for you, depending on the value specified for the `-target` compiler option.</span></span>  
  
|<span data-ttu-id="298f9-115">Pour définir - out dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="298f9-115">To set -out in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="298f9-116">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="298f9-116">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="298f9-117">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="298f9-117">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="298f9-118">2.  Cliquez sur l’onglet **Application** .</span><span class="sxs-lookup"><span data-stu-id="298f9-118">2.  Click the **Application** tab.</span></span><br /><span data-ttu-id="298f9-119">3.  Modifiez la valeur dans le **nom de l’Assembly** boîte.</span><span class="sxs-lookup"><span data-stu-id="298f9-119">3.  Modify the value in the **Assembly Name** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="298f9-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="298f9-120">Example</span></span>  
 <span data-ttu-id="298f9-121">Le code suivant compile `T2.vb` et crée le fichier de sortie `T2.exe`.</span><span class="sxs-lookup"><span data-stu-id="298f9-121">The following code compiles `T2.vb` and creates output file `T2.exe`.</span></span>  
  
```console
vbc t2.vb -out:t3.exe  
```  
  
## <a name="see-also"></a><span data-ttu-id="298f9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="298f9-122">See also</span></span>

- [<span data-ttu-id="298f9-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="298f9-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="298f9-124">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="298f9-124">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="298f9-125">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="298f9-125">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
