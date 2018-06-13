---
title: -refonly (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- -refonly
helpviewer_keywords:
- /refonly compiler option [Visual Basic]
- -refonly compiler option [Visual Basic]
- refonly compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e8f6c15084ac9b1a07aef8a0311edfcc4a93337c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653044"
---
# <a name="-refonly-visual-basic"></a><span data-ttu-id="c9285-102">-refonly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c9285-102">-refonly (Visual Basic)</span></span>

<span data-ttu-id="c9285-103">Le **- refonly** option indique que la sortie principale de la compilation doit être un assembly de référence au lieu d’un assembly de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c9285-103">The **-refonly** option indicates that the primary output of the compilation should be a reference assembly instead of an implementation assembly.</span></span> <span data-ttu-id="c9285-104">Le paramètre `-refonly` désactive sans assistance la génération de fichiers PDB, car les assemblys de référence ne peuvent pas être exécutés.</span><span class="sxs-lookup"><span data-stu-id="c9285-104">The `-refonly` parameter silently disables outputting PDBs, as reference assemblies cannot be executed.</span></span>

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a><span data-ttu-id="c9285-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9285-105">Syntax</span></span>

```console
-refonly
```

## <a name="remarks"></a><span data-ttu-id="c9285-106">Notes</span><span class="sxs-lookup"><span data-stu-id="c9285-106">Remarks</span></span>

<span data-ttu-id="c9285-107">Visual Basic prend en charge la `-refout` basculer depuis la version 15.3.</span><span class="sxs-lookup"><span data-stu-id="c9285-107">Visual Basic supports the `-refout` switch starting with version 15.3.</span></span>

<span data-ttu-id="c9285-108">Les assemblys de référence sont uniquement des métadonnées des assemblys qui contiennent des métadonnées, mais aucun code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c9285-108">Reference assemblies are metadata-only assemblies that contain metadata but no implementation code.</span></span> <span data-ttu-id="c9285-109">Elles incluent des informations de type et de membre pour tout sauf les types anonymes.</span><span class="sxs-lookup"><span data-stu-id="c9285-109">They include type and member information for everything except anonymous types.</span></span> <span data-ttu-id="c9285-110">L’utilisation de corps `throw null` (plutôt qu’aucun corps) permet la bonne exécution de PEVerify (et, par voie de conséquence, la validation de la conformité des métadonnées).</span><span class="sxs-lookup"><span data-stu-id="c9285-110">The reason for using `throw null` bodies (as opposed to no bodies) is so that PEVerify could run and pass (thus validating the completeness of the metadata).</span></span>

<span data-ttu-id="c9285-111">Incluent des assemblys de référence de niveau assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut.</span><span class="sxs-lookup"><span data-stu-id="c9285-111">Reference assemblies include an assembly-level [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribute.</span></span> <span data-ttu-id="c9285-112">Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser).</span><span class="sxs-lookup"><span data-stu-id="c9285-112">This attribute may be specified in source (then the compiler won't need to synthesize it).</span></span> <span data-ttu-id="c9285-113">En raison de cet attribut, runtimes refuse charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement).</span><span class="sxs-lookup"><span data-stu-id="c9285-113">Because of this attribute, runtimes will refuse to load reference assemblies for execution (but they can still be loaded in a reflection-only context).</span></span> <span data-ttu-id="c9285-114">Outils réfléchir les assemblys doivent s’assurer de que leur chargement des assemblys de référence en tant que de réflexion uniquement ; Sinon, le runtime lève une <xref:System.BadImageFormatException>.</span><span class="sxs-lookup"><span data-stu-id="c9285-114">Tools that reflect on assemblies need to ensure they load reference assemblies as reflection-only; otherwise, the runtime throws a <xref:System.BadImageFormatException>.</span></span>

<span data-ttu-id="c9285-115">Les options `-refonly` et [`-refout`](refout-compiler-option.md) s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="c9285-115">The `-refonly` and [`-refout`](refout-compiler-option.md) options are mutually exclusive.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9285-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9285-116">See also</span></span>
<span data-ttu-id="c9285-117">[-refout](refout-compiler-option.md) </span><span class="sxs-lookup"><span data-stu-id="c9285-117">[-refout](refout-compiler-option.md) </span></span>  
[<span data-ttu-id="c9285-118">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c9285-118">Visual Basic Command-Line Compiler</span></span>](index.md)  
[<span data-ttu-id="c9285-119">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="c9285-119">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)   
