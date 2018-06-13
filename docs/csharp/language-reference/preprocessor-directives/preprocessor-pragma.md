---
title: '#pragma (informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '#pragma'
helpviewer_keywords:
- '#pragma directive [C#]'
ms.assetid: 5b7944cd-d402-46a1-ad8f-feffb2d83673
ms.openlocfilehash: a4829d5062474922d45a2f4f8e1cddf9023b6ad8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33278807"
---
# <a name="pragma-c-reference"></a><span data-ttu-id="b0f4c-102">#pragma (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b0f4c-102">#pragma (C# Reference)</span></span>
<span data-ttu-id="b0f4c-103">La directive `#pragma` fournit au compilateur des instructions spéciales pour la compilation du fichier dans lequel elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="b0f4c-103">`#pragma` gives the compiler special instructions for the compilation of the file in which it appears.</span></span> <span data-ttu-id="b0f4c-104">Les instructions doivent être prises en charge par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="b0f4c-104">The instructions must be supported by the compiler.</span></span> <span data-ttu-id="b0f4c-105">En d’autres termes, vous ne pouvez pas utiliser `#pragma` pour créer des instructions de prétraitement personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b0f4c-105">In other words, you cannot use `#pragma` to create custom preprocessing instructions.</span></span> <span data-ttu-id="b0f4c-106">Le compilateur Microsoft C# prend en charge les deux instructions `#pragma` suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0f4c-106">The Microsoft C# compiler supports the following two `#pragma` instructions:</span></span>  
  
 [<span data-ttu-id="b0f4c-107">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="b0f4c-107">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)  
  
 [<span data-ttu-id="b0f4c-108">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="b0f4c-108">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)  
  
## <a name="syntax"></a><span data-ttu-id="b0f4c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0f4c-109">Syntax</span></span>  
  
```csharp
#pragma pragma-name pragma-arguments  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b0f4c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0f4c-110">Parameters</span></span>  
 `pragma-name`  
 <span data-ttu-id="b0f4c-111">Nom d’une directive pragma reconnue.</span><span class="sxs-lookup"><span data-stu-id="b0f4c-111">The name of a recognized pragma.</span></span>  
  
 `pragma-arguments`  
 <span data-ttu-id="b0f4c-112">Arguments propres à la directive pragma.</span><span class="sxs-lookup"><span data-stu-id="b0f4c-112">Pragma-specific arguments.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0f4c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0f4c-113">See Also</span></span>  
 [<span data-ttu-id="b0f4c-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b0f4c-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="b0f4c-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b0f4c-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="b0f4c-116">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="b0f4c-116">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)  
 [<span data-ttu-id="b0f4c-117">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="b0f4c-117">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)  
 [<span data-ttu-id="b0f4c-118">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="b0f4c-118">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)
