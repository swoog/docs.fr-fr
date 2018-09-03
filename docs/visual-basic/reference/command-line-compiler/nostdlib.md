---
title: -nostdlib (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- nostdlib compiler option [Visual Basic]
- -nostdlib compiler option [Visual Basic]
- /nostdlib compiler option [Visual Basic]
ms.assetid: 140381b8-dc96-4ad5-ae11-792c9ed0be4d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3764409f13a00f6d8a050bfbdd0f59e537a5ded3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43456290"
---
# <a name="-nostdlib-visual-basic"></a><span data-ttu-id="4ef9f-102">-nostdlib (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4ef9f-102">-nostdlib (Visual Basic)</span></span>
<span data-ttu-id="4ef9f-103">Indique au compilateur pour ne pas automatiquement de référencer les bibliothèques standards.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-103">Causes the compiler not to automatically reference the standard libraries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ef9f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ef9f-104">Syntax</span></span>  
  
```  
-nostdlib  
```  
  
## <a name="remarks"></a><span data-ttu-id="4ef9f-105">Notes</span><span class="sxs-lookup"><span data-stu-id="4ef9f-105">Remarks</span></span>  
 <span data-ttu-id="4ef9f-106">Le `-nostdlib` option supprime la référence automatique à l’assembly System.dll et empêche le compilateur de lire le fichier Vbc.rsp.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-106">The `-nostdlib` option removes the automatic reference to the System.dll assembly and prevents the compiler from reading the Vbc.rsp file.</span></span> <span data-ttu-id="4ef9f-107">Le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe, référence couramment utilisées [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblys et des importations le `System` et `Microsoft.VisualBasic` espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-107">The Vbc.rsp file, which is located in the same directory as the Vbc.exe file, references the commonly used [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblies and imports the `System` and `Microsoft.VisualBasic` namespaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4ef9f-108">Les assemblys Mscorlib.dll et de Microsoft.VisualBasic.dll sont toujours référencés.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-108">The Mscorlib.dll and Microsoft.VisualBasic.dll assemblies are always referenced.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4ef9f-109">Le `-nostdlib` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-109">The `-nostdlib` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4ef9f-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="4ef9f-110">Example</span></span>  
 <span data-ttu-id="4ef9f-111">Le code suivant compile `T2.vb` sans référencer les bibliothèques standards.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-111">The following code compiles `T2.vb` without referencing the standard libraries.</span></span> <span data-ttu-id="4ef9f-112">Vous devez définir le `_MYTYPE` constante de compilation conditionnelle à la chaîne « Vide » si vous souhaitez supprimer le `My` objet.</span><span class="sxs-lookup"><span data-stu-id="4ef9f-112">You must set the `_MYTYPE` conditional-compilation constant to the string "Empty" to remove the `My` object.</span></span>  
  
```console
vbc -nostdlib -define:_MYTYPE=\"Empty\" T2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="4ef9f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ef9f-113">See Also</span></span>  
 [<span data-ttu-id="4ef9f-114">-noconfig</span><span class="sxs-lookup"><span data-stu-id="4ef9f-114">-noconfig</span></span>](../../../visual-basic/reference/command-line-compiler/noconfig.md)  
 [<span data-ttu-id="4ef9f-115">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4ef9f-115">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="4ef9f-116">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="4ef9f-116">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="4ef9f-117">Personnalisation de la disponibilité ou non des objets dans My</span><span class="sxs-lookup"><span data-stu-id="4ef9f-117">Customizing Which Objects are Available in My</span></span>](../../../visual-basic/developing-apps/customizing-extending-my/customizing-which-objects-are-available-in-my.md)
