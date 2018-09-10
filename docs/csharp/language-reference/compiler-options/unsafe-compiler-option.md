---
title: -unsafe (Options du compilateur C#)
ms.date: 04/25/2018
f1_keywords:
- /unsafe
helpviewer_keywords:
- -unsafe compiler option [C#]
- unsafe compiler option [C#]
- /unsafe compiler option [C#]
ms.openlocfilehash: 138c7cce83fd069f44025c57e52b2d01bcb23432
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43518048"
---
# <a name="-unsafe-c-compiler-options"></a><span data-ttu-id="26c60-102">-unsafe (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="26c60-102">-unsafe (C# Compiler Options)</span></span>
<span data-ttu-id="26c60-103">L’option de compilateur **-unsafe** permet la compilation de code utilisant le mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="26c60-103">The **-unsafe** compiler option allows code that uses the [unsafe](../../../csharp/language-reference/keywords/unsafe.md) keyword to compile.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26c60-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26c60-104">Syntax</span></span>  
  
```console  
-unsafe  
```  
  
## <a name="remarks"></a><span data-ttu-id="26c60-105">Notes</span><span class="sxs-lookup"><span data-stu-id="26c60-105">Remarks</span></span>  
 <span data-ttu-id="26c60-106">Pour plus d’informations sur le code unsafe, consultez [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md).</span><span class="sxs-lookup"><span data-stu-id="26c60-106">For more information about unsafe code, see [Unsafe Code and Pointers](../../../csharp/programming-guide/unsafe-code-pointers/index.md).</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="26c60-107">Pour définir cette option du compilateur dans l'environnement de développement Visual Studio</span><span class="sxs-lookup"><span data-stu-id="26c60-107">To set this compiler option in the Visual Studio development environment</span></span>  
  
1.  <span data-ttu-id="26c60-108">Ouvrez la page **Propriétés** du projet.</span><span class="sxs-lookup"><span data-stu-id="26c60-108">Open the project's **Properties** page.</span></span>  
  
2.  <span data-ttu-id="26c60-109">Cliquez sur la page de propriétés **Générer**.</span><span class="sxs-lookup"><span data-stu-id="26c60-109">Click the **Build** property page.</span></span>  
  
3.  <span data-ttu-id="26c60-110">Cochez la case **Autoriser le code unsafe**.</span><span class="sxs-lookup"><span data-stu-id="26c60-110">Select the **Allow Unsafe Code** check box.</span></span>  
  
### <a name="to-add-this-option-in-a-csproj-file"></a><span data-ttu-id="26c60-111">Pour ajouter cette option dans un fichier csproj</span><span class="sxs-lookup"><span data-stu-id="26c60-111">To add this option in a csproj file</span></span>

<span data-ttu-id="26c60-112">Ouvrez le fichier .csproj d’un projet et ajoutez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="26c60-112">Open the .csproj file for a project, and add the following elements:</span></span>

```xml
  <PropertyGroup>
    <AllowUnsafeBlocks>true</AllowUnsafeBlocks>
  </PropertyGroup>
```

 <span data-ttu-id="26c60-113">Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>.</span><span class="sxs-lookup"><span data-stu-id="26c60-113">For information about how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="26c60-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="26c60-114">Example</span></span>  
 <span data-ttu-id="26c60-115">Compilez `in.cs` selon le mode non sécurisé :</span><span class="sxs-lookup"><span data-stu-id="26c60-115">Compile `in.cs` for unsafe mode:</span></span>  
  
```console  
csc -unsafe in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="26c60-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c60-116">See Also</span></span>  

- [<span data-ttu-id="26c60-117">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="26c60-117">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
- [<span data-ttu-id="26c60-118">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="26c60-118">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
