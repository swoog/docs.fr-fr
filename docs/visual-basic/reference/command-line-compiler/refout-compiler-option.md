---
title: -refout (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- /refout
helpviewer_keywords:
- refout compiler option [Visual Basic]
- /refout compiler option [Visual Basic]
- -refout compiler option [Visual Basic]
ms.openlocfilehash: 3d7f5f9065ba53bd037d7307f62c9acad913b8e9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54638702"
---
# <a name="-refout-visual-basic"></a><span data-ttu-id="def49-102">-refout (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="def49-102">-refout (Visual Basic)</span></span>

<span data-ttu-id="def49-103">L’option **-refout** spécifie un chemin de fichier où l’assembly de référence doit être généré.</span><span class="sxs-lookup"><span data-stu-id="def49-103">The **-refout** option specifies a file path where the reference assembly should be output.</span></span>

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a><span data-ttu-id="def49-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="def49-104">Syntax</span></span>

```console
-refout:filepath
```

## <a name="arguments"></a><span data-ttu-id="def49-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="def49-105">Arguments</span></span>

 <span data-ttu-id="def49-106">`filepath` Le chemin d’accès et le nom de l’assembly de référence.</span><span class="sxs-lookup"><span data-stu-id="def49-106">`filepath` The path and filename of the reference assembly.</span></span> <span data-ttu-id="def49-107">En règle générale, il doit être dans un sous-dossier de l’assembly principal.</span><span class="sxs-lookup"><span data-stu-id="def49-107">It should generally be in a sub-folder of the primary assembly.</span></span> <span data-ttu-id="def49-108">La convention recommandée (utilisée par MSBuild) consiste à placer l’assembly de référence dans un sous-dossier « ref/ » par rapport à l’assembly principal.</span><span class="sxs-lookup"><span data-stu-id="def49-108">The recommended convention (used by MSBuild) is to place the reference assembly in a "ref/" sub-folder relative to the primary assembly.</span></span> <span data-ttu-id="def49-109">Tous les dossiers `filepath` doit exister ; le compilateur ne crée pas les.</span><span class="sxs-lookup"><span data-stu-id="def49-109">All folders in `filepath` must exist; the compiler does not create them.</span></span> 

## <a name="remarks"></a><span data-ttu-id="def49-110">Notes</span><span class="sxs-lookup"><span data-stu-id="def49-110">Remarks</span></span>

<span data-ttu-id="def49-111">Visual Basic prend en charge la `-refout` basculer à partir de la version 15.3.</span><span class="sxs-lookup"><span data-stu-id="def49-111">Visual Basic supports the `-refout` switch starting with version 15.3.</span></span>

<span data-ttu-id="def49-112">Assemblys de référence sont des assemblys de métadonnées uniquement qui contiennent des métadonnées, mais aucun code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="def49-112">Reference assemblies are metadata-only assemblies that contain metadata but no implementation code.</span></span> <span data-ttu-id="def49-113">Elles incluent des informations de membre et de type pour tout sauf les types anonymes.</span><span class="sxs-lookup"><span data-stu-id="def49-113">They include type and member information for everything except anonymous types.</span></span> <span data-ttu-id="def49-114">Leurs corps de méthode sont remplacés par un seul `throw null` instruction.</span><span class="sxs-lookup"><span data-stu-id="def49-114">Their method bodies are replaced with a single `throw null` statement.</span></span> <span data-ttu-id="def49-115">La raison pour l’utilisation de `throw null` corps de méthode (par opposition à aucun corps) est de pouvoir les PEVerify peut exécuter et passer (valider ainsi l’exhaustivité des métadonnées).</span><span class="sxs-lookup"><span data-stu-id="def49-115">The reason for using `throw null` method bodies (as opposed to no bodies) is so that PEVerify can run and pass (thus validating the completeness of the metadata).</span></span>

<span data-ttu-id="def49-116">Assemblys de référence incluent un niveau de l’assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut.</span><span class="sxs-lookup"><span data-stu-id="def49-116">Reference assemblies include an assembly-level [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribute.</span></span> <span data-ttu-id="def49-117">Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser).</span><span class="sxs-lookup"><span data-stu-id="def49-117">This attribute may be specified in source (then the compiler won't need to synthesize it).</span></span> <span data-ttu-id="def49-118">En raison de cet attribut, runtimes refusent de charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement).</span><span class="sxs-lookup"><span data-stu-id="def49-118">Because of this attribute, runtimes refuse to load reference assemblies for execution (but they can still be loaded in a reflection-only context).</span></span> <span data-ttu-id="def49-119">Les outils reflétés dans les assemblys doivent absolument que charger les assemblys de référence en mode réflexion uniquement ; Sinon, le runtime lève un <xref:System.BadImageFormatException>.</span><span class="sxs-lookup"><span data-stu-id="def49-119">Tools that reflect on assemblies need to ensure they load reference assemblies as reflection-only; otherwise, the runtime throws a <xref:System.BadImageFormatException>.</span></span>

<span data-ttu-id="def49-120">Les options `-refout` et [`-refonly`](refonly-compiler-option.md) s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="def49-120">The `-refout` and [`-refonly`](refonly-compiler-option.md) options are mutually exclusive.</span></span>

## <a name="see-also"></a><span data-ttu-id="def49-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="def49-121">See also</span></span>
- [<span data-ttu-id="def49-122">-refonly</span><span class="sxs-lookup"><span data-stu-id="def49-122">-refonly</span></span>](refonly-compiler-option.md)
- [<span data-ttu-id="def49-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="def49-123">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="def49-124">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="def49-124">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)

