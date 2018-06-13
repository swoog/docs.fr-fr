---
title: Paramètres de méthode (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- methods [C#], parameters
- method parameters [C#]
- parameters [C#]
ms.assetid: 680e39ff-775b-48b0-9f47-4186a5bfc4a1
ms.openlocfilehash: 8a8d300661eec42030900dd9ee85a17e66aa0922
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33269344"
---
# <a name="method-parameters-c-reference"></a><span data-ttu-id="33028-102">Paramètres de méthode (référence C#)</span><span class="sxs-lookup"><span data-stu-id="33028-102">Method Parameters (C# Reference)</span></span>

<span data-ttu-id="33028-103">Les paramètres déclarés pour une méthode sans [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) ou [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) sont passés à la méthode appelée par valeur.</span><span class="sxs-lookup"><span data-stu-id="33028-103">Parameters declared for a method without [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) or [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md), are passed to the called method by value.</span></span> <span data-ttu-id="33028-104">Cette valeur peut être modifiée dans la méthode, mais la valeur modifiée n’est pas conservée quand le contrôle repasse à la procédure appelante.</span><span class="sxs-lookup"><span data-stu-id="33028-104">That value can be changed in the method, but the changed value will not be retained when control passes back to the calling procedure.</span></span> <span data-ttu-id="33028-105">En utilisant un mot clé de paramètre de méthode, vous pouvez modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="33028-105">By using a method parameter keyword, you can change this behavior.</span></span>  
  
 <span data-ttu-id="33028-106">Cette section décrit les mots clés que vous pouvez utiliser pour déclarer des paramètres de méthode :</span><span class="sxs-lookup"><span data-stu-id="33028-106">This section describes the keywords you can use when declaring method parameters:</span></span>  
  
-   <span data-ttu-id="33028-107">[params](../../../csharp/language-reference/keywords/params.md) spécifie que ce paramètre peut prendre un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="33028-107">[params](../../../csharp/language-reference/keywords/params.md) specifies that this parameter may take a variable number of arguments.</span></span>
  
-   <span data-ttu-id="33028-108">[in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) spécifie que ce paramètre est passé par référence, mais qu’il est lu uniquement par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="33028-108">[in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) specifies that this parameter is passed by reference but is only read by the called method.</span></span>
  
-   <span data-ttu-id="33028-109">[ref](../../../csharp/language-reference/keywords/ref.md) spécifie que ce paramètre est passé par référence et qu’il peut être lu ou écrit par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="33028-109">[ref](../../../csharp/language-reference/keywords/ref.md) specifies that this parameter is passed by reference and may be read or written by the called method.</span></span>
  
-   <span data-ttu-id="33028-110">[out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) spécifie que ce paramètre est passé par référence et qu’il est écrit par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="33028-110">[out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) specifies that this parameter is passed by reference and is written by the called method.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33028-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33028-111">See Also</span></span>  
 [<span data-ttu-id="33028-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="33028-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="33028-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="33028-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="33028-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="33028-114">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
