---
title: set, mot clé - Référence C#
ms.custom: seodec18
ms.date: 03/10/2017
f1_keywords:
- set
- set_CSharpKeyword
helpviewer_keywords:
- set keyword [C#]
ms.assetid: 30d7e4e5-cc2e-4635-a597-14a724879619
ms.openlocfilehash: 3020badc8b7873d7feb0b8133d3a181e1c051cbd
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243736"
---
# <a name="set-c-reference"></a><span data-ttu-id="2c8b0-102">set (référence C#)</span><span class="sxs-lookup"><span data-stu-id="2c8b0-102">set (C# Reference)</span></span>

<span data-ttu-id="2c8b0-103">Le mot clé `set` définit une méthode *accessor* dans une propriété ou un indexeur qui assigne une valeur à l’élément de la propriété ou de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-103">The `set` keyword defines an *accessor* method in a property or indexer that assigns a value to the property or the indexer element.</span></span> <span data-ttu-id="2c8b0-104">Pour plus d’informations et des exemples, consultez [Propriétés](../../programming-guide/classes-and-structs/properties.md), [Propriétés implémentées automatiquement](../../programming-guide/classes-and-structs/auto-implemented-properties.md) et [Indexeurs](../../programming-guide/indexers/index.md).</span><span class="sxs-lookup"><span data-stu-id="2c8b0-104">For more information and examples, see [Properties](../../programming-guide/classes-and-structs/properties.md), [Auto-Implemented Properties](../../programming-guide/classes-and-structs/auto-implemented-properties.md), and [Indexers](../../programming-guide/indexers/index.md).</span></span>

<span data-ttu-id="2c8b0-105">L’exemple suivant définit un accesseur `get` et un accesseur `set` pour une propriété nommée `Seconds`.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-105">The following example defines both a `get` and a `set` accessor for a property named `Seconds`.</span></span> <span data-ttu-id="2c8b0-106">Il utilise un champ privé nommé `_seconds` pour stocker la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-106">It uses a private field named `_seconds` to back the property value.</span></span>

[!code-csharp[set#1](~/samples/snippets/csharp/language-reference/keywords/get/get-1.cs)]

<span data-ttu-id="2c8b0-107">Souvent, l’accesseur `set` se compose d’une seule instruction qui retourne une valeur, comme dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-107">Often, the `set` accessor consists of a single statement that returns a value, as it did in the previous example.</span></span> <span data-ttu-id="2c8b0-108">À compter de C# 7.0, vous pouvez implémenter l’accesseur `set` comme membre expression-bodied.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-108">Starting with C# 7.0, you can implement the `set` accessor as an expression-bodied member.</span></span> <span data-ttu-id="2c8b0-109">L’exemple suivant implémente l’accesseur `get` et l’accesseur `set` en tant que membres expression-bodied.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-109">The following example implements both the `get` and the `set` accessors as expression-bodied members.</span></span>

[!code-csharp[set#3](~/samples/snippets/csharp/language-reference/keywords/get/get-3.cs)]
  
<span data-ttu-id="2c8b0-110">Pour les cas simples dans lesquels les accesseurs `get` et `set` d’une propriété n’effectuent aucune autre opération que la définition ou la récupération d’une valeur dans un champ de stockage privé, vous pouvez tirer parti de la prise en charge par le compilateur C# des propriétés implémentées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-110">For simple cases in which a property's `get` and `set` accessors perform no other operation than setting or retrieving a value in a private backing field, you can take advantage of the C# compiler's support for auto-implemented properties.</span></span> <span data-ttu-id="2c8b0-111">L’exemple suivant implémente `Hours` en tant que propriété implémentée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2c8b0-111">The following example implements `Hours` as an auto-implemented property.</span></span> 

[!code-csharp[set#2](~/samples/snippets/csharp/language-reference/keywords/get/get-2.cs)]
  
## <a name="c-language-specification"></a><span data-ttu-id="2c8b0-112">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="2c8b0-112">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="2c8b0-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c8b0-113">See also</span></span>

- [<span data-ttu-id="2c8b0-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="2c8b0-114">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="2c8b0-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2c8b0-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="2c8b0-116">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="2c8b0-116">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="2c8b0-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c8b0-117">Properties</span></span>](../../programming-guide/classes-and-structs/properties.md)