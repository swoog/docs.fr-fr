---
title: Directives de préprocesseur C#
ms.date: 07/20/2015
f1_keywords:
- cs.preprocessor
helpviewer_keywords:
- preprocessor directives [C#]
- keywords [C#], preprocessor directives
ms.assetid: f2406090-b244-4f7e-ab72-3698fefed724
ms.openlocfilehash: 54067777ed2e92eea263b17cce0d4cdf13ed731d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61689318"
---
# <a name="c-preprocessor-directives"></a><span data-ttu-id="51c17-102">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="51c17-102">C# preprocessor directives</span></span>
<span data-ttu-id="51c17-103">Cette section contient des informations sur les directives de préprocesseur C# :</span><span class="sxs-lookup"><span data-stu-id="51c17-103">This section contains information about the following C# preprocessor directives:</span></span>

- [<span data-ttu-id="51c17-104">#if</span><span class="sxs-lookup"><span data-stu-id="51c17-104">#if</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)
- [<span data-ttu-id="51c17-105">#else</span><span class="sxs-lookup"><span data-stu-id="51c17-105">#else</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-else.md)
- [<span data-ttu-id="51c17-106">#elif</span><span class="sxs-lookup"><span data-stu-id="51c17-106">#elif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md)
- [<span data-ttu-id="51c17-107">#endif</span><span class="sxs-lookup"><span data-stu-id="51c17-107">#endif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md)
- [<span data-ttu-id="51c17-108">#define</span><span class="sxs-lookup"><span data-stu-id="51c17-108">#define</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md)
- [<span data-ttu-id="51c17-109">#undef</span><span class="sxs-lookup"><span data-stu-id="51c17-109">#undef</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-undef.md)
- [<span data-ttu-id="51c17-110">#warning</span><span class="sxs-lookup"><span data-stu-id="51c17-110">#warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md)
- [<span data-ttu-id="51c17-111">#error</span><span class="sxs-lookup"><span data-stu-id="51c17-111">#error</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md)
- [<span data-ttu-id="51c17-112">#line</span><span class="sxs-lookup"><span data-stu-id="51c17-112">#line</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-line.md)
- [<span data-ttu-id="51c17-113">#region</span><span class="sxs-lookup"><span data-stu-id="51c17-113">#region</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-region.md)
- [<span data-ttu-id="51c17-114">#endregion</span><span class="sxs-lookup"><span data-stu-id="51c17-114">#endregion</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endregion.md)
- [<span data-ttu-id="51c17-115">#pragma</span><span class="sxs-lookup"><span data-stu-id="51c17-115">#pragma</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma.md)
- [<span data-ttu-id="51c17-116">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="51c17-116">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)
- [<span data-ttu-id="51c17-117">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="51c17-117">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)

<span data-ttu-id="51c17-118">Pour plus d’informations et des exemples, consultez les rubriques spécifiques.</span><span class="sxs-lookup"><span data-stu-id="51c17-118">See the individual topics for more information and examples.</span></span>

<span data-ttu-id="51c17-119">Bien que le compilateur n’ait pas de préprocesseur distinct, les directives décrites dans cette section sont traitées comme si c’était le cas.</span><span class="sxs-lookup"><span data-stu-id="51c17-119">Although the compiler doesn't have a separate preprocessor, the directives described in this section are processed as if there were one.</span></span> <span data-ttu-id="51c17-120">Elles sont utilisées pour faciliter la compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="51c17-120">They are used to help in conditional compilation.</span></span> <span data-ttu-id="51c17-121">Contrairement aux directives C et C++, vous ne pouvez pas les utiliser pour créer des macros.</span><span class="sxs-lookup"><span data-stu-id="51c17-121">Unlike C and C++ directives, you cannot use these directives to create macros.</span></span>

<span data-ttu-id="51c17-122">Une directive de préprocesseur doit être la seule instruction sur une ligne.</span><span class="sxs-lookup"><span data-stu-id="51c17-122">A preprocessor directive must be the only instruction on a line.</span></span>

## <a name="see-also"></a><span data-ttu-id="51c17-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51c17-123">See also</span></span>

- [<span data-ttu-id="51c17-124">Référence C#</span><span class="sxs-lookup"><span data-stu-id="51c17-124">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="51c17-125">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="51c17-125">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
