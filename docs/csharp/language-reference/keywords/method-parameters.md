---
title: Paramètres de méthode - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- methods [C#], parameters
- method parameters [C#]
- parameters [C#]
ms.assetid: 680e39ff-775b-48b0-9f47-4186a5bfc4a1
ms.openlocfilehash: 6746b572719b3233f3b99afde3dd8b5c0b7abcf1
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592975"
---
# <a name="method-parameters-c-reference"></a><span data-ttu-id="c04d0-102">Paramètres de méthode (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c04d0-102">Method Parameters (C# Reference)</span></span>

<span data-ttu-id="c04d0-103">Les paramètres déclarés pour une méthode sans [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) ou [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) sont passés à la méthode appelée par valeur.</span><span class="sxs-lookup"><span data-stu-id="c04d0-103">Parameters declared for a method without [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) or [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md), are passed to the called method by value.</span></span> <span data-ttu-id="c04d0-104">Cette valeur peut être modifiée dans la méthode, mais la valeur modifiée n’est pas conservée quand le contrôle repasse à la procédure appelante.</span><span class="sxs-lookup"><span data-stu-id="c04d0-104">That value can be changed in the method, but the changed value will not be retained when control passes back to the calling procedure.</span></span> <span data-ttu-id="c04d0-105">En utilisant un mot clé de paramètre de méthode, vous pouvez modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c04d0-105">By using a method parameter keyword, you can change this behavior.</span></span>  
  
 <span data-ttu-id="c04d0-106">Cette section décrit les mots clés que vous pouvez utiliser pour déclarer des paramètres de méthode :</span><span class="sxs-lookup"><span data-stu-id="c04d0-106">This section describes the keywords you can use when declaring method parameters:</span></span>  
  
- <span data-ttu-id="c04d0-107">[params](../../../csharp/language-reference/keywords/params.md) spécifie que ce paramètre peut prendre un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="c04d0-107">[params](../../../csharp/language-reference/keywords/params.md) specifies that this parameter may take a variable number of arguments.</span></span>
  
- <span data-ttu-id="c04d0-108">[in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) spécifie que ce paramètre est passé par référence, mais qu’il est lu uniquement par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="c04d0-108">[in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) specifies that this parameter is passed by reference but is only read by the called method.</span></span>
  
- <span data-ttu-id="c04d0-109">[ref](../../../csharp/language-reference/keywords/ref.md) spécifie que ce paramètre est passé par référence et qu’il peut être lu ou écrit par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="c04d0-109">[ref](../../../csharp/language-reference/keywords/ref.md) specifies that this parameter is passed by reference and may be read or written by the called method.</span></span>
  
- <span data-ttu-id="c04d0-110">[out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) spécifie que ce paramètre est passé par référence et qu’il est écrit par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="c04d0-110">[out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) specifies that this parameter is passed by reference and is written by the called method.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c04d0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c04d0-111">See also</span></span>

- [<span data-ttu-id="c04d0-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c04d0-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="c04d0-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c04d0-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="c04d0-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="c04d0-114">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
