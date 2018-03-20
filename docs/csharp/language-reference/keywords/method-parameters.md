---
title: "Paramètres de méthode (référence C#)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- methods [C#], parameters
- method parameters [C#]
- parameters [C#]
ms.assetid: 680e39ff-775b-48b0-9f47-4186a5bfc4a1
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: b20d2d233350cfb9de55cbd07e722082ec311597
ms.sourcegitcommit: 83dd5ec003e788ccb3e33f3412a7af39ae347646
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2018
---
# <a name="method-parameters-c-reference"></a><span data-ttu-id="c77da-102">Paramètres de méthode (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c77da-102">Method Parameters (C# Reference)</span></span>

<span data-ttu-id="c77da-103">Les paramètres déclarés pour une méthode sans [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) ou [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) sont passés à la méthode appelée par valeur.</span><span class="sxs-lookup"><span data-stu-id="c77da-103">Parameters declared for a method without [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) or [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md), are passed to the called method by value.</span></span> <span data-ttu-id="c77da-104">Cette valeur peut être modifiée dans la méthode, mais la valeur modifiée n’est pas conservée quand le contrôle repasse à la procédure appelante.</span><span class="sxs-lookup"><span data-stu-id="c77da-104">That value can be changed in the method, but the changed value will not be retained when control passes back to the calling procedure.</span></span> <span data-ttu-id="c77da-105">En utilisant un mot clé de paramètre de méthode, vous pouvez modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c77da-105">By using a method parameter keyword, you can change this behavior.</span></span>  
  
 <span data-ttu-id="c77da-106">Cette section décrit les mots clés que vous pouvez utiliser pour déclarer des paramètres de méthode :</span><span class="sxs-lookup"><span data-stu-id="c77da-106">This section describes the keywords you can use when declaring method parameters:</span></span>  
  
-   [<span data-ttu-id="c77da-107">params</span><span class="sxs-lookup"><span data-stu-id="c77da-107">params</span></span>](../../../csharp/language-reference/keywords/params.md)  
  
-   [<span data-ttu-id="c77da-108">in</span><span class="sxs-lookup"><span data-stu-id="c77da-108">in</span></span>](../../../csharp/language-reference/keywords/in-parameter-modifier.md)  
  
-   [<span data-ttu-id="c77da-109">ref</span><span class="sxs-lookup"><span data-stu-id="c77da-109">ref</span></span>](../../../csharp/language-reference/keywords/ref.md)  
  
-   [<span data-ttu-id="c77da-110">out</span><span class="sxs-lookup"><span data-stu-id="c77da-110">out</span></span>](../../../csharp/language-reference/keywords/out-parameter-modifier.md)  
  
## <a name="see-also"></a><span data-ttu-id="c77da-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c77da-111">See Also</span></span>  
 [<span data-ttu-id="c77da-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c77da-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="c77da-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c77da-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="c77da-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="c77da-114">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
