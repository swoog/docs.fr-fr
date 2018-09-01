---
title: Directives de préprocesseur C#
ms.date: 07/20/2015
f1_keywords:
- cs.preprocessor
helpviewer_keywords:
- preprocessor directives [C#]
- keywords [C#], preprocessor directives
ms.assetid: f2406090-b244-4f7e-ab72-3698fefed724
ms.openlocfilehash: 1c0a97cabce347be0bc9367f3d090a1fc699db19
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43421999"
---
# <a name="c-preprocessor-directives"></a><span data-ttu-id="1fa17-102">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="1fa17-102">C# preprocessor directives</span></span>
<span data-ttu-id="1fa17-103">Cette section contient des informations sur les directives de préprocesseur C# :</span><span class="sxs-lookup"><span data-stu-id="1fa17-103">This section contains information about the following C# preprocessor directives:</span></span>

- [<span data-ttu-id="1fa17-104">#if</span><span class="sxs-lookup"><span data-stu-id="1fa17-104">#if</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)
- [<span data-ttu-id="1fa17-105">#else</span><span class="sxs-lookup"><span data-stu-id="1fa17-105">#else</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-else.md)
- [<span data-ttu-id="1fa17-106">#elif</span><span class="sxs-lookup"><span data-stu-id="1fa17-106">#elif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md)
- [<span data-ttu-id="1fa17-107">#endif</span><span class="sxs-lookup"><span data-stu-id="1fa17-107">#endif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md)
- [<span data-ttu-id="1fa17-108">#define</span><span class="sxs-lookup"><span data-stu-id="1fa17-108">#define</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md)
- [<span data-ttu-id="1fa17-109">#undef</span><span class="sxs-lookup"><span data-stu-id="1fa17-109">#undef</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-undef.md)
- [<span data-ttu-id="1fa17-110">#warning</span><span class="sxs-lookup"><span data-stu-id="1fa17-110">#warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md)
- [<span data-ttu-id="1fa17-111">#error</span><span class="sxs-lookup"><span data-stu-id="1fa17-111">#error</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md)
- [<span data-ttu-id="1fa17-112">#line</span><span class="sxs-lookup"><span data-stu-id="1fa17-112">#line</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-line.md)
- [<span data-ttu-id="1fa17-113">#region</span><span class="sxs-lookup"><span data-stu-id="1fa17-113">#region</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-region.md)
- [<span data-ttu-id="1fa17-114">#endregion</span><span class="sxs-lookup"><span data-stu-id="1fa17-114">#endregion</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endregion.md)
- [<span data-ttu-id="1fa17-115">#pragma</span><span class="sxs-lookup"><span data-stu-id="1fa17-115">#pragma</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma.md)
- [<span data-ttu-id="1fa17-116">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="1fa17-116">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)
- [<span data-ttu-id="1fa17-117">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="1fa17-117">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)

<span data-ttu-id="1fa17-118">Pour plus d’informations et des exemples, consultez les rubriques spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1fa17-118">See the individual topics for more information and examples.</span></span>

<span data-ttu-id="1fa17-119">Bien que le compilateur n’ait pas de préprocesseur distinct, les directives décrites dans cette section sont traitées comme si c’était le cas.</span><span class="sxs-lookup"><span data-stu-id="1fa17-119">Although the compiler doesn't have a separate preprocessor, the directives described in this section are processed as if there were one.</span></span> <span data-ttu-id="1fa17-120">Elles sont utilisées pour faciliter la compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="1fa17-120">They are used to help in conditional compilation.</span></span> <span data-ttu-id="1fa17-121">Contrairement aux directives C et C++, vous ne pouvez pas les utiliser pour créer des macros.</span><span class="sxs-lookup"><span data-stu-id="1fa17-121">Unlike C and C++ directives, you cannot use these directives to create macros.</span></span>

<span data-ttu-id="1fa17-122">Une directive de préprocesseur doit être la seule instruction sur une ligne.</span><span class="sxs-lookup"><span data-stu-id="1fa17-122">A preprocessor directive must be the only instruction on a line.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fa17-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa17-123">See also</span></span>

- [<span data-ttu-id="1fa17-124">Référence C#</span><span class="sxs-lookup"><span data-stu-id="1fa17-124">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="1fa17-125">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1fa17-125">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
