---
title: -refonly (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- -refonly
helpviewer_keywords:
- /refonly compiler option [Visual Basic]
- -refonly compiler option [Visual Basic]
- refonly compiler option [Visual Basic]
ms.openlocfilehash: b22fb9ae24a04d9fe530811bf764352199c31813
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50036058"
---
# <a name="-refonly-visual-basic"></a><span data-ttu-id="d492f-102">-refonly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d492f-102">-refonly (Visual Basic)</span></span>

<span data-ttu-id="d492f-103">Le **- refonly** option indique que la sortie principale de la compilation doit être un assembly de référence au lieu d’un assembly d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="d492f-103">The **-refonly** option indicates that the primary output of the compilation should be a reference assembly instead of an implementation assembly.</span></span> <span data-ttu-id="d492f-104">Le paramètre `-refonly` désactive sans assistance la génération de fichiers PDB, car les assemblys de référence ne peuvent pas être exécutés.</span><span class="sxs-lookup"><span data-stu-id="d492f-104">The `-refonly` parameter silently disables outputting PDBs, as reference assemblies cannot be executed.</span></span>

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a><span data-ttu-id="d492f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d492f-105">Syntax</span></span>

```console
-refonly
```

## <a name="remarks"></a><span data-ttu-id="d492f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="d492f-106">Remarks</span></span>

<span data-ttu-id="d492f-107">Visual Basic prend en charge la `-refout` basculer à partir de la version 15.3.</span><span class="sxs-lookup"><span data-stu-id="d492f-107">Visual Basic supports the `-refout` switch starting with version 15.3.</span></span>

<span data-ttu-id="d492f-108">Assemblys de référence sont des assemblys de métadonnées uniquement qui contiennent des métadonnées, mais aucun code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="d492f-108">Reference assemblies are metadata-only assemblies that contain metadata but no implementation code.</span></span> <span data-ttu-id="d492f-109">Elles incluent des informations de membre et de type pour tout sauf les types anonymes.</span><span class="sxs-lookup"><span data-stu-id="d492f-109">They include type and member information for everything except anonymous types.</span></span> <span data-ttu-id="d492f-110">L’utilisation de corps `throw null` (plutôt qu’aucun corps) permet la bonne exécution de PEVerify (et, par voie de conséquence, la validation de la conformité des métadonnées).</span><span class="sxs-lookup"><span data-stu-id="d492f-110">The reason for using `throw null` bodies (as opposed to no bodies) is so that PEVerify could run and pass (thus validating the completeness of the metadata).</span></span>

<span data-ttu-id="d492f-111">Assemblys de référence incluent un niveau de l’assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut.</span><span class="sxs-lookup"><span data-stu-id="d492f-111">Reference assemblies include an assembly-level [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribute.</span></span> <span data-ttu-id="d492f-112">Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser).</span><span class="sxs-lookup"><span data-stu-id="d492f-112">This attribute may be specified in source (then the compiler won't need to synthesize it).</span></span> <span data-ttu-id="d492f-113">En raison de cet attribut, runtimes refusent de charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement).</span><span class="sxs-lookup"><span data-stu-id="d492f-113">Because of this attribute, runtimes will refuse to load reference assemblies for execution (but they can still be loaded in a reflection-only context).</span></span> <span data-ttu-id="d492f-114">Les outils reflétés dans les assemblys doivent absolument que charger les assemblys de référence en mode réflexion uniquement ; Sinon, le runtime lève un <xref:System.BadImageFormatException>.</span><span class="sxs-lookup"><span data-stu-id="d492f-114">Tools that reflect on assemblies need to ensure they load reference assemblies as reflection-only; otherwise, the runtime throws a <xref:System.BadImageFormatException>.</span></span>

<span data-ttu-id="d492f-115">Les options `-refonly` et [`-refout`](refout-compiler-option.md) s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="d492f-115">The `-refonly` and [`-refout`](refout-compiler-option.md) options are mutually exclusive.</span></span>

## <a name="see-also"></a><span data-ttu-id="d492f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d492f-116">See also</span></span>
<span data-ttu-id="d492f-117">[-refout](refout-compiler-option.md) </span><span class="sxs-lookup"><span data-stu-id="d492f-117">[-refout](refout-compiler-option.md) </span></span>  
[<span data-ttu-id="d492f-118">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d492f-118">Visual Basic Command-Line Compiler</span></span>](index.md)  
[<span data-ttu-id="d492f-119">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="d492f-119">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)   
