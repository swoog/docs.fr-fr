---
title: -unsafe (Options du compilateur C#)
ms.date: 04/25/2018
f1_keywords:
- /unsafe
helpviewer_keywords:
- -unsafe compiler option [C#]
- unsafe compiler option [C#]
- /unsafe compiler option [C#]
ms.openlocfilehash: 4cfd7c82bc2cbf816164b235642c0647eeb7e5b6
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59337329"
---
# <a name="-unsafe-c-compiler-options"></a><span data-ttu-id="e84c7-102">-unsafe (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="e84c7-102">-unsafe (C# Compiler Options)</span></span>
<span data-ttu-id="e84c7-103">L’option de compilateur **-unsafe** permet la compilation de code utilisant le mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="e84c7-103">The **-unsafe** compiler option allows code that uses the [unsafe](../../../csharp/language-reference/keywords/unsafe.md) keyword to compile.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e84c7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e84c7-104">Syntax</span></span>  
  
```console  
-unsafe  
```  
  
## <a name="remarks"></a><span data-ttu-id="e84c7-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e84c7-105">Remarks</span></span>  
 <span data-ttu-id="e84c7-106">Pour plus d’informations sur le code unsafe, consultez [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md).</span><span class="sxs-lookup"><span data-stu-id="e84c7-106">For more information about unsafe code, see [Unsafe Code and Pointers](../../../csharp/programming-guide/unsafe-code-pointers/index.md).</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="e84c7-107">Pour définir cette option du compilateur dans l'environnement de développement Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e84c7-107">To set this compiler option in the Visual Studio development environment</span></span>  
  
1. <span data-ttu-id="e84c7-108">Ouvrez la page **Propriétés** du projet.</span><span class="sxs-lookup"><span data-stu-id="e84c7-108">Open the project's **Properties** page.</span></span>  
  
2. <span data-ttu-id="e84c7-109">Cliquez sur la page de propriétés **Générer**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-109">Click the **Build** property page.</span></span>  
  
3. <span data-ttu-id="e84c7-110">Cochez la case **Autoriser le code unsafe**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-110">Select the **Allow Unsafe Code** check box.</span></span>  
  
### <a name="to-add-this-option-in-a-csproj-file"></a><span data-ttu-id="e84c7-111">Pour ajouter cette option dans un fichier csproj</span><span class="sxs-lookup"><span data-stu-id="e84c7-111">To add this option in a csproj file</span></span>

<span data-ttu-id="e84c7-112">Ouvrez le fichier .csproj d’un projet et ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e84c7-112">Open the .csproj file for a project, and add the following elements:</span></span>

```xml
  <PropertyGroup>
    <AllowUnsafeBlocks>true</AllowUnsafeBlocks>
  </PropertyGroup>
```

 <span data-ttu-id="e84c7-113">Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>.</span><span class="sxs-lookup"><span data-stu-id="e84c7-113">For information about how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e84c7-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="e84c7-114">Example</span></span>  
 <span data-ttu-id="e84c7-115">Compilez `in.cs` selon le mode non sécurisé :</span><span class="sxs-lookup"><span data-stu-id="e84c7-115">Compile `in.cs` for unsafe mode:</span></span>  
  
```console  
csc -unsafe in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="e84c7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e84c7-116">See also</span></span>

- [<span data-ttu-id="e84c7-117">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="e84c7-117">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
- [<span data-ttu-id="e84c7-118">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="e84c7-118">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
