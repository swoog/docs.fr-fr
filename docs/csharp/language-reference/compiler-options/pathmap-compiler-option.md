---
title: -pathmap (Options du compilateur C#)
ms.date: 05/16/2018
f1_keywords:
- /pathmap
helpviewer_keywords:
- -pathmap compiler option [C#]
- pathmap compiler option [C#]
- /pathmap compiler option [C#]
ms.openlocfilehash: 36196ffea19cfde7ff5f830ea358d2bd83edf419
ms.sourcegitcommit: 77d9a94dac4c05827ed0663d95e0f9ad35d6682e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2018
ms.locfileid: "34472812"
---
# <a name="-pathmap-c-compiler-options"></a><span data-ttu-id="ed68e-102">-pathmap (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="ed68e-102">-pathmap (C# Compiler Options)</span></span>

<span data-ttu-id="ed68e-103">L’option de compilateur **-pathmap** spécifie comment mapper des chemins physiques aux noms de chemin source générés en sortie par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="ed68e-103">The **-pathmap** compiler option specifies how to map physical paths to source path names output by the compiler.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed68e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed68e-104">Syntax</span></span>

```console
-pathmap:path1=sourcePath1,path2=sourcePath2
```

## <a name="arguments"></a><span data-ttu-id="ed68e-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="ed68e-105">Arguments</span></span>

 <span data-ttu-id="ed68e-106">`path1` : chemin complet aux fichiers sources dans l’environnement actuel</span><span class="sxs-lookup"><span data-stu-id="ed68e-106">`path1` The full path to the source files in the current environment</span></span>

 <span data-ttu-id="ed68e-107">`sourcePath1` : chemin source remplaçant `path1` dans les fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="ed68e-107">`sourcePath1` The source path substituted for `path1` in any output files.</span></span>

<span data-ttu-id="ed68e-108">Pour spécifier plusieurs chemins sources mappés, séparez-les par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ed68e-108">To specify multiple mapped source paths, separate each with a comma.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed68e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ed68e-109">Remarks</span></span>

<span data-ttu-id="ed68e-110">Le compilateur écrit le chemin source dans sa sortie dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="ed68e-110">The compiler writes the source path path into its output for the following reasons:</span></span>

1. <span data-ttu-id="ed68e-111">Le chemin source est remplacé par un argument quand <xref:System.Runtime.CompilerServices.CallerFilePathAttribute> est appliqué à un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="ed68e-111">The source path is substituted for an argument when the <xref:System.Runtime.CompilerServices.CallerFilePathAttribute> is applied to an optional parameter.</span></span>
1. <span data-ttu-id="ed68e-112">Le chemin source est incorporé dans un fichier PDB.</span><span class="sxs-lookup"><span data-stu-id="ed68e-112">The source path is embedded in a PDB file.</span></span>
1. <span data-ttu-id="ed68e-113">Le chemin du fichier PDB est incorporé dans un fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="ed68e-113">The path of the PDB file is embedded into a PE (portable executable) file.</span></span>

<span data-ttu-id="ed68e-114">Cette option mappe chaque chemin physique de l’ordinateur sur lequel le compilateur s’exécute à un chemin correspondant qui doit être écrit dans les fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="ed68e-114">This option maps each physical path on the machine where the compiler runs to a corresponding path that should be written in the output files.</span></span>

## <a name="example"></a><span data-ttu-id="ed68e-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed68e-115">Example</span></span>

<span data-ttu-id="ed68e-116">Compilez `t.cs` dans le répertoire **C:\\work\\tests** et mappez ce répertoire à **\publish** dans la sortie :</span><span class="sxs-lookup"><span data-stu-id="ed68e-116">Compile `t.cs` in the directory **C:\\work\\tests** and map that directory to **\publish** in the output:</span></span>

```console
csc -pathmap:C:\work\tests=\publish t.cs
```

## <a name="see-also"></a><span data-ttu-id="ed68e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed68e-117">See also</span></span>

 [<span data-ttu-id="ed68e-118">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="ed68e-118">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
 [<span data-ttu-id="ed68e-119">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="ed68e-119">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
