---
title: -recurse (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /recurse
helpviewer_keywords:
- /recurse compiler option [C#]
- recurse compiler option [C#]
- -recurse compiler option [C#]
ms.assetid: 4e8212e5-04e3-45b1-8a42-41bc50e683b0
ms.openlocfilehash: a4a55090cf465d0eac05303392ba7500dd96ee90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54679368"
---
# <a name="-recurse-c-compiler-options"></a><span data-ttu-id="097eb-102">-recurse (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="097eb-102">-recurse (C# Compiler Options)</span></span>
<span data-ttu-id="097eb-103">L’option -recurse permet de compiler des fichiers de code source dans tous les répertoires enfants du répertoire spécifié (dir) ou du répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="097eb-103">The -recurse option enables you to compile source code files in all child directories of either the specified directory (dir) or of the project directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="097eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="097eb-104">Syntax</span></span>  
  
```console  
-recurse:[dir\]file  
```  
  
## <a name="arguments"></a><span data-ttu-id="097eb-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="097eb-105">Arguments</span></span>  
 <span data-ttu-id="097eb-106">`dir` (facultatif)</span><span class="sxs-lookup"><span data-stu-id="097eb-106">`dir` (optional)</span></span>  
 <span data-ttu-id="097eb-107">Répertoire dans lequel vous voulez commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="097eb-107">The directory in which you want the search to begin.</span></span> <span data-ttu-id="097eb-108">Si ce répertoire n’est pas spécifié, la recherche commence dans le répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="097eb-108">If this is not specified, the search begins in the project directory.</span></span>  
  
 `file`  
 <span data-ttu-id="097eb-109">Le ou les fichiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="097eb-109">The file(s) to search for.</span></span> <span data-ttu-id="097eb-110">Les caractères génériques sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="097eb-110">Wildcard characters are allowed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="097eb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="097eb-111">Remarks</span></span>  
 <span data-ttu-id="097eb-112">L’option **-recurse** permet de compiler des fichiers de code source dans tous les répertoires enfants du répertoire spécifié (`dir`) ou du répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="097eb-112">The **-recurse** option lets you compile source code files in all child directories of either the specified directory (`dir`) or of the project directory.</span></span>  
  
 <span data-ttu-id="097eb-113">Vous pouvez utiliser des caractères génériques dans un nom de fichier pour compiler tous les fichiers correspondants dans le répertoire du projet sans utiliser **-recurse**.</span><span class="sxs-lookup"><span data-stu-id="097eb-113">You can use wildcards in a file name to compile all matching files in the project directory without using **-recurse**.</span></span>  
  
 <span data-ttu-id="097eb-114">Cette option de compilateur n’est pas disponible dans Visual Studio et ne peut pas être changée par programmation.</span><span class="sxs-lookup"><span data-stu-id="097eb-114">This compiler option is unavailable in Visual Studio and cannot be changed programmatically.</span></span>  
  
## <a name="example"></a><span data-ttu-id="097eb-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="097eb-115">Example</span></span>  
 <span data-ttu-id="097eb-116">Compile tous les fichiers C# qui se trouvent dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="097eb-116">Compiles all C# files in the current directory:</span></span>  
  
```console  
csc *.cs  
```  
  
 <span data-ttu-id="097eb-117">Compile tous les fichiers C# du répertoire dir1\dir2 et de tous les sous-répertoires qui se situent en dessous de celui-ci, puis génère dir2.dll :</span><span class="sxs-lookup"><span data-stu-id="097eb-117">Compiles all of the C# files in the dir1\dir2 directory and any directories below it and generates dir2.dll:</span></span>  
  
```console  
csc -target:library -out:dir2.dll -recurse:dir1\dir2\*.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="097eb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="097eb-118">See also</span></span>

- [<span data-ttu-id="097eb-119">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="097eb-119">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
- [<span data-ttu-id="097eb-120">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="097eb-120">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
