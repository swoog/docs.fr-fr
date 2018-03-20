---
title: "Types référence (référence C#)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- cs.referencetypes
helpviewer_keywords:
- reference types [C#]
- C# language, reference types
- types [C#], reference types
ms.assetid: 801cf030-6e2d-4a0d-9daf-1431b0c31f47
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e671abac6d49170ac76e4633c4f55c50dcbe01c6
ms.sourcegitcommit: 83dd5ec003e788ccb3e33f3412a7af39ae347646
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2018
---
# <a name="reference-types-c-reference"></a><span data-ttu-id="4c557-102">Types référence (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4c557-102">Reference Types (C# Reference)</span></span>
<span data-ttu-id="4c557-103">Il existe deux genres de types en C# : les types référence et les types valeur.</span><span class="sxs-lookup"><span data-stu-id="4c557-103">There are two kinds of types in C#: reference types and value types.</span></span> <span data-ttu-id="4c557-104">Les variables des types référence font référence à leurs données (objets), tandis que les variables des types valeur contiennent directement leurs données.</span><span class="sxs-lookup"><span data-stu-id="4c557-104">Variables of reference types store references to their data (objects), while variables of value types directly contain their data.</span></span> <span data-ttu-id="4c557-105">Avec les types référence, deux variables peuvent faire référence au même objet ; par conséquent, les opérations sur une variable peuvent affecter le même objet référencé par l'autre variable.</span><span class="sxs-lookup"><span data-stu-id="4c557-105">With reference types, two variables can reference the same object; therefore, operations on one variable can affect the object referenced by the other variable.</span></span> <span data-ttu-id="4c557-106">Avec les types valeur, chaque variable a sa propre copie des données et les opérations sur une variable ne peuvent pas affecter l’autre (sauf pour les variables de paramètre in, ref et out ; consultez les modificateurs de paramètre [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) et [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md)).</span><span class="sxs-lookup"><span data-stu-id="4c557-106">With value types, each variable has its own copy of the data, and it is not possible for operations on one variable to affect the other (except in the case of in, ref and out parameter variables; see [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) and [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) parameter modifier).</span></span>  
  
 <span data-ttu-id="4c557-107">Les mots clés suivants sont utilisés pour déclarer des types référence :</span><span class="sxs-lookup"><span data-stu-id="4c557-107">The following keywords are used to declare reference types:</span></span>  
  
-   [<span data-ttu-id="4c557-108">class</span><span class="sxs-lookup"><span data-stu-id="4c557-108">class</span></span>](../../../csharp/language-reference/keywords/class.md)  
  
-   [<span data-ttu-id="4c557-109">interface</span><span class="sxs-lookup"><span data-stu-id="4c557-109">interface</span></span>](../../../csharp/language-reference/keywords/interface.md)  
  
-   [<span data-ttu-id="4c557-110">delegate</span><span class="sxs-lookup"><span data-stu-id="4c557-110">delegate</span></span>](../../../csharp/language-reference/keywords/delegate.md)  
  
 <span data-ttu-id="4c557-111">C# fournit également les types référence intégrés suivants :</span><span class="sxs-lookup"><span data-stu-id="4c557-111">C# also provides the following built-in reference types:</span></span>  
  
-   [<span data-ttu-id="4c557-112">dynamic</span><span class="sxs-lookup"><span data-stu-id="4c557-112">dynamic</span></span>](../../../csharp/language-reference/keywords/dynamic.md)  
  
-   [<span data-ttu-id="4c557-113">object</span><span class="sxs-lookup"><span data-stu-id="4c557-113">object</span></span>](../../../csharp/language-reference/keywords/object.md)  
  
-   [<span data-ttu-id="4c557-114">string</span><span class="sxs-lookup"><span data-stu-id="4c557-114">string</span></span>](../../../csharp/language-reference/keywords/string.md)  
  
## <a name="see-also"></a><span data-ttu-id="4c557-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c557-115">See Also</span></span>  
 [<span data-ttu-id="4c557-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4c557-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="4c557-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4c557-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="4c557-118">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="4c557-118">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="4c557-119">Types</span><span class="sxs-lookup"><span data-stu-id="4c557-119">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
 [<span data-ttu-id="4c557-120">Types valeur</span><span class="sxs-lookup"><span data-stu-id="4c557-120">Value Types</span></span>](../../../csharp/language-reference/keywords/value-types.md)
