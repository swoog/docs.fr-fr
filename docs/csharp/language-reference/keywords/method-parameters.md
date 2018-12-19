---
title: Paramètres de méthode - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- methods [C#], parameters
- method parameters [C#]
- parameters [C#]
ms.assetid: 680e39ff-775b-48b0-9f47-4186a5bfc4a1
ms.openlocfilehash: f6d0309a91c426123be13a4302d711c92d4ea0f7
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53242709"
---
# <a name="method-parameters-c-reference"></a><span data-ttu-id="d002b-102">Paramètres de méthode (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d002b-102">Method Parameters (C# Reference)</span></span>

<span data-ttu-id="d002b-103">Les paramètres déclarés pour une méthode sans [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) ou [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) sont passés à la méthode appelée par valeur.</span><span class="sxs-lookup"><span data-stu-id="d002b-103">Parameters declared for a method without [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) or [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md), are passed to the called method by value.</span></span> <span data-ttu-id="d002b-104">Cette valeur peut être modifiée dans la méthode, mais la valeur modifiée n’est pas conservée quand le contrôle repasse à la procédure appelante.</span><span class="sxs-lookup"><span data-stu-id="d002b-104">That value can be changed in the method, but the changed value will not be retained when control passes back to the calling procedure.</span></span> <span data-ttu-id="d002b-105">En utilisant un mot clé de paramètre de méthode, vous pouvez modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="d002b-105">By using a method parameter keyword, you can change this behavior.</span></span>  
  
 <span data-ttu-id="d002b-106">Cette section décrit les mots clés que vous pouvez utiliser pour déclarer des paramètres de méthode :</span><span class="sxs-lookup"><span data-stu-id="d002b-106">This section describes the keywords you can use when declaring method parameters:</span></span>  
  
-   <span data-ttu-id="d002b-107">[params](../../../csharp/language-reference/keywords/params.md) spécifie que ce paramètre peut prendre un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="d002b-107">[params](../../../csharp/language-reference/keywords/params.md) specifies that this parameter may take a variable number of arguments.</span></span>
  
-   <span data-ttu-id="d002b-108">[in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) spécifie que ce paramètre est passé par référence, mais qu’il est lu uniquement par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="d002b-108">[in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) specifies that this parameter is passed by reference but is only read by the called method.</span></span>
  
-   <span data-ttu-id="d002b-109">[ref](../../../csharp/language-reference/keywords/ref.md) spécifie que ce paramètre est passé par référence et qu’il peut être lu ou écrit par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="d002b-109">[ref](../../../csharp/language-reference/keywords/ref.md) specifies that this parameter is passed by reference and may be read or written by the called method.</span></span>
  
-   <span data-ttu-id="d002b-110">[out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) spécifie que ce paramètre est passé par référence et qu’il est écrit par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="d002b-110">[out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) specifies that this parameter is passed by reference and is written by the called method.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d002b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d002b-111">See Also</span></span>

- [<span data-ttu-id="d002b-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d002b-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="d002b-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d002b-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="d002b-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="d002b-114">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
