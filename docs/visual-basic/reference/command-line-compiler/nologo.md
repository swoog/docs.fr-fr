---
title: -nologo (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- -nologo compiler option [Visual Basic]
- banners [Visual Basic], suppressing startup
- nologo compiler option [Visual Basic]
- /nologo compiler option [Visual Basic]
ms.assetid: 25ef54b6-d676-4639-a2d2-a747a158bc07
ms.openlocfilehash: c1824e4a086ecdd4b6a776bd6894f6e003d02867
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789002"
---
# <a name="-nologo-visual-basic"></a><span data-ttu-id="f5458-102">-nologo (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f5458-102">-nologo (Visual Basic)</span></span>
<span data-ttu-id="f5458-103">Supprime l’affichage de la bannière de copyright et les messages d’information pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="f5458-103">Suppresses display of the copyright banner and informational messages during compilation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5458-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5458-104">Syntax</span></span>  
  
```  
-nologo  
```  
  
## <a name="remarks"></a><span data-ttu-id="f5458-105">Notes</span><span class="sxs-lookup"><span data-stu-id="f5458-105">Remarks</span></span>  
 <span data-ttu-id="f5458-106">Si vous spécifiez `-nologo`, le compilateur n’affiche pas la bannière de copyright.</span><span class="sxs-lookup"><span data-stu-id="f5458-106">If you specify `-nologo`, the compiler does not display a copyright banner.</span></span> <span data-ttu-id="f5458-107">Par défaut, l'option `-nologo` n'est pas activée.</span><span class="sxs-lookup"><span data-stu-id="f5458-107">By default, `-nologo` is not in effect.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5458-108">Le `-nologo` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f5458-108">The `-nologo` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f5458-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="f5458-109">Example</span></span>  
 <span data-ttu-id="f5458-110">Le code suivant compile `T2.vb` et n’affiche pas la bannière de copyright.</span><span class="sxs-lookup"><span data-stu-id="f5458-110">The following code compiles `T2.vb` and does not display a copyright banner.</span></span>  
  
```console
vbc -nologo t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="f5458-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5458-111">See also</span></span>

- [<span data-ttu-id="f5458-112">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f5458-112">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="f5458-113">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="f5458-113">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
