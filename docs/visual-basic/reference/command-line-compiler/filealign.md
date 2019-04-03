---
title: -filealign
ms.date: 03/10/2018
helpviewer_keywords:
- sections compiler option [Visual Basic]
- alignment compiler option [Visual Basic]
- -filealign compiler option [Visual Basic]
- section alignment
- /filealign compiler option [Visual Basic]
- filealign compiler option [Visual Basic]
ms.assetid: cc61ec3d-ad38-4b28-9659-099d73cad099
ms.openlocfilehash: 9a844515a4596064937762ac05b850463f1b5e14
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819175"
---
# <a name="-filealign"></a><span data-ttu-id="91a1d-102">-filealign</span><span class="sxs-lookup"><span data-stu-id="91a1d-102">-filealign</span></span>
<span data-ttu-id="91a1d-103">Spécifie où les sections du fichier de sortie doivent être alignées.</span><span class="sxs-lookup"><span data-stu-id="91a1d-103">Specifies where to align the sections of the output file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91a1d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91a1d-104">Syntax</span></span>  
  
```  
-filealign:number  
```  
  
## <a name="arguments"></a><span data-ttu-id="91a1d-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="91a1d-105">Arguments</span></span>  
 `number`  
 <span data-ttu-id="91a1d-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="91a1d-106">Required.</span></span> <span data-ttu-id="91a1d-107">Une valeur qui spécifie l’alignement des sections dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="91a1d-107">A value that specifies the alignment of sections in the output file.</span></span> <span data-ttu-id="91a1d-108">Les valeurs valides sont 512, 1024, 2048, 4096 et 8192.</span><span class="sxs-lookup"><span data-stu-id="91a1d-108">Valid values are 512, 1024, 2048, 4096, and 8192.</span></span> <span data-ttu-id="91a1d-109">Ces valeurs sont exprimées en octets.</span><span class="sxs-lookup"><span data-stu-id="91a1d-109">These values are in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="91a1d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="91a1d-110">Remarks</span></span>  
 <span data-ttu-id="91a1d-111">Vous pouvez utiliser la `-filealign` option pour spécifier l’alignement des sections dans votre fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="91a1d-111">You can use the `-filealign` option to specify the alignment of sections in your output file.</span></span> <span data-ttu-id="91a1d-112">Les sections sont les blocs de mémoire contiguë dans un fichier exécutable Portable (PE) qui contient le code ou des données.</span><span class="sxs-lookup"><span data-stu-id="91a1d-112">Sections are blocks of contiguous memory in a Portable Executable (PE) file that contains either code or data.</span></span> <span data-ttu-id="91a1d-113">Le `-filealign` option vous permet de compiler votre application avec un alignement non standard ; la plupart des développeurs n’avez pas besoin d’utiliser cette option.</span><span class="sxs-lookup"><span data-stu-id="91a1d-113">The `-filealign` option lets you compile your application with a nonstandard alignment; most developers do not need to use this option.</span></span>  
  
 <span data-ttu-id="91a1d-114">Chaque section est alignée sur une limite qui est un multiple de la `-filealign` valeur.</span><span class="sxs-lookup"><span data-stu-id="91a1d-114">Each section is aligned on a boundary that is a multiple of the `-filealign` value.</span></span> <span data-ttu-id="91a1d-115">Il n’existe aucune valeur fixe par défaut.</span><span class="sxs-lookup"><span data-stu-id="91a1d-115">There is no fixed default.</span></span> <span data-ttu-id="91a1d-116">Si `-filealign` n’est pas spécifié, le compilateur choisit une valeur par défaut au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="91a1d-116">If `-filealign` is not specified, the compiler picks a default at compile time.</span></span>  
  
 <span data-ttu-id="91a1d-117">En spécifiant la taille de la section, vous pouvez modifier la taille du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="91a1d-117">By specifying the section size, you can change the size of the output file.</span></span> <span data-ttu-id="91a1d-118">Il peut être utile de modifier la taille de la section pour les programmes qui sont exécutés sur des appareils de petite taille.</span><span class="sxs-lookup"><span data-stu-id="91a1d-118">Modifying section size may be useful for programs that will run on smaller devices.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="91a1d-119">Le `-filealign` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="91a1d-119">The `-filealign` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91a1d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91a1d-120">See also</span></span>

- [<span data-ttu-id="91a1d-121">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="91a1d-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
