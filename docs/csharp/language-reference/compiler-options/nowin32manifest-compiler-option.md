---
title: -nowin32manifest (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /nowin32manifest
helpviewer_keywords:
- nowin32manifest compiler option [C#]
- -nowin32manifest compiler option [C#]
- /nowin32manifest compiler option [C#]
ms.assetid: 6f06365b-b87b-46a2-b187-b3bfeaf4862d
ms.openlocfilehash: 3ab52d541c169850f6ae7ba7e7cfded290f890e7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43420617"
---
# <a name="-nowin32manifest-c-compiler-options"></a><span data-ttu-id="b35c8-102">-nowin32manifest (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="b35c8-102">-nowin32manifest (C# Compiler Options)</span></span>
<span data-ttu-id="b35c8-103">Utilisez l’option **-nowin32manifest** pour indiquer au compilateur de ne pas incorporer le manifeste de l’application dans le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="b35c8-103">Use the **-nowin32manifest** option to instruct the compiler not to embed any application manifest into the executable file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b35c8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b35c8-104">Syntax</span></span>  
  
```console  
-nowin32manifest  
```  
  
## <a name="remarks"></a><span data-ttu-id="b35c8-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b35c8-105">Remarks</span></span>  
 <span data-ttu-id="b35c8-106">Quand cette option est utilisée, l’application est soumise à la virtualisation sur Windows Vista, sauf si vous fournissez un manifeste de l’application dans un fichier de ressources Win32 ou au cours d’une étape de génération ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b35c8-106">When this option is used, the application will be subject to virtualization on Windows Vista unless you provide an application manifest in a Win32 Resource file or during a later build step.</span></span>  
  
 <span data-ttu-id="b35c8-107">Dans Visual Studio, définissez cette option dans la page de propriétés **Application** en sélectionnant l’option **Créer une application sans fichier manifeste** dans la zone de liste déroulante **Manifeste**.</span><span class="sxs-lookup"><span data-stu-id="b35c8-107">In Visual Studio, set this option in the **Application Property** page by selecting the **Create Application Without a Manifest** option in the **Manifest** drop down list.</span></span> <span data-ttu-id="b35c8-108">Pour plus d’informations, consultez [Page Application, Concepteur de projets (C#)](/visualstudio/ide/reference/application-page-project-designer-csharp).</span><span class="sxs-lookup"><span data-stu-id="b35c8-108">For more information, see [Application Page, Project Designer (C#)](/visualstudio/ide/reference/application-page-project-designer-csharp).</span></span>  
  
 <span data-ttu-id="b35c8-109">Pour plus d’informations sur la création d’un manifeste, consultez [-win32manifest (options du compilateur C#)](../../../csharp/language-reference/compiler-options/win32manifest-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="b35c8-109">For more information about manifest creation, see [-win32manifest (C# Compiler Options)](../../../csharp/language-reference/compiler-options/win32manifest-compiler-option.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b35c8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b35c8-110">See Also</span></span>  

- [<span data-ttu-id="b35c8-111">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="b35c8-111">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
- [<span data-ttu-id="b35c8-112">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="b35c8-112">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
