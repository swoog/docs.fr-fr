---
title: -nostdlib (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /nostdlib
helpviewer_keywords:
- nostdlib compiler option [C#]
- -nostdlib compiler option [C#]
- /nostdlib compiler option [C#]
ms.assetid: ec197989-fa49-4725-a455-e06b551eb65f
ms.openlocfilehash: 1dc0ab70ca28626c4a3f505c13ec1d6f828a4b05
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33216133"
---
# <a name="-nostdlib-c-compiler-options"></a><span data-ttu-id="dd4b3-102">-nostdlib (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="dd4b3-102">-nostdlib (C# Compiler Options)</span></span>
<span data-ttu-id="dd4b3-103">**-nostdlib** empêche l’importation du fichier mscorlib.dll, qui définit l’espace de noms System tout entier.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-103">**-nostdlib** prevents the import of mscorlib.dll, which defines the entire System namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd4b3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd4b3-104">Syntax</span></span>  
  
```console  
-nostdlib[+ | -]  
```  
  
## <a name="remarks"></a><span data-ttu-id="dd4b3-105">Notes</span><span class="sxs-lookup"><span data-stu-id="dd4b3-105">Remarks</span></span>  
 <span data-ttu-id="dd4b3-106">Utilisez cette option si vous souhaitez définir ou créer vos propres objets et espace de noms System.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-106">Use this option if you want to define or create your own System namespace and objects.</span></span>  
  
 <span data-ttu-id="dd4b3-107">Si vous ne spécifiez pas **-nostdlib**, mscorlib.dll est importé dans votre programme (ce qui équivaut à spécifier **-nostdlib-**).</span><span class="sxs-lookup"><span data-stu-id="dd4b3-107">If you do not specify **-nostdlib**, mscorlib.dll will be imported into your program (same as specifying **-nostdlib-**).</span></span> <span data-ttu-id="dd4b3-108">Les options **-nostdlib** et **-nostdlib+** sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-108">Specifying **-nostdlib** is the same as specifying **-nostdlib+**.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="dd4b3-109">Pour définir cette option du compilateur dans l'environnement de développement Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dd4b3-109">To set this compiler option in the Visual Studio development environment</span></span>  
  
1.  <span data-ttu-id="dd4b3-110">Ouvrez la page **Propriétés** du projet.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-110">Open the **Properties** page for the project.</span></span>  
  
2.  <span data-ttu-id="dd4b3-111">Cliquez sur la page de propriétés **Générer** .</span><span class="sxs-lookup"><span data-stu-id="dd4b3-111">Click the **Build** properties page.</span></span>  
  
3.  <span data-ttu-id="dd4b3-112">Cliquez sur le bouton **Avancées** .</span><span class="sxs-lookup"><span data-stu-id="dd4b3-112">Click the **Advanced** button.</span></span>  
  
4.  <span data-ttu-id="dd4b3-113">Modifiez la propriété **Ne pas référencer mscorlib.dll** .</span><span class="sxs-lookup"><span data-stu-id="dd4b3-113">Modify the **Do not reference mscorlib.dll** property.</span></span>  
  
 <span data-ttu-id="dd4b3-114">Pour plus d’informations sur la définition de cette option du compilateur par programmation, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.NoStdLib%2A>.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-114">For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.NoStdLib%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd4b3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd4b3-115">See Also</span></span>  
 [<span data-ttu-id="dd4b3-116">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="dd4b3-116">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
