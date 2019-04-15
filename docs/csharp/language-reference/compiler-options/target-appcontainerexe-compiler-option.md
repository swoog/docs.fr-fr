---
title: -target:appcontainerexe (Options du compilateur C#)
ms.date: 07/20/2015
ms.assetid: e7e62229-23ea-4e53-bef5-380d951bf95f
ms.openlocfilehash: b3819c0582c414e1f1e3b75ab5bfe517873a1eb3
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59311069"
---
# <a name="-targetappcontainerexe-c-compiler-options"></a><span data-ttu-id="9012d-102">-target:appcontainerexe (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="9012d-102">-target:appcontainerexe (C# Compiler Options)</span></span>
<span data-ttu-id="9012d-103">Si vous utilisez l’option du compilateur **-target:appcontainerexe**, le compilateur crée un fichier exécutable Windows (.exe) qui doit être exécuté dans un conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="9012d-103">If you use the **-target:appcontainerexe** compiler option, the compiler creates a Windows executable (.exe) file that must be run in an app container.</span></span> <span data-ttu-id="9012d-104">Cette option est équivalente à [-target:winexe](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md), mais elle est destinée aux applications [!INCLUDE[win8_appname_long](~/includes/win8-appname-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9012d-104">This option is equivalent to [-target:winexe](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md) but is designed for [!INCLUDE[win8_appname_long](~/includes/win8-appname-long-md.md)] apps.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9012d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9012d-105">Syntax</span></span>  
  
```console  
-target:appcontainerexe  
```  
  
## <a name="remarks"></a><span data-ttu-id="9012d-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="9012d-106">Remarks</span></span>  
 <span data-ttu-id="9012d-107">Pour exiger que l’application s’exécute dans un conteneur d’application, cette option définit un bit dans le fichier [Portable Executable](/windows/desktop/Debug/pe-format) (PE).</span><span class="sxs-lookup"><span data-stu-id="9012d-107">To require the app to run in an app container, this option sets a bit in the [Portable Executable](/windows/desktop/Debug/pe-format) (PE) file.</span></span> <span data-ttu-id="9012d-108">Lorsque ce bit est défini, une erreur se produit si la méthode CreateProcess tente de lancer l'exécutable en dehors d'un conteneur d'application.</span><span class="sxs-lookup"><span data-stu-id="9012d-108">When that bit is set, an error occurs if the CreateProcess method tries to launch the executable file outside an app container.</span></span>  
  
 <span data-ttu-id="9012d-109">À moins que vous utilisiez l’option [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md), le fichier de sortie prend le nom du fichier d’entrée qui contient la méthode [Main](../../../csharp/programming-guide/main-and-command-args/index.md).</span><span class="sxs-lookup"><span data-stu-id="9012d-109">Unless you use the [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md) option, the output file name takes the name of the input file that contains the [Main](../../../csharp/programming-guide/main-and-command-args/index.md) method.</span></span>  
  
 <span data-ttu-id="9012d-110">Quand vous spécifiez cette option à une invite de commandes, tous les fichiers jusqu’à l’option **-out** ou **-target** suivante sont utilisés pour créer le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="9012d-110">When you specify this option at a command prompt, all files until the next **-out** or **-target** option are used to create the executable file.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-ide"></a><span data-ttu-id="9012d-111">Pour définir cette option du compilateur dans l'IDE</span><span class="sxs-lookup"><span data-stu-id="9012d-111">To set this compiler option in the IDE</span></span>  
  
1. <span data-ttu-id="9012d-112">Dans l’**Explorateur de solutions**, ouvrez le menu contextuel de votre projet et choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="9012d-112">In **Solution Explorer**, open the shortcut menu for your project, and then choose **Properties**.</span></span>  
  
2. <span data-ttu-id="9012d-113">Sous l’onglet **Application**, dans la liste **Type de sortie**, choisissez **Application Windows Store**.</span><span class="sxs-lookup"><span data-stu-id="9012d-113">On the **Application** tab, in the **Output type** list, choose **Windows Store App**.</span></span>  
  
     <span data-ttu-id="9012d-114">Cette option est disponible uniquement pour les modèles d'applications [!INCLUDE[win8_appname_long](~/includes/win8-appname-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9012d-114">This option is available only for [!INCLUDE[win8_appname_long](~/includes/win8-appname-long-md.md)] app templates.</span></span>  
  
 <span data-ttu-id="9012d-115">Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.</span><span class="sxs-lookup"><span data-stu-id="9012d-115">For information about how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9012d-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="9012d-116">Example</span></span>  
 <span data-ttu-id="9012d-117">La commande suivante compile `filename.cs` dans un fichier exécutable Windows qui peut être exécuté uniquement dans un conteneur d'application.</span><span class="sxs-lookup"><span data-stu-id="9012d-117">The following command compiles `filename.cs` into a Windows executable file that can be run only in an app container.</span></span>  
  
```console  
csc -target:appcontainerexe filename.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="9012d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9012d-118">See also</span></span>

- [<span data-ttu-id="9012d-119">-target (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="9012d-119">-target (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/target-compiler-option.md)
- [<span data-ttu-id="9012d-120">-target:winexe (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="9012d-120">-target:winexe (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/target-winexe-compiler-option.md)
- [<span data-ttu-id="9012d-121">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="9012d-121">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
