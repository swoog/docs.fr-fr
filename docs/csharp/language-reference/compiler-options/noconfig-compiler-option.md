---
title: -noconfig (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /noconfig
helpviewer_keywords:
- /noconfig compiler option [C#]
- csc.rsp
- -noconfig compiler option [C#]
- noconfig compiler option [C#]
ms.assetid: cd26967e-e494-4c8c-b5c9-af13b2f78b2e
ms.openlocfilehash: 96321de5982a79cb073b658a84e0e580dd466539
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33214440"
---
# <a name="-noconfig-c-compiler-options"></a><span data-ttu-id="b2b00-102">-noconfig (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="b2b00-102">-noconfig (C# Compiler Options)</span></span>
<span data-ttu-id="b2b00-103">L’option **-noconfig** indique au compilateur de ne pas compiler avec le fichier csc.rsp, qui se trouve dans le même répertoire que le fichier csc.exe d’où il est chargé.</span><span class="sxs-lookup"><span data-stu-id="b2b00-103">The **-noconfig** option tells the compiler not to compile with the csc.rsp file, which is located in and loaded from the same directory as the csc.exe file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2b00-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2b00-104">Syntax</span></span>  
  
```console  
-noconfig  
```  
  
## <a name="remarks"></a><span data-ttu-id="b2b00-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b2b00-105">Remarks</span></span>  
 <span data-ttu-id="b2b00-106">Le fichier csc.rsp fait référence à tous les assemblys fournis avec le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b2b00-106">The csc.rsp file references all the assemblies shipped with the .NET Framework.</span></span> <span data-ttu-id="b2b00-107">Les références réelles qui sont incluses dans l’environnement de développement Visual Studio .NET varient en fonction du type de projet.</span><span class="sxs-lookup"><span data-stu-id="b2b00-107">The actual references that the Visual Studio .NET development environment includes depend on the project type.</span></span>  
  
 <span data-ttu-id="b2b00-108">Vous pouvez modifier le fichier csc.rsp et spécifier les options de compilateur supplémentaires qui doivent être incluses dans chaque compilation avec csc.exe par le biais de la ligne de commande (à l’exception de l’option **-noconfig**).</span><span class="sxs-lookup"><span data-stu-id="b2b00-108">You can modify the csc.rsp file and specify additional compiler options that should be included in every compilation from the command line with csc.exe (except the **-noconfig** option).</span></span>  
  
 <span data-ttu-id="b2b00-109">Le compilateur traite les options passées à la commande **csc** en dernier.</span><span class="sxs-lookup"><span data-stu-id="b2b00-109">The compiler processes the options passed to the **csc** command last.</span></span> <span data-ttu-id="b2b00-110">De ce fait, toute option sur la ligne de commande se substitue au paramètre de la même option dans le fichier csc.rsp.</span><span class="sxs-lookup"><span data-stu-id="b2b00-110">Therefore, any option on the command line overrides the setting of the same option in the csc.rsp file.</span></span>  
  
 <span data-ttu-id="b2b00-111">Si vous ne voulez pas que le compilateur recherche et utilise les paramètres du fichier csc.rsp, spécifiez **-noconfig**.</span><span class="sxs-lookup"><span data-stu-id="b2b00-111">If you do not want the compiler to look for and use the settings in the csc.rsp file, specify **-noconfig**.</span></span>  
  
 <span data-ttu-id="b2b00-112">Cette option de compilateur n’est pas disponible dans Visual Studio et ne peut pas être changée par programmation.</span><span class="sxs-lookup"><span data-stu-id="b2b00-112">This compiler option is unavailable in Visual Studio and cannot be changed programmatically.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2b00-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2b00-113">See Also</span></span>  
 [<span data-ttu-id="b2b00-114">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="b2b00-114">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
 [<span data-ttu-id="b2b00-115">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="b2b00-115">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
