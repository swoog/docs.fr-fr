---
title: '#pragma - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#pragma'
helpviewer_keywords:
- '#pragma directive [C#]'
ms.assetid: 5b7944cd-d402-46a1-ad8f-feffb2d83673
ms.openlocfilehash: 65867bc441711193f93142d1c65122b6bc60c25d
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241825"
---
# <a name="pragma-c-reference"></a><span data-ttu-id="e09c8-102">#pragma (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e09c8-102">#pragma (C# Reference)</span></span>
<span data-ttu-id="e09c8-103">La directive `#pragma` fournit au compilateur des instructions spéciales pour la compilation du fichier dans lequel elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="e09c8-103">`#pragma` gives the compiler special instructions for the compilation of the file in which it appears.</span></span> <span data-ttu-id="e09c8-104">Les instructions doivent être prises en charge par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="e09c8-104">The instructions must be supported by the compiler.</span></span> <span data-ttu-id="e09c8-105">En d’autres termes, vous ne pouvez pas utiliser `#pragma` pour créer des instructions de prétraitement personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e09c8-105">In other words, you cannot use `#pragma` to create custom preprocessing instructions.</span></span> <span data-ttu-id="e09c8-106">Le compilateur Microsoft C# prend en charge les deux instructions `#pragma` suivantes :</span><span class="sxs-lookup"><span data-stu-id="e09c8-106">The Microsoft C# compiler supports the following two `#pragma` instructions:</span></span>  
  
 [<span data-ttu-id="e09c8-107">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="e09c8-107">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)  
  
 [<span data-ttu-id="e09c8-108">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="e09c8-108">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)  
  
## <a name="syntax"></a><span data-ttu-id="e09c8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e09c8-109">Syntax</span></span>  
  
```csharp
#pragma pragma-name pragma-arguments  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e09c8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e09c8-110">Parameters</span></span>  
 `pragma-name`  
 <span data-ttu-id="e09c8-111">Nom d’une directive pragma reconnue.</span><span class="sxs-lookup"><span data-stu-id="e09c8-111">The name of a recognized pragma.</span></span>  
  
 `pragma-arguments`  
 <span data-ttu-id="e09c8-112">Arguments propres à la directive pragma.</span><span class="sxs-lookup"><span data-stu-id="e09c8-112">Pragma-specific arguments.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e09c8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e09c8-113">See Also</span></span>

- [<span data-ttu-id="e09c8-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e09c8-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="e09c8-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e09c8-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="e09c8-116">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="e09c8-116">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)  
- [<span data-ttu-id="e09c8-117">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="e09c8-117">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)  
- [<span data-ttu-id="e09c8-118">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="e09c8-118">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)
